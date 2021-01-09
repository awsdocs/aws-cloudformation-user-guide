# AWS::Redshift::ClusterParameterGroup Parameter<a name="aws-property-redshift-clusterparametergroup-parameter"></a>

Describes a parameter in a cluster parameter group\.

## Syntax<a name="aws-property-redshift-clusterparametergroup-parameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-property-redshift-clusterparametergroup-parameter-syntax.json"></a>

```
{
  "[ParameterName](#cfn-redshift-clusterparametergroup-parameter-parametername)" : String,
  "[ParameterValue](#cfn-redshift-clusterparametergroup-parameter-parametervalue)" : String
}
```

### YAML<a name="aws-property-redshift-clusterparametergroup-parameter-syntax.yaml"></a>

```
  [ParameterName](#cfn-redshift-clusterparametergroup-parameter-parametername): String
  [ParameterValue](#cfn-redshift-clusterparametergroup-parameter-parametervalue): String
```

## Properties<a name="aws-property-redshift-clusterparametergroup-parameter-properties"></a>

`ParameterName`  <a name="cfn-redshift-clusterparametergroup-parameter-parametername"></a>
The name of the parameter\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValue`  <a name="cfn-redshift-clusterparametergroup-parameter-parametervalue"></a>
The value of the parameter\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)