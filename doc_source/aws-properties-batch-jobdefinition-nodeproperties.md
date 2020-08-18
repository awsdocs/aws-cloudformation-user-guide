# AWS::Batch::JobDefinition NodeProperties<a name="aws-properties-batch-jobdefinition-nodeproperties"></a>

An object representing the node properties of a multi\-node parallel job\.

## Syntax<a name="aws-properties-batch-jobdefinition-nodeproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-nodeproperties-syntax.json"></a>

```
{
  "[MainNode](#cfn-batch-jobdefinition-nodeproperties-mainnode)" : Integer,
  "[NodeRangeProperties](#cfn-batch-jobdefinition-nodeproperties-noderangeproperties)" : [ NodeRangeProperty, ... ],
  "[NumNodes](#cfn-batch-jobdefinition-nodeproperties-numnodes)" : Integer
}
```

### YAML<a name="aws-properties-batch-jobdefinition-nodeproperties-syntax.yaml"></a>

```
  [MainNode](#cfn-batch-jobdefinition-nodeproperties-mainnode): Integer
  [NodeRangeProperties](#cfn-batch-jobdefinition-nodeproperties-noderangeproperties): 
    - NodeRangeProperty
  [NumNodes](#cfn-batch-jobdefinition-nodeproperties-numnodes): Integer
```

## Properties<a name="aws-properties-batch-jobdefinition-nodeproperties-properties"></a>

`MainNode`  <a name="cfn-batch-jobdefinition-nodeproperties-mainnode"></a>
Specifies the node index for the main node of a multi\-node parallel job\. This node index value must be fewer than the number of nodes\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NodeRangeProperties`  <a name="cfn-batch-jobdefinition-nodeproperties-noderangeproperties"></a>
A list of node ranges and their properties associated with a multi\-node parallel job\.  
*Required*: Yes  
*Type*: List of [NodeRangeProperty](aws-properties-batch-jobdefinition-noderangeproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumNodes`  <a name="cfn-batch-jobdefinition-nodeproperties-numnodes"></a>
The number of nodes associated with a multi\-node parallel job\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-batch-jobdefinition-nodeproperties--seealso"></a>
+  [Multi\-node Parallel Jobs](https://docs.aws.amazon.com/batch/latest/userguide/multi-node-parallel-jobs.html) in the *AWS Batch User Guide*\.