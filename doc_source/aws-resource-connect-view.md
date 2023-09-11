# AWS::Connect::View<a name="aws-resource-connect-view"></a>

Creates a customer\-managed view in the published state within the specified instance\.

## Syntax<a name="aws-resource-connect-view-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-view-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::View",
  "Properties" : {
      "[Actions](#cfn-connect-view-actions)" : [ String, ... ],
      "[Description](#cfn-connect-view-description)" : String,
      "[InstanceArn](#cfn-connect-view-instancearn)" : String,
      "[Name](#cfn-connect-view-name)" : String,
      "[Tags](#cfn-connect-view-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Template](#cfn-connect-view-template)" : Json
    }
}
```

### YAML<a name="aws-resource-connect-view-syntax.yaml"></a>

```
Type: AWS::Connect::View
Properties: 
  [Actions](#cfn-connect-view-actions): 
    - String
  [Description](#cfn-connect-view-description): String
  [InstanceArn](#cfn-connect-view-instancearn): String
  [Name](#cfn-connect-view-name): String
  [Tags](#cfn-connect-view-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Template](#cfn-connect-view-template): Json
```

## Properties<a name="aws-resource-connect-view-properties"></a>

`Actions`  <a name="cfn-connect-view-actions"></a>
A list of actions possible from the view\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-connect-view-description"></a>
The description of the view\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-connect-view-instancearn"></a>
The Amazon Resource Name \(ARN\) of the instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-connect-view-name"></a>
The name of the view\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connect-view-tags"></a>
The tags associated with the view resource \(not specific to view version\)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Template`  <a name="cfn-connect-view-template"></a>
The view template representing the structure of the view\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-connect-view-return-values"></a>

### Ref<a name="aws-resource-connect-view-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-connect-view-return-values-fn--getatt"></a>

#### <a name="aws-resource-connect-view-return-values-fn--getatt-fn--getatt"></a>

`ViewArn`  <a name="ViewArn-fn::getatt"></a>
The unqualified Amazon Resource Name \(ARN\) of the view\.  
For example:  

```
arn:<partition>:connect:<region>:<accountId>:instance/00000000-0000-0000-0000-000000000000/view/00000000-0000-0000-0000-000000000000
```

`ViewContentSha256`  <a name="ViewContentSha256-fn::getatt"></a>
Indicates the checksum value of the latest published view content\.

`ViewId`  <a name="ViewId-fn::getatt"></a>
The identifier of the view\.