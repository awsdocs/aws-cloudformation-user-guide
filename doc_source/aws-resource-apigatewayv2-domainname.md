# AWS::ApiGatewayV2::DomainName<a name="aws-resource-apigatewayv2-domainname"></a>

The `AWS::ApiGatewayV2::DomainName` resource specifies a custom domain name for your API in Amazon API Gateway \(API Gateway\)\. 

You can use a custom domain name to provide a URL that's more intuitive and easier to recall\. For more information about using custom domain names, see [Set up Custom Domain Name for an API in API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/how-to-custom-domains.html) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigatewayv2-domainname-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-domainname-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::DomainName",
  "Properties" : {
      "[DomainName](#cfn-apigatewayv2-domainname-domainname)" : String,
      "[DomainNameConfigurations](#cfn-apigatewayv2-domainname-domainnameconfigurations)" : [ DomainNameConfiguration, ... ],
      "[MutualTlsAuthentication](#cfn-apigatewayv2-domainname-mutualtlsauthentication)" : MutualTlsAuthentication,
      "[Tags](#cfn-apigatewayv2-domainname-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-domainname-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::DomainName
Properties: 
  [DomainName](#cfn-apigatewayv2-domainname-domainname): String
  [DomainNameConfigurations](#cfn-apigatewayv2-domainname-domainnameconfigurations): 
    - DomainNameConfiguration
  [MutualTlsAuthentication](#cfn-apigatewayv2-domainname-mutualtlsauthentication): 
    MutualTlsAuthentication
  [Tags](#cfn-apigatewayv2-domainname-tags): Json
```

## Properties<a name="aws-resource-apigatewayv2-domainname-properties"></a>

`DomainName`  <a name="cfn-apigatewayv2-domainname-domainname"></a>
The custom domain name for your API in Amazon API Gateway\. Uppercase letters are not supported\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DomainNameConfigurations`  <a name="cfn-apigatewayv2-domainname-domainnameconfigurations"></a>
The domain name configurations\.  
*Required*: No  
*Type*: List of [DomainNameConfiguration](aws-properties-apigatewayv2-domainname-domainnameconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MutualTlsAuthentication`  <a name="cfn-apigatewayv2-domainname-mutualtlsauthentication"></a>
The mutual TLS authentication configuration for a custom domain name\.  
*Required*: No  
*Type*: [MutualTlsAuthentication](aws-properties-apigatewayv2-domainname-mutualtlsauthentication.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-apigatewayv2-domainname-tags"></a>
The collection of tags associated with a domain name\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-domainname-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-domainname-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the domain name, such as `example.mydomain.com`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apigatewayv2-domainname-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apigatewayv2-domainname-return-values-fn--getatt-fn--getatt"></a>

`RegionalDomainName`  <a name="RegionalDomainName-fn::getatt"></a>
The domain name associated with the regional endpoint for this custom domain name\. You set up this association by adding a DNS record that points the custom domain name to this regional domain name\.

`RegionalHostedZoneId`  <a name="RegionalHostedZoneId-fn::getatt"></a>
The region\-specific Amazon Route 53 Hosted Zone ID of the regional endpoint\.

## Examples<a name="aws-resource-apigatewayv2-domainname--examples"></a>



### Domain name creation example<a name="aws-resource-apigatewayv2-domainname--examples--Domain_name_creation_example"></a>

The following example creates a `DomainName` resource called `MyDomainName`\.

#### JSON<a name="aws-resource-apigatewayv2-domainname--examples--Domain_name_creation_example--json"></a>

```
{
    "MyDomainName": {
        "Type": "AWS::ApiGatewayV2::DomainName",
        "Properties": {
            "DomainName": "mydomainame.us-east-1.com",
            "DomainNameConfigurations": [
                {
                    "EndpointType": "REGIONAL",
                    "CertificateArn": "arn:aws:acm:us-east-1:123456789012:certificate/1a2b3c4d-aaaa-aaaa-aaaa-1a2b3c4d5e6f",
                    "CertificateName": "testCertificate"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-apigatewayv2-domainname--examples--Domain_name_creation_example--yaml"></a>

```
MyDomainName:
  Type: 'AWS::ApiGatewayV2::DomainName'
  Properties:
    DomainName: mydomainame.us-east-1.com
    DomainNameConfigurations:
      - EndpointType: REGIONAL
        CertificateArn: >-
          arn:aws:acm:us-east-1:123456789012:certificate/1a2b3c4d-aaaa-aaaa-aaaa-1a2b3c4d5e6f
        CertificateName: testCertificate
```

## See also<a name="aws-resource-apigatewayv2-domainname--seealso"></a>
+ [CreateDomainName](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/domainnames.html#CreateDomainName) in the *Amazon API Gateway Version 2 API Reference*

