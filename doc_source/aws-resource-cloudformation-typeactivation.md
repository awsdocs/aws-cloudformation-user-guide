# AWS::CloudFormation::TypeActivation<a name="aws-resource-cloudformation-typeactivation"></a>

Activates a public third\-party extension, making it available for use in stack templates\. For more information, see [Using public extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-public.html) in the * AWS CloudFormation User Guide*\.

Once you have activated a public third\-party extension in your account and region, use [SetTypeConfiguration](AWSCloudFormation/latest/APIReference/API_SetTypeConfiguration.html) to specify configuration properties for the extension\. For more information, see [Configuring extensions at the account level](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-register.html#registry-set-configuration) in the *CloudFormation User Guide*\.

## Syntax<a name="aws-resource-cloudformation-typeactivation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-typeactivation-syntax.json"></a>

```
{
  "Type" : "AWS::CloudFormation::TypeActivation",
  "Properties" : {
      "[AutoUpdate](#cfn-cloudformation-typeactivation-autoupdate)" : Boolean,
      "[ExecutionRoleArn](#cfn-cloudformation-typeactivation-executionrolearn)" : String,
      "[LoggingConfig](#cfn-cloudformation-typeactivation-loggingconfig)" : LoggingConfig,
      "[MajorVersion](#cfn-cloudformation-typeactivation-majorversion)" : String,
      "[PublicTypeArn](#cfn-cloudformation-typeactivation-publictypearn)" : String,
      "[PublisherId](#cfn-cloudformation-typeactivation-publisherid)" : String,
      "[Type](#cfn-cloudformation-typeactivation-type)" : String,
      "[TypeName](#cfn-cloudformation-typeactivation-typename)" : String,
      "[TypeNameAlias](#cfn-cloudformation-typeactivation-typenamealias)" : String,
      "[VersionBump](#cfn-cloudformation-typeactivation-versionbump)" : String
    }
}
```

### YAML<a name="aws-resource-cloudformation-typeactivation-syntax.yaml"></a>

```
Type: AWS::CloudFormation::TypeActivation
Properties: 
  [AutoUpdate](#cfn-cloudformation-typeactivation-autoupdate): Boolean
  [ExecutionRoleArn](#cfn-cloudformation-typeactivation-executionrolearn): String
  [LoggingConfig](#cfn-cloudformation-typeactivation-loggingconfig): 
    LoggingConfig
  [MajorVersion](#cfn-cloudformation-typeactivation-majorversion): String
  [PublicTypeArn](#cfn-cloudformation-typeactivation-publictypearn): String
  [PublisherId](#cfn-cloudformation-typeactivation-publisherid): String
  [Type](#cfn-cloudformation-typeactivation-type): String
  [TypeName](#cfn-cloudformation-typeactivation-typename): String
  [TypeNameAlias](#cfn-cloudformation-typeactivation-typenamealias): String
  [VersionBump](#cfn-cloudformation-typeactivation-versionbump): String
```

## Properties<a name="aws-resource-cloudformation-typeactivation-properties"></a>

`AutoUpdate`  <a name="cfn-cloudformation-typeactivation-autoupdate"></a>
Whether to automatically update the extension in this account and region when a new *minor* version is published by the extension publisher\. Major versions released by the publisher must be manually updated\.  
The default is `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionRoleArn`  <a name="cfn-cloudformation-typeactivation-executionrolearn"></a>
The name of the IAM execution role to use to activate the extension\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `arn:.+:iam::[0-9]{12}:role/.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingConfig`  <a name="cfn-cloudformation-typeactivation-loggingconfig"></a>
Specifies logging configuration information for an extension\.  
*Required*: No  
*Type*: [LoggingConfig](aws-properties-cloudformation-typeactivation-loggingconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MajorVersion`  <a name="cfn-cloudformation-typeactivation-majorversion"></a>
The major version of this extension you want to activate, if multiple major versions are available\. The default is the latest major version\. CloudFormation uses the latest available *minor* version of the major version selected\.  
You can specify `MajorVersion` or `VersionBump`, but not both\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PublicTypeArn`  <a name="cfn-cloudformation-typeactivation-publictypearn"></a>
The Amazon Resource Number \(ARN\) of the public extension\.  
Conditional: You must specify `PublicTypeArn`, or `TypeName`, `Type`, and `PublisherId`\.  
*Required*: Conditional  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `arn:aws[A-Za-z0-9-]{0,64}:cloudformation:[A-Za-z0-9-]{1,64}::type/.+/[0-9a-zA-Z]{12,40}/.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PublisherId`  <a name="cfn-cloudformation-typeactivation-publisherid"></a>
The ID of the extension publisher\.  
Conditional: You must specify `PublicTypeArn`, or `TypeName`, `Type`, and `PublisherId`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `40`  
*Pattern*: `[0-9a-zA-Z]{12,40}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-cloudformation-typeactivation-type"></a>
The extension type\.  
Conditional: You must specify `PublicTypeArn`, or `TypeName`, `Type`, and `PublisherId`\.  
*Required*: Conditional  
*Type*: String  
*Allowed values*: `HOOK | MODULE | RESOURCE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TypeName`  <a name="cfn-cloudformation-typeactivation-typename"></a>
The name of the extension\.  
Conditional: You must specify `PublicTypeArn`, or `TypeName`, `Type`, and `PublisherId`\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `204`  
*Pattern*: `[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}(::MODULE){0,1}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TypeNameAlias`  <a name="cfn-cloudformation-typeactivation-typenamealias"></a>
An alias to assign to the public extension, in this account and region\. If you specify an alias for the extension, CloudFormation treats the alias as the extension type name within this account and region\. You must use the alias to refer to the extension in your templates, API calls, and CloudFormation console\.  
An extension alias must be unique within a given account and region\. You can activate the same public resource multiple times in the same account and region, using different type name aliases\.  
*Required*: No  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `204`  
*Pattern*: `[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}::[A-Za-z0-9]{2,64}(::MODULE){0,1}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VersionBump`  <a name="cfn-cloudformation-typeactivation-versionbump"></a>
Manually updates a previously\-activated type to a new major or minor version, if available\. You can also use this parameter to update the value of `AutoUpdate`\.  
+  `MAJOR`: CloudFormation updates the extension to the newest major version, if one is available\.
+  `MINOR`: CloudFormation updates the extension to the newest minor version, if one is available\.
*Required*: No  
*Type*: String  
*Allowed values*: `MAJOR | MINOR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudformation-typeactivation-return-values"></a>

### Ref<a name="aws-resource-cloudformation-typeactivation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Number \(ARN\) of the activated extension, in this account and Region\.

 `{ "Ref": "arn:aws:cloudformation:us-east-1:123456789013:type/resource/My-Example" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloudformation-typeactivation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudformation-typeactivation-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Number \(ARN\) of the activated extension, in this account and Region\.