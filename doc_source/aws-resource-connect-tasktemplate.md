# AWS::Connect::TaskTemplate<a name="aws-resource-connect-tasktemplate"></a>

Specifies a task template for a Amazon Connect instance\.

## Syntax<a name="aws-resource-connect-tasktemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-tasktemplate-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::TaskTemplate",
  "Properties" : {
      "[ClientToken](#cfn-connect-tasktemplate-clienttoken)" : String,
      "[Constraints](#cfn-connect-tasktemplate-constraints)" : Constraints,
      "[ContactFlowArn](#cfn-connect-tasktemplate-contactflowarn)" : String,
      "[Defaults](#cfn-connect-tasktemplate-defaults)" : [ DefaultFieldValue, ... ],
      "[Description](#cfn-connect-tasktemplate-description)" : String,
      "[Fields](#cfn-connect-tasktemplate-fields)" : [ Field, ... ],
      "[InstanceArn](#cfn-connect-tasktemplate-instancearn)" : String,
      "[Name](#cfn-connect-tasktemplate-name)" : String,
      "[Status](#cfn-connect-tasktemplate-status)" : String,
      "[Tags](#cfn-connect-tasktemplate-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-connect-tasktemplate-syntax.yaml"></a>

```
Type: AWS::Connect::TaskTemplate
Properties: 
  [ClientToken](#cfn-connect-tasktemplate-clienttoken): String
  [Constraints](#cfn-connect-tasktemplate-constraints): 
    Constraints
  [ContactFlowArn](#cfn-connect-tasktemplate-contactflowarn): String
  [Defaults](#cfn-connect-tasktemplate-defaults): 
    - DefaultFieldValue
  [Description](#cfn-connect-tasktemplate-description): String
  [Fields](#cfn-connect-tasktemplate-fields): 
    - Field
  [InstanceArn](#cfn-connect-tasktemplate-instancearn): String
  [Name](#cfn-connect-tasktemplate-name): String
  [Status](#cfn-connect-tasktemplate-status): String
  [Tags](#cfn-connect-tasktemplate-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-connect-tasktemplate-properties"></a>

`ClientToken`  <a name="cfn-connect-tasktemplate-clienttoken"></a>
A unique, case\-sensitive identifier that you provide to ensure the idempotency of the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Constraints`  <a name="cfn-connect-tasktemplate-constraints"></a>
Constraints that are applicable to the fields listed\.  
The values can be represented in either JSON or YAML format\. For an example of the JSON configuration, see *Examples* at the bottom of this page\.  
*Required*: No  
*Type*: [Constraints](aws-properties-connect-tasktemplate-constraints.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContactFlowArn`  <a name="cfn-connect-tasktemplate-contactflowarn"></a>
The Amazon Resource Name \(ARN\) of the flow that runs by default when a task is created by referencing this template\. `ContactFlowArn` is not required when there is a field with `fieldType` = `QUICK_CONNECT`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Defaults`  <a name="cfn-connect-tasktemplate-defaults"></a>
The default values for fields when a task is created by referencing this template\.  
*Required*: No  
*Type*: List of [DefaultFieldValue](aws-properties-connect-tasktemplate-defaultfieldvalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-connect-tasktemplate-description"></a>
The description of the task template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Fields`  <a name="cfn-connect-tasktemplate-fields"></a>
Fields that are part of the template\. A template requires at least one field that has type `Name`\.  
*Required*: No  
*Type*: List of [Field](aws-properties-connect-tasktemplate-field.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-connect-tasktemplate-instancearn"></a>
The Amazon Resource Name \(ARN\) of the Amazon Connect instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-connect-tasktemplate-name"></a>
The name of the task template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-connect-tasktemplate-status"></a>
The status of the task template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connect-tasktemplate-tags"></a>
The tags used to organize, track, or control access for this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-connect-tasktemplate-return-values"></a>

### Ref<a name="aws-resource-connect-tasktemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the task template\. For example:

`{ "Ref": "myTaskTemplate" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connect-tasktemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connect-tasktemplate-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the task template\.

## Examples<a name="aws-resource-connect-tasktemplate--examples"></a>

### JSON format for Constraints<a name="aws-resource-connect-tasktemplate--examples--JSON_format_for_Constraints"></a>

Following is an example of the JSON format for the `Constraints` property\.

#### JSON<a name="aws-resource-connect-tasktemplate--examples--JSON_format_for_Constraints--json"></a>

```
{
  "Type" : "AWS::Connect::TaskTemplate",
  "Properties" : {
      "ClientToken" : String,
      "Constraints" : Constraints,
      "ContactFlowArn" : String,
      "Defaults" : [ DefaultFieldValue, ... ],
      "Description" : String,
      "Fields" : [ Field, ... ],
      "InstanceArn" : String,
      "Name" : String,
      "Status" : String,
      "Tags" : [ Tag, ... ]
    }
}
```