# AWS::CloudFormation::PublicTypeVersion<a name="aws-resource-cloudformation-publictypeversion"></a>

Tests and publishes a registered extension as a public, third\-party extension\.

CloudFormation first tests the extension to make sure it meets all necessary requirements for being published in the CloudFormation registry\. If it does, CloudFormation then publishes it to the registry as a public third\-party extension in this Region\. Public extensions are available for use by all CloudFormation users\.
+ For resource types, testing includes passing all contracts tests defined for the type\.
+ For modules, testing includes determining if the module's model meets all necessary requirements\.

For more information, see [Testing your public extension prior to publishing](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/publish-extension.html#publish-extension-testing) in the *CloudFormation CLI User Guide*\.

If you don't specify a version, CloudFormation uses the default version of the extension in your account and Region for testing\.

To perform testing, CloudFormation assumes the execution role specified when the type was registered\.

An extension must have a test status of `PASSED` before it can be published\. For more information, see [Publishing extensions to make them available for public use](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/resource-type-publish.html) in the *CloudFormation CLI User Guide*\.

## Syntax<a name="aws-resource-cloudformation-publictypeversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-publictypeversion-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::PublicTypeVersion",
  "Properties" : {
      "[Arn](#cfn-cloudformation-publictypeversion-arn)" : String,
      "[LogDeliveryBucket](#cfn-cloudformation-publictypeversion-logdeliverybucket)" : String,
      "[PublicVersionNumber](#cfn-cloudformation-publictypeversion-publicversionnumber)" : String,
      "[Type](#cfn-cloudformation-publictypeversion-type)" : String,
      "[TypeName](#cfn-cloudformation-publictypeversion-typename)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-publictypeversion-syntax.yaml"></a>

```
Type: AWS::CloudFormation::PublicTypeVersion
Properties: 
  [Arn](#cfn-cloudformation-publictypeversion-arn): String
  [LogDeliveryBucket](#cfn-cloudformation-publictypeversion-logdeliverybucket): String
  [PublicVersionNumber](#cfn-cloudformation-publictypeversion-publicversionnumber): String
  [Type](#cfn-cloudformation-publictypeversion-type): String
  [TypeName](#cfn-cloudformation-publictypeversion-typename): String
```

## Properties<a name="aws-resource-cloudformation-publictypeversion-properties"></a>

`Arn`  <a name="cfn-cloudformation-publictypeversion-arn"></a>
The Amazon Resource Number \(ARN\) of the extension\.  
Conditional: You must specify `Arn`, or `TypeName` and `Type`\.  
*Required*: Conditional  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `arn:aws[A-Za-z0-9-]{0,64}:cloudformation:[A-Za-z0-9-]{1,64}:([0-9]{12})?:type/.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogDeliveryBucket`  <a name="cfn-cloudformation-publictypeversion-logdeliverybucket"></a>
The S3 bucket to which CloudFormation delivers the contract test execution logs\.  
CloudFormation delivers the logs by the time contract testing has completed and the extension has been assigned a test type status of `PASSED` or `FAILED`\.  
The user initiating the stack operation must be able to access items in the specified S3 bucket\. Specifically, the user needs the following permissions:  
+ GetObject
+ PutObject
For more information, see [Actions, Resources, and Condition Keys for Amazon S3](https://docs.aws.amazon.com/service-authorization/latest/reference/list_amazons3.html) in the *AWS Identity and Access Management User Guide*\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `63`  
*Pattern*: `[\s\S]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PublicVersionNumber`  <a name="cfn-cloudformation-publictypeversion-publicversionnumber"></a>
The version number to assign to this version of the extension\.  
Use the following format, and adhere to semantic versioning when assigning a version number to your extension:  
 `MAJOR.MINOR.PATCH`   
For more information, see [Semantic Versioning 2\.0\.0](https://semver.org/)\.  
If you don't specify a version number, CloudFormation increments the version number by one minor version release\.  
You cannot specify a version number the first time you publish a type\. AWS CloudFormation automatically sets the first version number to be `1.0.0`\.  
*Required*: No  
*Type*: String  
*Minimum*: `5`  
*Pattern*: `^(0|[1-9]\d*)\.(0|[1-9]\d*)\.(.*)$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-cloudformation-publictypeversion-type"></a>
The type of the extension to test\.  
Conditional: You must specify `Arn`, or `TypeName` and `Type`\.  
*Required*: Conditional  
*Type*: String  
*Allowed values*: `HOOK | MODULE | RESOURCE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TypeName`  <a name="cfn-cloudformation-publictypeversion-typename"></a>
The name of the extension to test\.  
Conditional: You must specify `Arn`, or `TypeName` and `Type`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `204`  
*Pattern*: `[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}(::MODULE){0,1}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cloudformation-publictypeversion-return-values"></a>

### Ref<a name="aws-resource-cloudformation-publictypeversion-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Number \(ARN\) assigned to the public extension upon publication\. For example: 

 `{ "Ref": "arn:aws:cloudformation:us-east-1::type/resource/2a33349e7e606a8ad2e30e3c84521f93123456/My-Extension/2.1.3" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudformation-publictypeversion-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudformation-publictypeversion-return-values-fn--getatt-fn--getatt"></a>

`PublicTypeArn`  <a name="PublicTypeArn-fn::getatt"></a>
The Amazon Resource Number \(ARN\) assigned to the public extension upon publication\.

`PublisherId`  <a name="PublisherId-fn::getatt"></a>
The publisher ID of the extension publisher\.

`TypeVersionArn`  <a name="TypeVersionArn-fn::getatt"></a>
The Amazon Resource Number \(ARN\) assigned to this version of the extension\.