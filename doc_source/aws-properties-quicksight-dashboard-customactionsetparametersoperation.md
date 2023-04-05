# AWS::QuickSight::Dashboard CustomActionSetParametersOperation<a name="aws-properties-quicksight-dashboard-customactionsetparametersoperation"></a>

The set parameter operation that sets parameters in custom action\.

## Syntax<a name="aws-properties-quicksight-dashboard-customactionsetparametersoperation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-customactionsetparametersoperation-syntax.json"></a>

```
{
  "[ParameterValueConfigurations](#cfn-quicksight-dashboard-customactionsetparametersoperation-parametervalueconfigurations)" : [ SetParameterValueConfiguration, ... ]
}
```

### YAML<a name="aws-properties-quicksight-dashboard-customactionsetparametersoperation-syntax.yaml"></a>

```
  [ParameterValueConfigurations](#cfn-quicksight-dashboard-customactionsetparametersoperation-parametervalueconfigurations): 
    - SetParameterValueConfiguration
```

## Properties<a name="aws-properties-quicksight-dashboard-customactionsetparametersoperation-properties"></a>

`ParameterValueConfigurations`  <a name="cfn-quicksight-dashboard-customactionsetparametersoperation-parametervalueconfigurations"></a>
The parameter that determines the value configuration\.  
*Required*: Yes  
*Type*: List of [SetParameterValueConfiguration](aws-properties-quicksight-dashboard-setparametervalueconfiguration.md)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)