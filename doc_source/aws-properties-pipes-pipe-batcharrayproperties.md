# AWS::Pipes::Pipe BatchArrayProperties<a name="aws-properties-pipes-pipe-batcharrayproperties"></a>

The array properties for the submitted job, such as the size of the array\. The array size can be between 2 and 10,000\. If you specify array properties for a job, it becomes an array job\. This parameter is used only if the target is an AWS Batch job\.

## Syntax<a name="aws-properties-pipes-pipe-batcharrayproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pipes-pipe-batcharrayproperties-syntax.json"></a>

```
{
  "[Size](#cfn-pipes-pipe-batcharrayproperties-size)" : Integer
}
```

### YAML<a name="aws-properties-pipes-pipe-batcharrayproperties-syntax.yaml"></a>

```
  [Size](#cfn-pipes-pipe-batcharrayproperties-size): Integer
```

## Properties<a name="aws-properties-pipes-pipe-batcharrayproperties-properties"></a>

`Size`  <a name="cfn-pipes-pipe-batcharrayproperties-size"></a>
The size of the array, if this is an array batch job\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)