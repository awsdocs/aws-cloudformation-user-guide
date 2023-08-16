# AWS::XRay::Group<a name="aws-resource-xray-group"></a>

Use the `AWS::XRay::Group` resource to specify a group with a name and a filter expression\. Groups enable the collection of traces that match the filter expression, can be used to filter service graphs and traces, and to supply Amazon CloudWatch metrics\.

## Syntax<a name="aws-resource-xray-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-xray-group-syntax.json"></a>

```
{
  "Type" : "AWS::XRay::Group",
  "Properties" : {
      "[FilterExpression](#cfn-xray-group-filterexpression)" : String,
      "[GroupName](#cfn-xray-group-groupname)" : String,
      "[InsightsConfiguration](#cfn-xray-group-insightsconfiguration)" : InsightsConfiguration,
      "[Tags](#cfn-xray-group-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-xray-group-syntax.yaml"></a>

```
Type: AWS::XRay::Group
Properties: 
  [FilterExpression](#cfn-xray-group-filterexpression): String
  [GroupName](#cfn-xray-group-groupname): String
  [InsightsConfiguration](#cfn-xray-group-insightsconfiguration): 
    InsightsConfiguration
  [Tags](#cfn-xray-group-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-xray-group-properties"></a>

`FilterExpression`  <a name="cfn-xray-group-filterexpression"></a>
The filter expression defining the parameters to include traces\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupName`  <a name="cfn-xray-group-groupname"></a>
The unique case\-sensitive name of the group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InsightsConfiguration`  <a name="cfn-xray-group-insightsconfiguration"></a>
The structure containing configurations related to insights\.  
+ The InsightsEnabled boolean can be set to true to enable insights for the group or false to disable insights for the group\.
+ The NotificationsEnabled boolean can be set to true to enable insights notifications through Amazon EventBridge for the group\.
*Required*: No  
*Type*: [InsightsConfiguration](aws-properties-xray-group-insightsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-xray-group-tags"></a>
An array of key\-value pairs to apply to this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-xray-group-return-values"></a>

### Ref<a name="aws-resource-xray-group-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the Amazon Resource Name \(ARN\) of the group\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-xray-group-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-xray-group-return-values-fn--getatt-fn--getatt"></a>

`GroupARN`  <a name="GroupARN-fn::getatt"></a>
The group ARN that was created or updated\.

## Examples<a name="aws-resource-xray-group--examples"></a>



### Create group<a name="aws-resource-xray-group--examples--Create_group"></a>

This example creates a new group called MyGroup\.

#### JSON<a name="aws-resource-xray-group--examples--Create_group--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Resources": {
      "MyGroupResource": {
         "Type": "AWS::XRay::Group",
         "Properties": {
            "GroupName": "MyGroup",
            "FilterExpression": "duration > 10",
            "InsightsConfiguration": {
               "InsightsEnabled": "false",
               "NotificationsEnabled": "false"
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-xray-group--examples--Create_group--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
   MyGroupResource:
      Type: AWS::XRay::Group
      Properties:
         GroupName: MyGroup
         FilterExpression: duration > 10
         InsightsConfiguration:
            InsightsEnabled: false
            NotificationsEnabled: false
```

## See also<a name="aws-resource-xray-group--seealso"></a>
+ [Configuring groups in the X\-Ray console](https://docs.aws.amazon.com/xray/latest/devguide/xray-console-groups.html)
+ [Configuring groups with the X\-Ray API](https://docs.aws.amazon.com/xray/latest/devguide/xray-api-configuration.html#xray-api-configuration-groups)
+ [CreateGroup](https://docs.aws.amazon.com/xray/latest/api/API_CreateGroup.html) action in the X\-Ray API Reference

