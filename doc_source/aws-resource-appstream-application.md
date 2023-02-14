# AWS::AppStream::Application<a name="aws-resource-appstream-application"></a>

This resource creates an application\. Applications store the details about how to launch applications on streaming instances\. This is only supported for Elastic fleets\.

## Syntax<a name="aws-resource-appstream-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-application-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::Application",
  "Properties" : {
      "[AppBlockArn](#cfn-appstream-application-appblockarn)" : String,
      "[AttributesToDelete](#cfn-appstream-application-attributestodelete)" : [ String, ... ],
      "[Description](#cfn-appstream-application-description)" : String,
      "[DisplayName](#cfn-appstream-application-displayname)" : String,
      "[IconS3Location](#cfn-appstream-application-icons3location)" : S3Location,
      "[InstanceFamilies](#cfn-appstream-application-instancefamilies)" : [ String, ... ],
      "[LaunchParameters](#cfn-appstream-application-launchparameters)" : String,
      "[LaunchPath](#cfn-appstream-application-launchpath)" : String,
      "[Name](#cfn-appstream-application-name)" : String,
      "[Platforms](#cfn-appstream-application-platforms)" : [ String, ... ],
      "[Tags](#cfn-appstream-application-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[WorkingDirectory](#cfn-appstream-application-workingdirectory)" : String
    }
}
```

### YAML<a name="aws-resource-appstream-application-syntax.yaml"></a>

```
Type: AWS::AppStream::Application
Properties: 
  [AppBlockArn](#cfn-appstream-application-appblockarn): String
  [AttributesToDelete](#cfn-appstream-application-attributestodelete): 
    - String
  [Description](#cfn-appstream-application-description): String
  [DisplayName](#cfn-appstream-application-displayname): String
  [IconS3Location](#cfn-appstream-application-icons3location): 
    S3Location
  [InstanceFamilies](#cfn-appstream-application-instancefamilies): 
    - String
  [LaunchParameters](#cfn-appstream-application-launchparameters): String
  [LaunchPath](#cfn-appstream-application-launchpath): String
  [Name](#cfn-appstream-application-name): String
  [Platforms](#cfn-appstream-application-platforms): 
    - String
  [Tags](#cfn-appstream-application-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [WorkingDirectory](#cfn-appstream-application-workingdirectory): String
```

## Properties<a name="aws-resource-appstream-application-properties"></a>

`AppBlockArn`  <a name="cfn-appstream-application-appblockarn"></a>
The app block ARN with which the application should be associated\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^arn:aws(?:\-cn|\-iso\-b|\-iso|\-us\-gov)?:[A-Za-z0-9][A-Za-z0-9_/.-]{0,62}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9][A-Za-z0-9:_/+=,@.\\-]{0,1023}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AttributesToDelete`  <a name="cfn-appstream-application-attributestodelete"></a>
A list of attributes to delete from an application\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-appstream-application-description"></a>
The description of the application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-appstream-application-displayname"></a>
The display name of the application\. This name is visible to users in the application catalog\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IconS3Location`  <a name="cfn-appstream-application-icons3location"></a>
The icon S3 location of the application\.  
*Required*: Yes  
*Type*: [S3Location](aws-properties-appstream-application-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceFamilies`  <a name="cfn-appstream-application-instancefamilies"></a>
The instance families the application supports\.  
*Allowed Values*: `GENERAL_PURPOSE` \| `GRAPHICS_G4`  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LaunchParameters`  <a name="cfn-appstream-application-launchparameters"></a>
The launch parameters of the application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchPath`  <a name="cfn-appstream-application-launchpath"></a>
The launch path of the application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appstream-application-name"></a>
The name of the application\. This name is visible to users when a name is not specified in the DisplayName property\.  
*Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9_.-]{0,100}$`  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Platforms`  <a name="cfn-appstream-application-platforms"></a>
The platforms the application supports\.  
*Allowed Values*: `WINDOWS_SERVER_2019` \| `AMAZON_LINUX2`  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `4`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-appstream-application-tags"></a>
The tags of the application\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkingDirectory`  <a name="cfn-appstream-application-workingdirectory"></a>
The working directory of the application\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appstream-application-return-values"></a>

### Ref<a name="aws-resource-appstream-application-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `Arn` of the application, such as `arn:aws:appstream:us-west-2:123456789123:application/abcdefg`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appstream-application-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appstream-application-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the application\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
The time when the application was created\.