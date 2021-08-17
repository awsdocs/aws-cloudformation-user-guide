# AWS::ApiGateway::DomainName<a name="aws-resource-apigateway-domainname"></a>

The `AWS::ApiGateway::DomainName` resource specifies a custom domain name for your API in API Gateway\.

You can use a custom domain name to provide a URL that's more intuitive and easier to recall\. For more information about using custom domain names, see [Set up Custom Domain Name for an API in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-custom-domains.html) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigateway-domainname-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-domainname-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::DomainName",
  "Properties" : {
      "[CertificateArn](#cfn-apigateway-domainname-certificatearn)" : String,
      "[DomainName](#cfn-apigateway-domainname-domainname)" : String,
      "[EndpointConfiguration](#cfn-apigateway-domainname-endpointconfiguration)" : EndpointConfiguration,
      "[MutualTlsAuthentication](#cfn-apigateway-domainname-mutualtlsauthentication)" : MutualTlsAuthentication,
      "[RegionalCertificateArn](#cfn-apigateway-domainname-regionalcertificatearn)" : String,
      "[SecurityPolicy](#cfn-apigateway-domainname-securitypolicy)" : String,
      "[Tags](#cfn-apigateway-domainname-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-apigateway-domainname-syntax.yaml"></a>

```
Type: AWS::ApiGateway::DomainName
Properties: 
  [CertificateArn](#cfn-apigateway-domainname-certificatearn): String
  [DomainName](#cfn-apigateway-domainname-domainname): String
  [EndpointConfiguration](#cfn-apigateway-domainname-endpointconfiguration): 
    EndpointConfiguration
  [MutualTlsAuthentication](#cfn-apigateway-domainname-mutualtlsauthentication): 
    MutualTlsAuthentication
  [RegionalCertificateArn](#cfn-apigateway-domainname-regionalcertificatearn): String
  [SecurityPolicy](#cfn-apigateway-domainname-securitypolicy): String
  [Tags](#cfn-apigateway-domainname-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-apigateway-domainname-properties"></a>

`CertificateArn`  <a name="cfn-apigateway-domainname-certificatearn"></a>
The reference to an AWS\-managed certificate for use by the edge\-optimized endpoint for this domain name\. AWS Certificate Manager is the only supported source\. For requirements and additional information about setting up certificates, see [Get Certificates Ready in AWS Certificate Manager](https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-custom-domains.html#how-to-custom-domains-prerequisites) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-apigateway-domainname-domainname"></a>
The custom domain name for your API\. Uppercase letters are not supported\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndpointConfiguration`  <a name="cfn-apigateway-domainname-endpointconfiguration"></a>
A list of the endpoint types of the domain name\.  
*Required*: No  
*Type*: [EndpointConfiguration](aws-properties-apigateway-domainname-endpointconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MutualTlsAuthentication`  <a name="cfn-apigateway-domainname-mutualtlsauthentication"></a>
The mutual TLS authentication configuration for a custom domain name\.  
*Required*: No  
*Type*: [MutualTlsAuthentication](aws-properties-apigateway-domainname-mutualtlsauthentication.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegionalCertificateArn`  <a name="cfn-apigateway-domainname-regionalcertificatearn"></a>
The reference to an AWS\-managed certificate for use by the regional endpoint for the domain name\. AWS Certificate Manager is the only supported source\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityPolicy`  <a name="cfn-apigateway-domainname-securitypolicy"></a>
The Transport Layer Security \(TLS\) version \+ cipher suite for this domain name\.  
Valid values include `TLS_1_0` and `TLS_1_2`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-apigateway-domainname-tags"></a>
An array of arbitrary tags \(key\-value pairs\) to associate with the domain name\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-domainname-return-values"></a>

### Ref<a name="aws-resource-apigateway-domainname-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the domain name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apigateway-domainname-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apigateway-domainname-return-values-fn--getatt-fn--getatt"></a>

`DistributionDomainName`  <a name="DistributionDomainName-fn::getatt"></a>
The Amazon CloudFront distribution domain name that's mapped to the custom domain name\. This is only applicable for endpoints whose type is `EDGE`\.  
Example: `d111111abcdef8.cloudfront.net`

`DistributionHostedZoneId`  <a name="DistributionHostedZoneId-fn::getatt"></a>
The region\-agnostic Amazon Route 53 Hosted Zone ID of the edge\-optimized endpoint\. The only valid value is `Z2FDTNDATAQYW2` for all regions\.

`RegionalDomainName`  <a name="RegionalDomainName-fn::getatt"></a>
The domain name associated with the regional endpoint for this custom domain name\. You set up this association by adding a DNS record that points the custom domain name to this regional domain name\.

`RegionalHostedZoneId`  <a name="RegionalHostedZoneId-fn::getatt"></a>
The region\-specific Amazon Route 53 Hosted Zone ID of the regional endpoint\.

## Examples<a name="aws-resource-apigateway-domainname--examples"></a>



### Create Custom Domain<a name="aws-resource-apigateway-domainname--examples--Create_Custom_Domain"></a>

The following example creates a custom domain name of `api.mydomain.com`\.

#### JSON<a name="aws-resource-apigateway-domainname--examples--Create_Custom_Domain--json"></a>

```
{
    "MyDomainName": {
        "Type": "AWS::ApiGateway::DomainName",
        "Properties": {
            "DomainName": "api.mydomain.com",
            "CertificateArn": "arn:aws:acm:us-east-1:111122223333:certificate/fb1b9770-a305-495d-aefb-27e5e101ff3"
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-domainname--examples--Create_Custom_Domain--yaml"></a>

```
MyDomainName:
  Type: 'AWS::ApiGateway::DomainName'
  Properties:
    DomainName: api.mydomain.com
    CertificateArn: >-
      arn:aws:acm:us-east-1:111122223333:certificate/fb1b9770-a305-495d-aefb-27e5e101ff3
```

### Create Custom Domain from Parameters<a name="aws-resource-apigateway-domainname--examples--Create_Custom_Domain_from_Parameters"></a>

The following example creates a custom domain name of `example.mydomain.com`\.

#### JSON<a name="aws-resource-apigateway-domainname--examples--Create_Custom_Domain_from_Parameters--json"></a>

```
{
    "Parameters": {
        "basePath": {
            "Type": "String",
            "Default": "examplepath"
        },
        "domainName": {
            "Type": "String",
            "Default": "example.mydomain.com"
        },
        "restApiName": {
            "Type": "String",
            "Default": "exampleapi"
        }
    },
    "Resources": {
        "myCertificate": {
            "Type": "AWS::CertificateManager::Certificate",
            "Properties": {
                "DomainName": {
                    "Ref": "domainName"
                }
            }
        },
        "myDomainName": {
            "Type": "AWS::ApiGateway::DomainName",
            "Properties": {
                "CertificateArn": {
                    "Ref": "myCertificate"
                },
                "DomainName": {
                    "Ref": "domainName"
                }
            }
        },
        "myMapping": {
            "Type": "AWS::ApiGateway::BasePathMapping",
            "Properties": {
                "BasePath": {
                    "Ref": "basePath"
                },
                "DomainName": {
                    "Ref": "myDomainName"
                },
                "RestApiId": {
                    "Ref": "myRestApi"
                }
            }
        },
        "myRestApi": {
            "Type": "AWS::ApiGateway::RestApi",
            "Properties": {
                "Name": {
                    "Ref": "restApiName"
                }
            }
        }
    },
    "Outputs": {
        "domainName": {
            "Value": {
                "Fn::GetAtt": [
                    "myDomainName",
                    "DistributionDomainName"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-domainname--examples--Create_Custom_Domain_from_Parameters--yaml"></a>

```
Parameters:
  basePath:
    Type: String
    Default: examplepath
  domainName:
    Type: String
    Default: example.mydomain.com
  restApiName:
    Type: String
    Default: exampleapi
Resources:
  myCertificate:
    Type: 'AWS::CertificateManager::Certificate'
    Properties:
      DomainName: !Ref domainName
  myDomainName:
    Type: 'AWS::ApiGateway::DomainName'
    Properties:
      CertificateArn: !Ref myCertificate
      DomainName: !Ref domainName
  myMapping:
    Type: 'AWS::ApiGateway::BasePathMapping'
    Properties:
      BasePath: !Ref basePath
      DomainName: !Ref myDomainName
      RestApiId: !Ref myRestApi
  myRestApi:
    Type: 'AWS::ApiGateway::RestApi'
    Properties:
      Name: !Ref restApiName
Outputs:
  domainName:
    Value: !GetAtt 
      - myDomainName
      - DistributionDomainName
```

### Create domain name with EndpointConfiguration<a name="aws-resource-apigateway-domainname--examples--Create_domain_name_with_EndpointConfiguration"></a>

The following example creates a custom domain name that specifies a regional certificate ARN and an endpoint type\.

#### JSON<a name="aws-resource-apigateway-domainname--examples--Create_domain_name_with_EndpointConfiguration--json"></a>

```
{
  "Parameters": {
    "cfnDomainName": {
      "Type": "String"
    },
    "certificateArn": {
      "Type": "String"
    },
    "type": {
      "Type": "String"
    }
  },
  "Resources": {
    "myDomainName": {
      "Type": "AWS::ApiGateway::DomainName",
      "Properties": {
        "CertificateArn": {
          "Ref": "certificateArn"
        },
        "DomainName": {
          "Ref": "cfnDomainName"
        },
        "EndpointConfiguration": {
          "Types": [
            {
              "Ref": "type"
            }
          ]
        },
        "RegionalCertificateArn": {
          "Ref": "certificateArn"
        }
      }
    }
  },
  "Outputs": {  
    "DomainName": {
      "Value": {
        "Ref": "myDomainName"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-apigateway-domainname--examples--Create_domain_name_with_EndpointConfiguration--yaml"></a>

```
Parameters:
  cfnDomainName:
    Type: String
  certificateArn:
    Type: String
  type:
    Type: String
Resources:
  myDomainName:
    Type: AWS::ApiGateway::DomainName
    Properties:
      CertificateArn: !Ref certificateArn
      DomainName: !Ref cfnDomainName
      EndpointConfiguration:
        Types:
          - !Ref type
      RegionalCertificateArn: !Ref certificateArn
Outputs:  
  DomainName:
    Value: !Ref myDomainName
```

### Create Domain Names and Zone IDs as Outputs<a name="aws-resource-apigateway-domainname--examples--Create_Domain_Names_and_Zone_IDs_as_Outputs"></a>

The following example defines the distribution and regional domain names, as well as the distribution and regional hosted zone IDs, as outputs from the stack\.

#### JSON<a name="aws-resource-apigateway-domainname--examples--Create_Domain_Names_and_Zone_IDs_as_Outputs--json"></a>

```
{
    "Resources": {
        "myDomainName": {
            "Type": "AWS::ApiGateway::DomainName",
            "Properties": {
                "CertificateArn": {
                    "Ref": "certificateArn"
                },
                "DomainName": {
                    "Ref": "cfnDomainName"
                },
                "EndpointConfiguration": {
                    "Types": [
                        {
                            "Ref": "type"
                        }
                    ]
                },
                "RegionalCertificateArn": {
                    "Ref": "certificateArn"
                }
            }
        }
    },
    "Outputs": {
        "DistributionDomainName": {
            "Value": {
                "Fn::GetAtt": [
                    "myDomainName",
                    "DistributionDomainName"
                ]
            }
        },
        "DistributionHostedZoneId": {
            "Value": {
                "Fn::GetAtt": [
                    "myDomainName",
                    "DistributionHostedZoneId"
                ]
            }
        },
        "RegionalDomainName": {
            "Value": {
                "Fn::GetAtt": [
                    "myDomainName",
                    "RegionalDomainName"
                ]
            }
        },
        "RegionalHostedZoneId": {
            "Value": {
                "Fn::GetAtt": [
                    "myDomainName",
                    "RegionalHostedZoneId"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-domainname--examples--Create_Domain_Names_and_Zone_IDs_as_Outputs--yaml"></a>

```
Resources:
  myDomainName:
    Type: 'AWS::ApiGateway::DomainName'
    Properties:
      CertificateArn: !Ref certificateArn
      DomainName: !Ref cfnDomainName
      EndpointConfiguration:
        Types:
          - !Ref type
      RegionalCertificateArn: !Ref certificateArn
Outputs:
  DistributionDomainName:
    Value: !GetAtt 
      - myDomainName
      - DistributionDomainName
  DistributionHostedZoneId:
    Value: !GetAtt 
      - myDomainName
      - DistributionHostedZoneId
  RegionalDomainName:
    Value: !GetAtt 
      - myDomainName
      - RegionalDomainName
  RegionalHostedZoneId:
    Value: !GetAtt 
      - myDomainName
      - RegionalHostedZoneId
```

## See also<a name="aws-resource-apigateway-domainname--seealso"></a>
+ [domainname:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/domainname-create/) in the *Amazon API Gateway REST API Reference*

