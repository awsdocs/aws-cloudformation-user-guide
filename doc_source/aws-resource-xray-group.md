# AWS::XRay::Group<a name="aws-resource-xray-group"></a>

Use the `AWS::XRay::Group` resource to specify a group with a name and a filter expression\. 

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
      "[Tags](#cfn-xray-group-tags)" : [ TagsItems, ... ]
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
    - TagsItems
```

## Properties<a name="aws-resource-xray-group-properties"></a>

`FilterExpression`  <a name="cfn-xray-group-filterexpression"></a>
The filter expression defining the parameters to include traces\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupName`  <a name="cfn-xray-group-groupname"></a>
The unique case\-sensitive name of the group\.  
*Required*: No  
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
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [TagsItems](aws-properties-xray-group-tagsitems.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-xray-group-return-values"></a>

### Fn::GetAtt<a name="aws-resource-xray-group-return-values-fn--getatt"></a>

#### <a name="aws-resource-xray-group-return-values-fn--getatt-fn--getatt"></a>

`GroupARN`  <a name="GroupARN-fn::getatt"></a>
The group ARN that was created or updated\.

## Examples<a name="aws-resource-xray-group--examples"></a>



### Create group<a name="aws-resource-xray-group--examples--Create_group"></a>

This example creates a new group called MyGroup

#### JSON<a name="aws-resource-xray-group--examples--Create_group--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09",
   "Description": "XRay stack",
   "Resources": {
      "TestGrpResource": {
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
   Group:
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

