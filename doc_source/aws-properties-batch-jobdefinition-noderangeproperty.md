# AWS Batch JobDefinition NodeRangeProperty<a name="aws-properties-batch-jobdefinition-noderangeproperty"></a>

<a name="aws-properties-batch-jobdefinition-noderangeproperty-description"></a>The `NodeRangeProperty` property type specifies the properties of a multi\-node parallel node range in a job definition\.

<a name="aws-properties-batch-jobdefinition-noderangeproperty-inheritance"></a> `NodeRangeProperty` is a property of the [NodeProperties](aws-properties-batch-jobdefinition-nodeproperties.md) property type\.

## Syntax<a name="aws-properties-batch-jobdefinition-noderangeproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-noderangeproperty-syntax.json"></a>

```
{
  "[Container](#cfn-batch-jobdefinition-noderangeproperty-container)" : [*ContainerProperties*](aws-properties-batch-jobdefinition-containerproperties.md),
  "[TargetNodes](#cfn-batch-jobdefinition-noderangeproperty-targetnodes)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-noderangeproperty-syntax.yaml"></a>

```
[Container](#cfn-batch-jobdefinition-noderangeproperty-container): 
  [*ContainerProperties*](aws-properties-batch-jobdefinition-containerproperties.md)
[TargetNodes](#cfn-batch-jobdefinition-noderangeproperty-targetnodes): String
```

## Properties<a name="aws-properties-batch-jobdefinition-noderangeproperty-properties"></a>

`Container`  <a name="cfn-batch-jobdefinition-noderangeproperty-container"></a>
The container details for the node range\.  
 *Required*: No  
 *Type*: [ContainerProperties](aws-properties-batch-jobdefinition-containerproperties.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TargetNodes`  <a name="cfn-batch-jobdefinition-noderangeproperty-targetnodes"></a>
The range of nodes, using node index values\. A range of `0:3` indicates nodes with index values of `0` through `3`\. If the starting range value is omitted \(`:n`\), then `0` is used to start the range\. If the ending range value is omitted \(`n:`\), then the highest possible node index is used to end the range\. Your accumulative node ranges must account for all nodes \(0:n\)\. You may nest node ranges, for example 0:10 and 4:5, in which case the 4:5 range properties override the 0:10 properties\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-batch-jobdefinition-noderangeproperty-seealso"></a>
+ [Multi\-node Parallel Jobs](https://docs.aws.amazon.com/batch/latest/userguide/multi-node-parallel-jobs.html) in the *AWS Batch User Guide*