# AWS::QuickSight::Template RollingDateConfiguration<a name="aws-properties-quicksight-template-rollingdateconfiguration"></a>

The rolling date configuration of a date time filter\.

## Syntax<a name="aws-properties-quicksight-template-rollingdateconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-rollingdateconfiguration-syntax.json"></a>

```
{
  "[DataSetIdentifier](#cfn-quicksight-template-rollingdateconfiguration-datasetidentifier)" : String,
  "[Expression](#cfn-quicksight-template-rollingdateconfiguration-expression)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-rollingdateconfiguration-syntax.yaml"></a>

```
  [DataSetIdentifier](#cfn-quicksight-template-rollingdateconfiguration-datasetidentifier): String
  [Expression](#cfn-quicksight-template-rollingdateconfiguration-expression): String
```

## Properties<a name="aws-properties-quicksight-template-rollingdateconfiguration-properties"></a>

`DataSetIdentifier`  <a name="cfn-quicksight-template-rollingdateconfiguration-datasetidentifier"></a>
The data set that is used in the rolling date configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-quicksight-template-rollingdateconfiguration-expression"></a>
The expression of the rolling date configuration\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)