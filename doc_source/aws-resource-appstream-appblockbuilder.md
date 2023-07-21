# AWS::AppStream::AppBlockBuilder<a name="aws-resource-appstream-appblockbuilder"></a>

Creates an app block builder\.

## Syntax<a name="aws-resource-appstream-appblockbuilder-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-appblockbuilder-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::AppBlockBuilder",
  "Properties" : {
      "[AccessEndpoints](#cfn-appstream-appblockbuilder-accessendpoints)" : [ AccessEndpoint, ... ],
      "[AppBlockArns](#cfn-appstream-appblockbuilder-appblockarns)" : [ String, ... ],
      "[Description](#cfn-appstream-appblockbuilder-description)" : String,
      "[DisplayName](#cfn-appstream-appblockbuilder-displayname)" : String,
      "[EnableDefaultInternetAccess](#cfn-appstream-appblockbuilder-enabledefaultinternetaccess)" : Boolean,
      "[IamRoleArn](#cfn-appstream-appblockbuilder-iamrolearn)" : String,
      "[InstanceType](#cfn-appstream-appblockbuilder-instancetype)" : String,
      "[Name](#cfn-appstream-appblockbuilder-name)" : String,
      "[Platform](#cfn-appstream-appblockbuilder-platform)" : String,
      "[Tags](#cfn-appstream-appblockbuilder-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcConfig](#cfn-appstream-appblockbuilder-vpcconfig)" : VpcConfig
    }
}
```

### YAML<a name="aws-resource-appstream-appblockbuilder-syntax.yaml"></a>

```
Type: AWS::AppStream::AppBlockBuilder
Properties: 
  [AccessEndpoints](#cfn-appstream-appblockbuilder-accessendpoints): 
    - AccessEndpoint
  [AppBlockArns](#cfn-appstream-appblockbuilder-appblockarns): 
    - String
  [Description](#cfn-appstream-appblockbuilder-description): String
  [DisplayName](#cfn-appstream-appblockbuilder-displayname): String
  [EnableDefaultInternetAccess](#cfn-appstream-appblockbuilder-enabledefaultinternetaccess): Boolean
  [IamRoleArn](#cfn-appstream-appblockbuilder-iamrolearn): String
  [InstanceType](#cfn-appstream-appblockbuilder-instancetype): String
  [Name](#cfn-appstream-appblockbuilder-name): String
  [Platform](#cfn-appstream-appblockbuilder-platform): String
  [Tags](#cfn-appstream-appblockbuilder-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcConfig](#cfn-appstream-appblockbuilder-vpcconfig): 
    VpcConfig
```

## Properties<a name="aws-resource-appstream-appblockbuilder-properties"></a>

`AccessEndpoints`  <a name="cfn-appstream-appblockbuilder-accessendpoints"></a>
The access endpoints of the app block builder\.  
*Required*: No  
*Type*: List of [AccessEndpoint](aws-properties-appstream-appblockbuilder-accessendpoint.md)  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AppBlockArns`  <a name="cfn-appstream-appblockbuilder-appblockarns"></a>
The ARN of the app block\.  
*Maximum*: `1`  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-appstream-appblockbuilder-description"></a>
The description of the app block builder\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-appstream-appblockbuilder-displayname"></a>
The display name of the app block builder\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableDefaultInternetAccess`  <a name="cfn-appstream-appblockbuilder-enabledefaultinternetaccess"></a>
Indicates whether default internet access is enabled for the app block builder\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamRoleArn`  <a name="cfn-appstream-appblockbuilder-iamrolearn"></a>
The ARN of the IAM role that is applied to the app block builder\.  
*Required*: No  
*Type*: String  
*Pattern*: `^arn:aws(?:\-cn|\-iso\-b|\-iso|\-us\-gov)?:[A-Za-z0-9][A-Za-z0-9_/.-]{0,62}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9][A-Za-z0-9:_/+=,@.\\-]{0,1023}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-appstream-appblockbuilder-instancetype"></a>
The instance type of the app block builder\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appstream-appblockbuilder-name"></a>
The name of the app block builder\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Platform`  <a name="cfn-appstream-appblockbuilder-platform"></a>
The platform of the app block builder\.  
*Allowed values*: `WINDOWS_SERVER_2019`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appstream-appblockbuilder-tags"></a>
The tags of the app block builder\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfig`  <a name="cfn-appstream-appblockbuilder-vpcconfig"></a>
The VPC configuration for the app block builder\.  
*Required*: Yes  
*Type*: [VpcConfig](aws-properties-appstream-appblockbuilder-vpcconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appstream-appblockbuilder-return-values"></a>

### Ref<a name="aws-resource-appstream-appblockbuilder-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `Name` of the app block builder, such as `abcdefAppBlockBuilder`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appstream-appblockbuilder-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appstream-appblockbuilder-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the app block builder\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
The time when the app block builder was created\.