# AWS::Glue::Workflow<a name="aws-resource-glue-workflow"></a>

The AWS::Glue::Workflow is an AWS Glue resource type that manages AWS Glue workflows\. A workflow is a container for a set of related jobs, crawlers, and triggers in AWS Glue\. Using a workflow, you can design a complex multi\-job extract, transform, and load \(ETL\) activity that AWS Glue can execute and track as single entity\.

## Syntax<a name="aws-resource-glue-workflow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-workflow-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Workflow",
  "Properties" : {
      "[DefaultRunProperties](#cfn-glue-workflow-defaultrunproperties)" : Json,
      "[Description](#cfn-glue-workflow-description)" : String,
      "[Name](#cfn-glue-workflow-name)" : String,
      "[Tags](#cfn-glue-workflow-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-glue-workflow-syntax.yaml"></a>

```
Type: AWS::Glue::Workflow
Properties: 
  [DefaultRunProperties](#cfn-glue-workflow-defaultrunproperties): Json
  [Description](#cfn-glue-workflow-description): String
  [Name](#cfn-glue-workflow-name): String
  [Tags](#cfn-glue-workflow-tags): Json
```

## Properties<a name="aws-resource-glue-workflow-properties"></a>

`DefaultRunProperties`  <a name="cfn-glue-workflow-defaultrunproperties"></a>
A collection of properties to be used as part of each execution of the workflow  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-glue-workflow-description"></a>
A description of the workflow  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-workflow-name"></a>
The name of the workflow representing the flow  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-glue-workflow-tags"></a>
The tags to use with this workflow\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-glue-workflow-return-values"></a>

### Ref<a name="aws-resource-glue-workflow-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the workflow name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.