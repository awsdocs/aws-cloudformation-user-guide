# AWS::S3::AccessPoint<a name="aws-resource-s3-accesspoint"></a>

The AWS::S3::AccessPoint resource is an Amazon S3 resource type that you can use to access buckets\.

## Syntax<a name="aws-resource-s3-accesspoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3-accesspoint-syntax.json"></a>

```
{
  "Type" : "AWS::S3::AccessPoint",
  "Properties" : {
      "[AccountId](#cfn-s3-accesspoint-accountid)" : String,
      "[Bucket](#cfn-s3-accesspoint-bucket)" : String,
      "[Name](#cfn-s3-accesspoint-name)" : String,
      "[Policy](#cfn-s3-accesspoint-policy)" : String,
      "[PublicAccessBlockConfiguration](#cfn-s3-accesspoint-publicaccessblockconfiguration)" : [PublicAccessBlockConfiguration](aws-properties-s3-accesspoint-publicaccessblockconfiguration.md),
      "[VpcConfiguration](#cfn-s3-accesspoint-vpcconfiguration)" : [VpcConfiguration](aws-properties-s3-accesspoint-vpcconfiguration.md)
    }
}
```

### YAML<a name="aws-resource-s3-accesspoint-syntax.yaml"></a>

```
Type: AWS::S3::AccessPoint
Properties: 
  [AccountId](#cfn-s3-accesspoint-accountid): String
  [Bucket](#cfn-s3-accesspoint-bucket): String
  [Name](#cfn-s3-accesspoint-name): String
  [Policy](#cfn-s3-accesspoint-policy): String
  [PublicAccessBlockConfiguration](#cfn-s3-accesspoint-publicaccessblockconfiguration): 
    [PublicAccessBlockConfiguration](aws-properties-s3-accesspoint-publicaccessblockconfiguration.md)
  [VpcConfiguration](#cfn-s3-accesspoint-vpcconfiguration): 
    [VpcConfiguration](aws-properties-s3-accesspoint-vpcconfiguration.md)
```

## Properties<a name="aws-resource-s3-accesspoint-properties"></a>

`AccountId`  <a name="cfn-s3-accesspoint-accountid"></a>
The account ID for the owner of the bucket for which you want to create an access point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Bucket`  <a name="cfn-s3-accesspoint-bucket"></a>
The name of the bucket associated with this access point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-s3-accesspoint-name"></a>
The name of this access point\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policy`  <a name="cfn-s3-accesspoint-policy"></a>
The access point policy associated with this specified access point\.  
*Required*: No  
*Type*: String  
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

## Return Values<a name="aws-resource-s3-accesspoint-return-values"></a>

### Ref<a name="aws-resource-s3-accesspoint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the access point name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-s3-accesspoint-return-values-fn--getatt"></a>

#### <a name="aws-resource-s3-accesspoint-return-values-fn--getatt-fn--getatt"></a>

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
The creation date and time for the access point\.