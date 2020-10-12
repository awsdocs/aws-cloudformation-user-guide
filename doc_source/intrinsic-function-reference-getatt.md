# `Fn::GetAtt`<a name="intrinsic-function-reference-getatt"></a>

The `Fn::GetAtt` intrinsic function returns the value of an attribute from a resource in the template\. For more information about `GetAtt` return values for a particular resource, refer to the documentation for that resource in the [Resource and property reference](aws-template-resource-type-ref.md)\.

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

## Supported functions<a name="getatt-supported-functions"></a>

For the `Fn::GetAtt` logical resource name, you cannot use functions\. You must specify a string that is a resource's logical ID\.

For the `Fn::GetAtt` attribute name, you can use the `Ref` function\.