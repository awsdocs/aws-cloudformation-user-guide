# AWS::DataBrew::Recipe Action<a name="aws-properties-databrew-recipe-action"></a>

Represents a transformation and associated parameters that are used to apply a change to an AWS Glue DataBrew dataset\.

## Syntax<a name="aws-properties-databrew-recipe-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-recipe-action-syntax.json"></a>

```
{
  "[Operation](#cfn-databrew-recipe-action-operation)" : String,
  "[Parameters](#cfn-databrew-recipe-action-parameters)" : 
}
```

### YAML<a name="aws-properties-databrew-recipe-action-syntax.yaml"></a>

```
  [Operation](#cfn-databrew-recipe-action-operation): String
  [Parameters](#cfn-databrew-recipe-action-parameters):
```

## Properties<a name="aws-properties-databrew-recipe-action-properties"></a>

`Operation`  <a name="cfn-databrew-recipe-action-operation"></a>
The name of a valid DataBrew transformation to be performed on the data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-databrew-recipe-action-parameters"></a>
Contextual parameters for the transformation\.  
*Required*: No  
*Type*:   
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)