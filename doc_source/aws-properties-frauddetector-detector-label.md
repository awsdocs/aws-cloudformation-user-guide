# AWS::FraudDetector::Detector Label<a name="aws-properties-frauddetector-detector-label"></a>

The label details\.

## Syntax<a name="aws-properties-frauddetector-detector-label-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-frauddetector-detector-label-syntax.json"></a>

```
{
  "[Arn](#cfn-frauddetector-detector-label-arn)" : String,
  "[CreatedTime](#cfn-frauddetector-detector-label-createdtime)" : String,
  "[Description](#cfn-frauddetector-detector-label-description)" : String,
  "[Inline](#cfn-frauddetector-detector-label-inline)" : Boolean,
  "[LastUpdatedTime](#cfn-frauddetector-detector-label-lastupdatedtime)" : String,
  "[Name](#cfn-frauddetector-detector-label-name)" : String,
  "[Tags](#cfn-frauddetector-detector-label-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
}
```

### YAML<a name="aws-properties-frauddetector-detector-label-syntax.yaml"></a>

```
  [Arn](#cfn-frauddetector-detector-label-arn): String
  [CreatedTime](#cfn-frauddetector-detector-label-createdtime): String
  [Description](#cfn-frauddetector-detector-label-description): String
  [Inline](#cfn-frauddetector-detector-label-inline): Boolean
  [LastUpdatedTime](#cfn-frauddetector-detector-label-lastupdatedtime): String
  [Name](#cfn-frauddetector-detector-label-name): String
  [Tags](#cfn-frauddetector-detector-label-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-frauddetector-detector-label-properties"></a>

`Arn`  <a name="cfn-frauddetector-detector-label-arn"></a>
The label ARN\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^arn\:aws[a-z-]{0,15}\:frauddetector\:[a-z0-9-]{3,20}\:[0-9]{12}\:[^\s]{2,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreatedTime`  <a name="cfn-frauddetector-detector-label-createdtime"></a>
Timestamp of when the event type was created\.  
*Required*: No  
*Type*: String  
*Minimum*: `11`  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-frauddetector-detector-label-description"></a>
The label description\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Inline`  <a name="cfn-frauddetector-detector-label-inline"></a>
Indicates whether the resource is defined within this CloudFormation template and impacts the create, update, and delete behavior of the stack\. If the value is `true`, CloudFormation will create/update/delete the resource when creating/updating/deleting the stack\. If the value is `false`, CloudFormation will validate that the object exists and then use it within the resource without making changes to the object\.   
For example, when creating `AWS::FraudDetector::Detector` you must define at least two variables\. You can set `Inline=true` for these variables and CloudFormation will create/update/delete the variables as part of stack operations\. However, if you set `Inline=false`, CloudFormation will associate the variables to your detector but not execute any changes to the variables\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastUpdatedTime`  <a name="cfn-frauddetector-detector-label-lastupdatedtime"></a>
Timestamp of when the label was last updated\.  
*Required*: No  
*Type*: String  
*Minimum*: `11`  
*Maximum*: `30`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-frauddetector-detector-label-name"></a>
The label name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-frauddetector-detector-label-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)