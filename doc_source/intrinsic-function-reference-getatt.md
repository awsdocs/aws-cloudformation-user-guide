# `Fn::GetAtt`<a name="intrinsic-function-reference-getatt"></a>

The `Fn::GetAtt` intrinsic function returns the value of an attribute from a resource in the template\. When the [`AWS::LanguageExtensions` transform](transform-aws-languageextensions.md) transform is used, you can use intrinsic functions as a parameter to `Fn::GetAtt`\. For more information about `GetAtt` return values for a particular resource, refer to the documentation for that resource in the [Resource and property reference](aws-template-resource-type-ref.md)\.

## Declaration<a name="getatt-declaration"></a>

### JSON<a name="intrinsic-function-reference-getatt-syntax.json"></a>

```
{ "Fn::GetAtt" : [ "logicalNameOfResource", "attributeName" ] }
```

### YAML<a name="intrinsic-function-reference-getatt-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::GetAtt: [ logicalNameOfResource, attributeName ]
```

Syntax for the short form:

```
!GetAtt logicalNameOfResource.attributeName
```

## Parameters<a name="getatt-parameters"></a>

`logicalNameOfResource`  
The logical name \(also called *logical ID*\) of the resource that contains the attribute that you want\.

`attributeName`  
The name of the resource\-specific attribute whose value you want\. See the resource's reference page for details about the attributes available for that resource type\.

## Return value<a name="intrinsic-function-reference-getatt-return"></a>

The attribute value\.

## Examples<a name="intrinsic-function-reference-getatt-examples"></a>

### Return a string<a name="intrinsic-function-reference-getatt-example"></a>

This example snippet returns a string containing the DNS name of the load balancer with the logical name `myELB`\.

#### JSON<a name="intrinsic-function-reference-getatt-example.json"></a>

```
1. "Fn::GetAtt" : [ "myELB" , "DNSName" ]
```

#### YAML<a name="intrinsic-function-reference-getatt-example.yaml"></a>

```
1. !GetAtt myELB.DNSName
```

#### Return multiple strings<a name="intrinsic-function-reference-getatt-example2"></a>

The following example template returns the `SourceSecurityGroup.OwnerAlias` and `SourceSecurityGroup.GroupName` of the load balancer with the logical name `myELB`\.

##### JSON<a name="intrinsic-function-reference-getatt-example2.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "myELB": {
            "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
            "Properties": {
                "AvailabilityZones": [
                    "eu-west-1a"
                ],
                "Listeners": [
                    {
                        "LoadBalancerPort": "80",
                        "InstancePort": "80",
                        "Protocol": "HTTP"
                    }
                ]
            }
        },
        "myELBIngressGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "ELB ingress group",
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": 80,
                        "ToPort": 80,
                        "SourceSecurityGroupOwnerId": {
                            "Fn::GetAtt": [
                                "myELB",
                                "SourceSecurityGroup.OwnerAlias"
                            ]
                        },
                        "SourceSecurityGroupName": {
                            "Fn::GetAtt": [
                                "myELB",
                                "SourceSecurityGroup.GroupName"
                            ]
                        }
                    }
                ]
            }
        }
    }
}
```

##### YAML<a name="intrinsic-function-reference-getatt-example2.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myELB:
    Type: AWS::ElasticLoadBalancing::LoadBalancer
    Properties:
      AvailabilityZones:
        - eu-west-1a
      Listeners:
        - LoadBalancerPort: '80'
          InstancePort: '80'
          Protocol: HTTP
  myELBIngressGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: ELB ingress group
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: 80
          ToPort: 80
          SourceSecurityGroupOwnerId: !GetAtt myELB.SourceSecurityGroup.OwnerAlias
          SourceSecurityGroupName: !GetAtt myELB.SourceSecurityGroup.GroupName
```

#### Example: Use a standard Identifier for multiple resources using `Fn::Sub` within `Fn::GetAtt`, `Ref` and `Fn::ForEach`<a name="intrinsic-function-reference-getatt-foreach"></a>

The following examples shows how to use [`Fn::GetAtt`](#intrinsic-function-reference-getatt) with [`Fn::Sub`](intrinsic-function-reference-sub.md), in conjuction with [`Fn::ForEach`](intrinsic-function-reference-foreach.md), in the [Outputs](outputs-section-structure.md) of a template to reduce the template length and verbosity\. The use of [`Fn::Sub`](intrinsic-function-reference-sub.md) within [`Fn::GetAtt`](#intrinsic-function-reference-getatt) allows the template to contain one intrinsic function that can reference a different bucket at every iteration of the [`Fn::ForEach`](intrinsic-function-reference-foreach.md) call\. 

##### JSON<a name="intrinsic-function-reference-getatt-foreach.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Transform": "AWS::LanguageExtensions",
    "Mappings": {
        "Buckets": {
            "Properties": {
                "Identifiers": ["A", "B", "C"]
            }
        }
    },
    "Resources": {
        "Fn::ForEach::Buckets": [
            "Identifier",
            {"Fn::FindInMap": ["Buckets", "Properties", "Identifiers"]},
            {
                "S3Bucket${Identifier}": {
                    "Type": "AWS::S3::Bucket",
                    "Properties": {
                        "AccessControl": "PublicRead",
                        "MetricsConfigurations": [
                            {
                                "Id": {"Fn::Sub": "EntireBucket${Identifier}"}
                            }
                        ],
                        "WebsiteConfiguration": {
                            "IndexDocument": "index.html",
                            "ErrorDocument": "error.html",
                            "RoutingRules": [
                                {
                                    "RoutingRuleCondition": {
                                        "HttpErrorCodeReturnedEquals": "404",
                                        "KeyPrefixEquals": "out1/"
                                    },
                                    "RedirectRule": {
                                        "HostName": "ec2-11-22-333-44.compute-1.amazonaws.com",
                                        "ReplaceKeyPrefixWith": "report-404/"
                                    }
                                }
                            ]
                        }
                    },
                    "DeletionPolicy": "Retain",
                    "UpdateReplacePolicy": "Retain"
                }
            }
        ]
    },
    "Outputs": {
        "Fn::ForEach::BucketOutputs": [
            "Identifier",
            {"Fn::FindInMap": ["Buckets", "Properties", "Identifiers"]},
            {
                "Fn::ForEach::GetAttLoop": [
                    "Property",
                    ["Arn", "DomainName", "WebsiteURL"],
                    {
                        "S3Bucket${Identifier}${Property}": {
                            "Value": {
                                "Fn::GetAtt": [{"Fn::Sub": "S3Bucket${Identifier}"}, {"Ref": "Property"}]
                            }
                        }
                    }
                ]
            }
        ]
    }
}
```

##### YAML<a name="intrinsic-function-reference-getatt-foreach.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Transform: 'AWS::LanguageExtensions'
Mappings:
  Buckets:
    Properties:
      Identifiers:
        - A
        - B
        - C
Resources:
  'Fn::ForEach::Buckets':
    - Identifier
    - Fn::FindInMap: 
      - Buckets
      - Properties
      - Identifiers
    - 'S3Bucket${Identifier}':
        Type: 'AWS::S3::Bucket'
        Properties:
          AccessControl: PublicRead
          MetricsConfigurations:
            - Id: 
                Fn::Sub: 'EntireBucket${Identifier}'
          WebsiteConfiguration:
            IndexDocument: index.html
            ErrorDocument: error.html
            RoutingRules:
              - RoutingRuleCondition:
                  HttpErrorCodeReturnedEquals: '404'
                  KeyPrefixEquals: out1/
                RedirectRule:
                  HostName: ec2-11-22-333-44.compute-1.amazonaws.com
                  ReplaceKeyPrefixWith: report-404/
        DeletionPolicy: Retain
        UpdateReplacePolicy: Retain
Outputs:
  'Fn::ForEach::BucketOutputs':
    - Identifier
    - Fn::FindInMap:
      - Buckets
      - Properties
      - Identifiers
    - 'Fn::ForEach::GetAttLoop':
        - Property
        - - Arn
          - DomainName
          - WebsiteURL
        - 'S3Bucket${Identifier}${Property}':
            Value: !GetAtt 
              - !Sub 'S3Bucket${Identifier}'
              - !Ref Property
```

## Supported functions<a name="getatt-supported-functions"></a>

When the [`AWS::LanguageExtensions` transform](transform-aws-languageextensions.md) transform is not used:
+ The `Fn::GetAtt` logical resource name can't use functions\. You must specify a string that's a resource's logical ID\. For the `Fn::GetAtt` attribute name, you can use the ``Ref`` function\.
+ The `Fn::GetAtt` attribute name can use the ``Ref`` function\.

When the [`AWS::LanguageExtensions` transform](transform-aws-languageextensions.md) transform is used, within the `Fn::GetAtt` function, you can use the following functions\. This is true with either the `Fn::GetAtt` logical resource name or the `Fn::GetAtt` attribute name\.
+ ``Fn::Base64``
+ ``Fn::FindInMap``
+ ``Fn::If``
+ ``Fn::Join``
+ ``Fn::Sub``
+ ``Fn::ToJsonString``
+ ``Ref``