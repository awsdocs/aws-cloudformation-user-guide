# AWS::Omics::Workflow<a name="aws-resource-omics-workflow"></a>

Creates a workflow\.

## Syntax<a name="aws-resource-omics-workflow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-omics-workflow-syntax.json"></a>

```
{
  "Type" : "AWS::Omics::Workflow",
  "Properties" : {
      "[DefinitionUri](#cfn-omics-workflow-definitionuri)" : String,
      "[Description](#cfn-omics-workflow-description)" : String,
      "[Engine](#cfn-omics-workflow-engine)" : String,
      "[Main](#cfn-omics-workflow-main)" : String,
      "[Name](#cfn-omics-workflow-name)" : String,
      "[ParameterTemplate](#cfn-omics-workflow-parametertemplate)" : {Key : Value, ...},
      "[StorageCapacity](#cfn-omics-workflow-storagecapacity)" : Double,
      "[Tags](#cfn-omics-workflow-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-omics-workflow-syntax.yaml"></a>

```
Type: AWS::Omics::Workflow
Properties: 
  [DefinitionUri](#cfn-omics-workflow-definitionuri): String
  [Description](#cfn-omics-workflow-description): String
  [Engine](#cfn-omics-workflow-engine): String
  [Main](#cfn-omics-workflow-main): String
  [Name](#cfn-omics-workflow-name): String
  [ParameterTemplate](#cfn-omics-workflow-parametertemplate): 
    Key : Value
  [StorageCapacity](#cfn-omics-workflow-storagecapacity): Double
  [Tags](#cfn-omics-workflow-tags): 
    Key : Value
```

## Properties<a name="aws-resource-omics-workflow-properties"></a>

`DefinitionUri`  <a name="cfn-omics-workflow-definitionuri"></a>
The URI of a definition for the workflow\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\p{L}||\p{M}||\p{Z}||\p{S}||\p{N}||\p{P}]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-omics-workflow-description"></a>
The parameter's description\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `[\p{L}||\p{M}||\p{Z}||\p{S}||\p{N}||\p{P}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-omics-workflow-engine"></a>
An engine for the workflow\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NEXTFLOW | WDL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Main`  <a name="cfn-omics-workflow-main"></a>
The path of the main definition file for the workflow\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\p{L}||\p{M}||\p{Z}||\p{S}||\p{N}||\p{P}]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-omics-workflow-name"></a>
The workflow's name\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\p{L}||\p{M}||\p{Z}||\p{S}||\p{N}||\p{P}]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterTemplate`  <a name="cfn-omics-workflow-parametertemplate"></a>
The workflow's parameter template\.  
*Required*: No  
*Type*: Map of [WorkflowParameter](aws-properties-omics-workflow-workflowparameter.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageCapacity`  <a name="cfn-omics-workflow-storagecapacity"></a>
A storage capacity for the workflow in gigabytes\.  
*Required*: No  
*Type*: Double  
*Minimum*: `0`  
*Maximum*: `100000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-omics-workflow-tags"></a>
Tags for the workflow\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-omics-workflow-return-values"></a>

### Ref<a name="aws-resource-omics-workflow-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the details of this resource\. For example:

 `{ "Ref": "Workflow.Type" }` `Ref` returns the type of workflow\. 

### Fn::GetAtt<a name="aws-resource-omics-workflow-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-omics-workflow-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN for the workflow\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
When the workflow was created\.

`Id`  <a name="Id-fn::getatt"></a>
The workflow's ID\.

`Status`  <a name="Status-fn::getatt"></a>
The workflow's status\.

`Type`  <a name="Type-fn::getatt"></a>
The workflow's type\.