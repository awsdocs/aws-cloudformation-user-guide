# AWS::AppStream::AppBlock<a name="aws-resource-appstream-appblock"></a>

This resource creates an app block\. App blocks store details about the virtual hard disk that contains the files for the application in an S3 bucket\. It also stores the setup script with details about how to mount the virtual hard disk\. App blocks are only supported for Elastic fleets\.

## Syntax<a name="aws-resource-appstream-appblock-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-appblock-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::AppBlock",
  "Properties" : {
      "[Description](#cfn-appstream-appblock-description)" : String,
      "[DisplayName](#cfn-appstream-appblock-displayname)" : String,
      "[Name](#cfn-appstream-appblock-name)" : String,
      "[SetupScriptDetails](#cfn-appstream-appblock-setupscriptdetails)" : ScriptDetails,
      "[SourceS3Location](#cfn-appstream-appblock-sources3location)" : S3Location,
      "[Tags](#cfn-appstream-appblock-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-appstream-appblock-syntax.yaml"></a>

```
Type: AWS::AppStream::AppBlock
Properties: 
  [Description](#cfn-appstream-appblock-description): String
  [DisplayName](#cfn-appstream-appblock-displayname): String
  [Name](#cfn-appstream-appblock-name): String
  [SetupScriptDetails](#cfn-appstream-appblock-setupscriptdetails): 
    ScriptDetails
  [SourceS3Location](#cfn-appstream-appblock-sources3location): 
    S3Location
  [Tags](#cfn-appstream-appblock-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-appstream-appblock-properties"></a>

`Description`  <a name="cfn-appstream-appblock-description"></a>
The description of the app block\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DisplayName`  <a name="cfn-appstream-appblock-displayname"></a>
The display name of the app block\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-appstream-appblock-name"></a>
The name of the app block\.  
*Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9_.-]{0,100}$`  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SetupScriptDetails`  <a name="cfn-appstream-appblock-setupscriptdetails"></a>
The setup script details of the app block\.  
*Required*: Yes  
*Type*: [ScriptDetails](aws-properties-appstream-appblock-scriptdetails.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceS3Location`  <a name="cfn-appstream-appblock-sources3location"></a>
The source S3 location of the app block\.  
*Required*: Yes  
*Type*: [S3Location](aws-properties-appstream-appblock-s3location.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-appstream-appblock-tags"></a>
The tags of the app block\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appstream-appblock-return-values"></a>

### Ref<a name="aws-resource-appstream-appblock-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `Arn` of the app block, such as `arn:aws:appstream:us-west-2:123456789123:app-block/abcdefg`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appstream-appblock-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appstream-appblock-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the app block\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
The time when the app block was created\.