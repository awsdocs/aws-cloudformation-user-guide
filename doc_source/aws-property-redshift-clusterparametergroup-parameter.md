# Amazon Redshift Parameter Type<a name="aws-property-redshift-clusterparametergroup-parameter"></a>

Describes parameters for the [AWS::Redshift::ClusterParameterGroup](aws-resource-redshift-clusterparametergroup.md) resource type\.

## Syntax<a name="w3ab2c21c14e1617b5"></a>

### JSON<a name="aws-properties-redshift-clusterparametergroup-parameter-syntax.json"></a>

```
{
  "[ParameterName](#cfn-redshift-clusterparametergroup-parameter-parametername)" : String,
  "[ParameterValue](#cfn-redshift-clusterparametergroup-parameter-parametervalue)" : String
}
```

### YAML<a name="aws-properties-redshift-clusterparametergroup-parameter-syntax.yaml"></a>

```
[ParameterName](#cfn-redshift-clusterparametergroup-parameter-parametername): String
[ParameterValue](#cfn-redshift-clusterparametergroup-parameter-parametervalue): String
```

## Properties<a name="w3ab2c21c14e1617b7"></a>

`ParameterName`  <a name="cfn-redshift-clusterparametergroup-parameter-parametername"></a>
The name of the parameter\.  
*Required*: Yes  
*Type*: String

`ParameterValue`  <a name="cfn-redshift-clusterparametergroup-parameter-parametervalue"></a>
The value of the parameter\.  
*Required*: Yes  
*Type*: String