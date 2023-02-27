# AWS::Athena::WorkGroup EngineVersion<a name="aws-properties-athena-workgroup-engineversion"></a>

The Athena engine version for running queries, or the PySpark engine version for running sessions\.

## Syntax<a name="aws-properties-athena-workgroup-engineversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-athena-workgroup-engineversion-syntax.json"></a>

```
{
  "[EffectiveEngineVersion](#cfn-athena-workgroup-engineversion-effectiveengineversion)" : String,
  "[SelectedEngineVersion](#cfn-athena-workgroup-engineversion-selectedengineversion)" : String
}
```

### YAML<a name="aws-properties-athena-workgroup-engineversion-syntax.yaml"></a>

```
  [EffectiveEngineVersion](#cfn-athena-workgroup-engineversion-effectiveengineversion): String
  [SelectedEngineVersion](#cfn-athena-workgroup-engineversion-selectedengineversion): String
```

## Properties<a name="aws-properties-athena-workgroup-engineversion-properties"></a>

`EffectiveEngineVersion`  <a name="cfn-athena-workgroup-engineversion-effectiveengineversion"></a>
Read only\. The engine version on which the query runs\. If the user requests a valid engine version other than Auto, the effective engine version is the same as the engine version that the user requested\. If the user requests Auto, the effective engine version is chosen by Athena\. When a request to update the engine version is made by a `CreateWorkGroup` or `UpdateWorkGroup` operation, the `EffectiveEngineVersion` field is ignored\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SelectedEngineVersion`  <a name="cfn-athena-workgroup-engineversion-selectedengineversion"></a>
The engine version requested by the user\. Possible values are determined by the output of `ListEngineVersions`, including AUTO\. The default is AUTO\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)