# AWS::QuickSight::DataSource AthenaParameters<a name="aws-properties-quicksight-datasource-athenaparameters"></a>

Parameters for Amazon Athena\.

## Syntax<a name="aws-properties-quicksight-datasource-athenaparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-datasource-athenaparameters-syntax.json"></a>

```
{
  "[RoleArn](#cfn-quicksight-datasource-athenaparameters-rolearn)" : String,
  "[WorkGroup](#cfn-quicksight-datasource-athenaparameters-workgroup)" : String
}
```

### YAML<a name="aws-properties-quicksight-datasource-athenaparameters-syntax.yaml"></a>

```
  [RoleArn](#cfn-quicksight-datasource-athenaparameters-rolearn): String
  [WorkGroup](#cfn-quicksight-datasource-athenaparameters-workgroup): String
```

## Properties<a name="aws-properties-quicksight-datasource-athenaparameters-properties"></a>

`RoleArn`  <a name="cfn-quicksight-datasource-athenaparameters-rolearn"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkGroup`  <a name="cfn-quicksight-datasource-athenaparameters-workgroup"></a>
The workgroup that Amazon Athena uses\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)