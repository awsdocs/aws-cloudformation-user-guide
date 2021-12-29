# AWS::FraudDetector::Detector EventVariable<a name="aws-properties-frauddetector-detector-eventvariable"></a>

The event type variable for the detector\.

## Syntax<a name="aws-properties-frauddetector-detector-eventvariable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-frauddetector-detector-eventvariable-syntax.json"></a>

```
{
  "[Arn](#cfn-frauddetector-detector-eventvariable-arn)" : String,
  "[CreatedTime](#cfn-frauddetector-detector-eventvariable-createdtime)" : String,
  "[DataSource](#cfn-frauddetector-detector-eventvariable-datasource)" : String,
  "[DataType](#cfn-frauddetector-detector-eventvariable-datatype)" : String,
  "[DefaultValue](#cfn-frauddetector-detector-eventvariable-defaultvalue)" : String,
  "[Description](#cfn-frauddetector-detector-eventvariable-description)" : String,
  "[Inline](#cfn-frauddetector-detector-eventvariable-inline)" : Boolean,
  "[LastUpdatedTime](#cfn-frauddetector-detector-eventvariable-lastupdatedtime)" : String,
  "[Name](#cfn-frauddetector-detector-eventvariable-name)" : String,
  "[Tags](#cfn-frauddetector-detector-eventvariable-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
  "[VariableType](#cfn-frauddetector-detector-eventvariable-variabletype)" : String
}
```

### YAML<a name="aws-properties-frauddetector-detector-eventvariable-syntax.yaml"></a>

```
  [Arn](#cfn-frauddetector-detector-eventvariable-arn): String
  [CreatedTime](#cfn-frauddetector-detector-eventvariable-createdtime): String
  [DataSource](#cfn-frauddetector-detector-eventvariable-datasource): String
  [DataType](#cfn-frauddetector-detector-eventvariable-datatype): String
  [DefaultValue](#cfn-frauddetector-detector-eventvariable-defaultvalue): String
  [Description](#cfn-frauddetector-detector-eventvariable-description): String
  [Inline](#cfn-frauddetector-detector-eventvariable-inline): Boolean
  [LastUpdatedTime](#cfn-frauddetector-detector-eventvariable-lastupdatedtime): String
  [Name](#cfn-frauddetector-detector-eventvariable-name): String
  [Tags](#cfn-frauddetector-detector-eventvariable-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VariableType](#cfn-frauddetector-detector-eventvariable-variabletype): String
```

## Properties<a name="aws-properties-frauddetector-detector-eventvariable-properties"></a>

`Arn`  <a name="cfn-frauddetector-detector-eventvariable-arn"></a>
The event variable ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CreatedTime`  <a name="cfn-frauddetector-detector-eventvariable-createdtime"></a>
Timestamp for when the event variable was created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSource`  <a name="cfn-frauddetector-detector-eventvariable-datasource"></a>
The data source of the event variable\.  
Valid values: `EVENT | EXTERNAL_MODEL_SCORE`  
When defining a variable within a detector, you can only use the `EVENT` value for DataSource when the *Inline* property is set to true\. If the *Inline* property is set false, you can use either `EVENT` or `MODEL_SCORE` for DataSource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataType`  <a name="cfn-frauddetector-detector-eventvariable-datatype"></a>
The data type of the event variable\.  
Valid values: `STRING | INTEGER | BOOLEAN | FLOAT`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultValue`  <a name="cfn-frauddetector-detector-eventvariable-defaultvalue"></a>
The default value of the event variable\. This is required if you are providing the details of your variables instead of the ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-frauddetector-detector-eventvariable-description"></a>
The description of the event variable\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Inline`  <a name="cfn-frauddetector-detector-eventvariable-inline"></a>
Indicates whether the resource is defined within this CloudFormation template and impacts the create, update, and delete behavior of the stack\. If the value is `true`, CloudFormation will create/update/delete the resource when creating/updating/deleting the stack\. If the value is `false`, CloudFormation will validate that the object exists and then use it within the resource without making changes to the object\.   
For example, when creating `AWS::FraudDetector::Detector` you must define at least two variables\. You can set `Inline=true` for these variables and CloudFormation will create/update/delete the variables as part of stack operations\. However, if you set `Inline=false`, CloudFormation will associate the variables to your detector but not execute any changes to the variables\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastUpdatedTime`  <a name="cfn-frauddetector-detector-eventvariable-lastupdatedtime"></a>
Timestamp for when the event variable was last updated\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-frauddetector-detector-eventvariable-name"></a>
The name of the event variable\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-frauddetector-detector-eventvariable-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VariableType`  <a name="cfn-frauddetector-detector-eventvariable-variabletype"></a>
The type of event variable\. For more information, see [Variable types](https://docs.aws.amazon.com/frauddetector/latest/ug/create-a-variable.html#variable-types)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)