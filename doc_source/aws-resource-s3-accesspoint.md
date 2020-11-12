# AWS::S3::AccessPoint<a name="aws-resource-s3-accesspoint"></a>

The AWS::S3::AccessPoint resource is an Amazon S3 resource type that you can use to access buckets\.

## Syntax<a name="aws-resource-s3-accesspoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3-accesspoint-syntax.json"></a>

```
{
  "Type" : "AWS::S3::AccessPoint",
  "Properties" : {
      "[Bucket](#cfn-s3-accesspoint-bucket)" : String,
      "[CreationDate](#cfn-s3-accesspoint-creationdate)" : String,
      "[Name](#cfn-s3-accesspoint-name)" : String,
      "[NetworkOrigin](#cfn-s3-accesspoint-networkorigin)" : String,
      "[Policy](#cfn-s3-accesspoint-policy)" : Json,
      "[PolicyStatus](#cfn-s3-accesspoint-policystatus)" : Json,
      "[PublicAccessBlockConfiguration](#cfn-s3-accesspoint-publicaccessblockconfiguration)" : PublicAccessBlockConfiguration,
      "[VpcConfiguration](#cfn-s3-accesspoint-vpcconfiguration)" : VpcConfiguration
    }
}
```

### YAML<a name="aws-resource-s3-accesspoint-syntax.yaml"></a>

```
Type: AWS::S3::AccessPoint
Properties: 
  [Bucket](#cfn-s3-accesspoint-bucket): String
  [CreationDate](#cfn-s3-accesspoint-creationdate): String
  [Name](#cfn-s3-accesspoint-name): String
  [NetworkOrigin](#cfn-s3-accesspoint-networkorigin): String
  [Policy](#cfn-s3-accesspoint-policy): Json
  [PolicyStatus](#cfn-s3-accesspoint-policystatus): Json
  [PublicAccessBlockConfiguration](#cfn-s3-accesspoint-publicaccessblockconfiguration): 
    PublicAccessBlockConfiguration
  [VpcConfiguration](#cfn-s3-accesspoint-vpcconfiguration): 
    VpcConfiguration
```

## Properties<a name="aws-resource-s3-accesspoint-properties"></a>

`Bucket`  <a name="cfn-s3-accesspoint-bucket"></a>
The name of the bucket associated with this access point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CreationDate`  <a name="cfn-s3-accesspoint-creationdate"></a>
The date and time when this access point was created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-s3-accesspoint-name"></a>
The name of this access point\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkOrigin`  <a name="cfn-s3-accesspoint-networkorigin"></a>
Indicates whether this access point allows access from the internet\. If `VpcConfiguration` is specified for this access point, then `NetworkOrigin` is `VPC`, and the access point doesn't allow access from the internet\. Otherwise, `NetworkOrigin` is `Internet`, and the access point allows access from the internet, subject to the access point and bucket access policies\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policy`  <a name="cfn-s3-accesspoint-policy"></a>
The access point policy associated with this access point\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyStatus`  <a name="cfn-s3-accesspoint-policystatus"></a>
The container element for a bucket's policy status\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicAccessBlockConfiguration`  <a name="cfn-s3-accesspoint-publicaccessblockconfiguration"></a>
The PublicAccessBlock configuration that you want to apply to this Amazon S3 bucket\. You can enable the configuration options in any combination\. For more information about when Amazon S3 considers a bucket or object public, see [The Meaning of "Public"](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-control-block-public-access.html#access-control-block-public-access-policy-status) in the *Amazon Simple Storage Service Developer Guide*\.   
*Required*: No  
*Type*: [PublicAccessBlockConfiguration](aws-properties-s3-accesspoint-publicaccessblockconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcConfiguration`  <a name="cfn-s3-accesspoint-vpcconfiguration"></a>
The Virtual Private Cloud \(VPC\) configuration for this access point, if one exists\.  
*Required*: No  
*Type*: [VpcConfiguration](aws-properties-s3-accesspoint-vpcconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-s3-accesspoint-return-values"></a>

### Ref<a name="aws-resource-s3-accesspoint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the access point name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.