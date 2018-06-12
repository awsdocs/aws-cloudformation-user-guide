# AWS::ApiGateway::DomainName<a name="aws-resource-apigateway-domainname"></a>

<a name="aws-resource-apigateway-domainname.desc"></a>The `AWS::ApiGateway::DomainName` resource specifies a custom domain name for your API in Amazon API Gateway \(API Gateway\)\.

You can use a custom domain name to provide a URL that's more intuitive and easier to recall\. For more information about using custom domain names, see [Use Custom Domain Name as API Gateway API Host Name](http://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-custom-domains.html) in the *API Gateway Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-apigateway-domainname-syntax)
+ [Properties](#aws-resource-apigateway-domainname-properties)
+ [Return Values](#aws-resource-apigateway-domainname-returnvalues)
+ [Examples](#aws-resource-apigateway-domainname-examples)
+ [See Also](#aws-resource-apigateway-domainname-seealso)

## Syntax<a name="aws-resource-apigateway-domainname-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-domainname-syntax.json"></a>

```
{
  "Type": "AWS::ApiGateway::DomainName",
  "Properties": {
    "[CertificateArn](#cfn-apigateway-domainname-certificatearn)": String,
    "[DomainName](#cfn-apigateway-domainname-domainname)": String,
    "[EndpointConfiguration](#cfn-apigateway-domainname-endpointconfiguration)" : [*EndpointConfiguration*](aws-properties-apigateway-domainname-endpointconfiguration.md),
    "[RegionalCertificateArn](#cfn-apigateway-domainname-regionalcertificatearn)" : String
  }
}
```

### YAML<a name="aws-resource-apigateway-domainname-syntax.yaml"></a>

```
Type: "AWS::ApiGateway::DomainName"
Properties: 
  [CertificateArn](#cfn-apigateway-domainname-certificatearn): String
  [DomainName](#cfn-apigateway-domainname-domainname): String
  [EndpointConfiguration](#cfn-apigateway-domainname-endpointconfiguration): 
    [*EndpointConfiguration*](aws-properties-apigateway-domainname-endpointconfiguration.md)
  [RegionalCertificateArn](#cfn-apigateway-domainname-regionalcertificatearn): String
```

## Properties<a name="aws-resource-apigateway-domainname-properties"></a>

`CertificateArn`  <a name="cfn-apigateway-domainname-certificatearn"></a>
The reference to an AWS\-managed certificate for use by the edge\-optimized endpoint for this domain name\. AWS Certificate Manager is the only supported source\. For requirements and additional information about setting up certificates, see [Get Certificates Ready in AWS Certificate Manager](http://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-custom-domains.html#how-to-custom-domains-prerequisites) in the *API Gateway Developer Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DomainName`  <a name="cfn-apigateway-domainname-domainname"></a>
The custom domain name for your API in Amazon API Gateway\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EndpointConfiguration`  <a name="cfn-apigateway-domainname-endpointconfiguration"></a>
A list of the endpoint types of the domain name\.  
 *Required*: No  
 *Type*: [API Gateway DomainName EndpointConfiguration](aws-properties-apigateway-domainname-endpointconfiguration.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`RegionalCertificateArn`  <a name="cfn-apigateway-domainname-regionalcertificatearn"></a>
The reference to an AWS\-managed certificate for use by the regional endpoint for the domain name\. AWS Certificate Manager is the only supported source\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-apigateway-domainname-returnvalues"></a>

### Ref<a name="w3ab2c21c10c49c13b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the domain name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10c49c13b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. This section lists the available attribute and a sample return value\.

`DistributionDomainName`  
The Amazon CloudFront distribution domain name that's mapped to the custom domain name\.  
Example: `d111111abcdef8.cloudfront.net`

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-apigateway-domainname-examples"></a>

### Create Custom Domain<a name="aws-resource-apigateway-domainname-example1"></a>

The following example creates a custom domain name of `api.mydomain.com`\.

#### JSON<a name="aws-resource-apigateway-domainname-example1.json"></a>

```
"MyDomainName": {
  "Type": "AWS::ApiGateway::DomainName",
  "Properties": {
    "DomainName": "api.mydomain.com",
    "CertificateArn": "arn:aws:acm:us-east-1:111122223333:certificate/fb1b9770-a305-495d-aefb-27e5e101ff3"
  }
}
```

#### YAML<a name="aws-resource-apigateway-domainname-example1.yaml"></a>

```
MyDomainName:
  Type: 'AWS::ApiGateway::DomainName'
  Properties:
    DomainName: api.mydomain.com
    CertificateArn: arn:aws:acm:us-east-1:111122223333:certificate/fb1b9770-a305-495d-aefb-27e5e101ff3
```

### Create Custom Domain from Parameters<a name="aws-resource-apigateway-domainname-example2"></a>

The following example creates a custom domain name of `example.mydomain.com`\.

#### JSON<a name="aws-resource-apigateway-domainname-example2.json"></a>

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

#### YAML<a name="aws-resource-apigateway-domainname-example2.yaml"></a>

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

### <a name="aws-resource-apigateway-domainname-example3"></a>

The following example creates a custom domain name that specifies a regional certificate ARN and an endpoint type\.

#### JSON<a name="aws-resource-apigateway-domainname-example3.json"></a>

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
    },
    "DomainName": {
      "Value": {
        "Ref": "myDomainName"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-apigateway-domainname-example3.yaml"></a>

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
    Type: 'AWS::ApiGateway::DomainName'
    Properties:
      CertificateArn: !Ref certificateArn
      DomainName: !Ref cfnDomainName
      EndpointConfiguration:
        Types:
          - !Ref type
      RegionalCertificateArn: !Ref certificateArn
  DomainName:
    Value: !Ref myDomainName
```

## See Also<a name="aws-resource-apigateway-domainname-seealso"></a>
+ [domainname:create](http://docs.aws.amazon.com/apigateway/api-reference/link-relation/domainname-create/) operation in the *Amazon API Gateway REST API Reference*