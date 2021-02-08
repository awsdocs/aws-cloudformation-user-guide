# AWS::Batch::JobDefinition NodeRangeProperty<a name="aws-properties-batch-jobdefinition-noderangeproperty"></a>

An object representing the properties of the node range for a multi\-node parallel job\.

## Syntax<a name="aws-properties-batch-jobdefinition-noderangeproperty-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-noderangeproperty-syntax.json"></a>

```
{
  "[Container](#cfn-batch-jobdefinition-noderangeproperty-container)" : ContainerProperties,
  "[TargetNodes](#cfn-batch-jobdefinition-noderangeproperty-targetnodes)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-noderangeproperty-syntax.yaml"></a>

```
  [Container](#cfn-batch-jobdefinition-noderangeproperty-container): 
    ContainerProperties
  [TargetNodes](#cfn-batch-jobdefinition-noderangeproperty-targetnodes): String
```

## Properties<a name="aws-properties-batch-jobdefinition-noderangeproperty-properties"></a>

`Container`  <a name="cfn-batch-jobdefinition-noderangeproperty-container"></a>
The container details for the node range\.  
*Required*: No  
*Type*: [ContainerProperties](aws-properties-batch-jobdefinition-containerproperties.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetNodes`  <a name="cfn-batch-jobdefinition-noderangeproperty-targetnodes"></a>
The range of nodes, using node index values\. A range of `0:3` indicates nodes with index values of `0` through `3`\. If the starting range value is omitted \(`:n`\), then `0` is used to start the range\. If the ending range value is omitted \(`n:`\), then the highest possible node index is used to end the range\. Your accumulative node ranges must account for all nodes \(`0:n`\)\. You can nest node ranges, for example `0:10` and `4:5`, in which case the `4:5` range properties override the `0:10` properties\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-batch-jobdefinition-noderangeproperty--seealso"></a>
+  [Multi\-node Parallel Jobs](https://docs.aws.amazon.com/batch/latest/userguide/multi-node-parallel-jobs.html) in the *AWS Batch User Guide*\.