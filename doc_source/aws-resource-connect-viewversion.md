# AWS::Connect::ViewVersion<a name="aws-resource-connect-viewversion"></a>

Creates a version for the specified customer\-managed view within the specified instance\.

## Syntax<a name="aws-resource-connect-viewversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-viewversion-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::ViewVersion",
  "Properties" : {
      "[VersionDescription](#cfn-connect-viewversion-versiondescription)" : String,
      "[ViewArn](#cfn-connect-viewversion-viewarn)" : String,
      "[ViewContentSha256](#cfn-connect-viewversion-viewcontentsha256)" : String
    }
}
```

### YAML<a name="aws-resource-connect-viewversion-syntax.yaml"></a>

```
Type: AWS::Connect::ViewVersion
Properties: 
  [VersionDescription](#cfn-connect-viewversion-versiondescription): String
  [ViewArn](#cfn-connect-viewversion-viewarn): String
  [ViewContentSha256](#cfn-connect-viewversion-viewcontentsha256): String
```

## Properties<a name="aws-resource-connect-viewversion-properties"></a>

`VersionDescription`  <a name="cfn-connect-viewversion-versiondescription"></a>
The description of the view version\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ViewArn`  <a name="cfn-connect-viewversion-viewarn"></a>
The unqualified Amazon Resource Name \(ARN\) of the view\.  
For example:  

```
arn:<partition>:connect:<region>:<accountId>:instance/00000000-0000-0000-0000-000000000000/view/00000000-0000-0000-0000-000000000000
```
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ViewContentSha256`  <a name="cfn-connect-viewversion-viewcontentsha256"></a>
Indicates the checksum value of the latest published view content\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-connect-viewversion-return-values"></a>

### Ref<a name="aws-resource-connect-viewversion-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-connect-viewversion-return-values-fn--getatt"></a>

#### <a name="aws-resource-connect-viewversion-return-values-fn--getatt-fn--getatt"></a>

`Version`  <a name="Version-fn::getatt"></a>
Current version of the view\.

`ViewVersionArn`  <a name="ViewVersionArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the view version\.