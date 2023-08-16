# AWS::Batch::JobDefinition EphemeralStorage<a name="aws-properties-batch-jobdefinition-containerproperties-ephemeralstorage"></a>

The amount of ephemeral storage to allocate for the task\. This parameter is used to expand the total amount of ephemeral storage available, beyond the default amount, for tasks hosted on AWS Fargate\.

## Syntax<a name="aws-properties-batch-jobdefinition-containerproperties-ephemeralstorage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-containerproperties-ephemeralstorage-syntax.json"></a>

```
{
  "[SizeInGiB](#cfn-batch-jobdefinition-containerproperties-ephemeralstorage-sizeingib)" : Integer
}
```

### YAML<a name="aws-properties-batch-jobdefinition-containerproperties-ephemeralstorage-syntax.yaml"></a>

```
  [SizeInGiB](#cfn-batch-jobdefinition-containerproperties-ephemeralstorage-sizeingib): Integer
```

## Properties<a name="aws-properties-batch-jobdefinition-containerproperties-ephemeralstorage-properties"></a>

`SizeInGiB`  <a name="cfn-batch-jobdefinition-containerproperties-ephemeralstorage-sizeingib"></a>
The total amount, in GiB, of ephemeral storage to set for the task\. The minimum supported value is `21` GiB and the maximum supported value is `200` GiB\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)