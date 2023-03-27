# AWS::AppSync::DomainName<a name="aws-resource-appsync-domainname"></a>

The `AWS::AppSync::DomainName` resource creates a `DomainNameConfig` object to configure a custom domain\.

## Syntax<a name="aws-resource-appsync-domainname-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-domainname-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::DomainName",
  "Properties" : {
      "[CertificateArn](#cfn-appsync-domainname-certificatearn)" : String,
      "[Description](#cfn-appsync-domainname-description)" : String,
      "[DomainName](#cfn-appsync-domainname-domainname)" : String
    }
}
```

### YAML<a name="aws-resource-appsync-domainname-syntax.yaml"></a>

```
Type: AWS::AppSync::DomainName
Properties: 
  [CertificateArn](#cfn-appsync-domainname-certificatearn): String
  [Description](#cfn-appsync-domainname-description): String
  [DomainName](#cfn-appsync-domainname-domainname): String
```

## Properties<a name="aws-resource-appsync-domainname-properties"></a>

`CertificateArn`  <a name="cfn-appsync-domainname-certificatearn"></a>
The Amazon Resource Name \(ARN\) of the certificate\. This will be an AWS Certificate Manager certificate\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-appsync-domainname-description"></a>
The decription for your domain name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-appsync-domainname-domainname"></a>
The domain name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appsync-domainname-return-values"></a>

### Ref<a name="aws-resource-appsync-domainname-return-values-ref"></a>

When you pass the logical ID of an `AWS::AppSync::DomainName` resource to the intrinsic `Ref` function, the function returns the domain name\.

 For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref)\. 

### Fn::GetAtt<a name="aws-resource-appsync-domainname-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt)\. 

#### <a name="aws-resource-appsync-domainname-return-values-fn--getatt-fn--getatt"></a>

`AppSyncDomainName`  <a name="AppSyncDomainName-fn::getatt"></a>
The domain name provided by AWS AppSync\.

`DomainName`  <a name="DomainName-fn::getatt"></a>
The domain name\.

`HostedZoneId`  <a name="HostedZoneId-fn::getatt"></a>
The ID of your Amazon Route 53 hosted zone\.