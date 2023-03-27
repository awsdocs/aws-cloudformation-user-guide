# AWS::S3ObjectLambda::AccessPoint<a name="aws-resource-s3objectlambda-accesspoint"></a>

The `AWS::S3ObjectLambda::AccessPoint` resource specifies an Object Lambda Access Point used to access a bucket\.

## Syntax<a name="aws-resource-s3objectlambda-accesspoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-s3objectlambda-accesspoint-syntax.json"></a>

```
{
  "Type" : "AWS::S3ObjectLambda::AccessPoint",
  "Properties" : {
      "[Name](#cfn-s3objectlambda-accesspoint-name)" : String,
      "[ObjectLambdaConfiguration](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration)" : ObjectLambdaConfiguration
    }
}
```

### YAML<a name="aws-resource-s3objectlambda-accesspoint-syntax.yaml"></a>

```
Type: AWS::S3ObjectLambda::AccessPoint
Properties: 
  [Name](#cfn-s3objectlambda-accesspoint-name): String
  [ObjectLambdaConfiguration](#cfn-s3objectlambda-accesspoint-objectlambdaconfiguration): 
    ObjectLambdaConfiguration
```

## Properties<a name="aws-resource-s3objectlambda-accesspoint-properties"></a>

`Name`  <a name="cfn-s3objectlambda-accesspoint-name"></a>
The name of this access point\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ObjectLambdaConfiguration`  <a name="cfn-s3objectlambda-accesspoint-objectlambdaconfiguration"></a>
A configuration used when creating an Object Lambda Access Point\.  
*Required*: Yes  
*Type*: [ObjectLambdaConfiguration](aws-properties-s3objectlambda-accesspoint-objectlambdaconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-s3objectlambda-accesspoint-return-values"></a>

### Ref<a name="aws-resource-s3objectlambda-accesspoint-return-values-ref"></a>

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-s3objectlambda-accesspoint-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-s3objectlambda-accesspoint-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Specifies the ARN for the Object Lambda Access Point\.

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
The date and time when the specified Object Lambda Access Point was created\.

`PolicyStatus`  <a name="PolicyStatus-fn::getatt"></a>
Property description not available\.

`PolicyStatus.IsPublic`  <a name="PolicyStatus.IsPublic-fn::getatt"></a>
Property description not available\.

`PublicAccessBlockConfiguration`  <a name="PublicAccessBlockConfiguration-fn::getatt"></a>
Property description not available\.

`PublicAccessBlockConfiguration.BlockPublicAcls`  <a name="PublicAccessBlockConfiguration.BlockPublicAcls-fn::getatt"></a>
Property description not available\.

`PublicAccessBlockConfiguration.BlockPublicPolicy`  <a name="PublicAccessBlockConfiguration.BlockPublicPolicy-fn::getatt"></a>
Property description not available\.

`PublicAccessBlockConfiguration.IgnorePublicAcls`  <a name="PublicAccessBlockConfiguration.IgnorePublicAcls-fn::getatt"></a>
Property description not available\.

`PublicAccessBlockConfiguration.RestrictPublicBuckets`  <a name="PublicAccessBlockConfiguration.RestrictPublicBuckets-fn::getatt"></a>
Property description not available\.