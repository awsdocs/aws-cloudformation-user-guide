# AWS::RedshiftServerless::Workgroup ConfigParameter<a name="aws-properties-redshiftserverless-workgroup-configparameter"></a>

A array of parameters to set for more control over a serverless database\.

## Syntax<a name="aws-properties-redshiftserverless-workgroup-configparameter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-redshiftserverless-workgroup-configparameter-syntax.json"></a>

```
{
  "[ParameterKey](#cfn-redshiftserverless-workgroup-configparameter-parameterkey)" : String,
  "[ParameterValue](#cfn-redshiftserverless-workgroup-configparameter-parametervalue)" : String
}
```

### YAML<a name="aws-properties-redshiftserverless-workgroup-configparameter-syntax.yaml"></a>

```
  [ParameterKey](#cfn-redshiftserverless-workgroup-configparameter-parameterkey): String
  [ParameterValue](#cfn-redshiftserverless-workgroup-configparameter-parametervalue): String
```

## Properties<a name="aws-properties-redshiftserverless-workgroup-configparameter-properties"></a>

`ParameterKey`  <a name="cfn-redshiftserverless-workgroup-configparameter-parameterkey"></a>
The key of the parameter\. The options are `datestyle`, `enable_user_activity_logging`, `query_group`, `search_path`, and `max_query_execution_time`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParameterValue`  <a name="cfn-redshiftserverless-workgroup-configparameter-parametervalue"></a>
The value of the parameter to set\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)