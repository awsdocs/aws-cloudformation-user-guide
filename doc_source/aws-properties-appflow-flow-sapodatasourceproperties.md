# AWS::AppFlow::Flow SAPODataSourceProperties<a name="aws-properties-appflow-flow-sapodatasourceproperties"></a>

 The properties that are applied when using SAPOData as a flow source\. 

## Syntax<a name="aws-properties-appflow-flow-sapodatasourceproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-sapodatasourceproperties-syntax.json"></a>

```
{
  "[ObjectPath](#cfn-appflow-flow-sapodatasourceproperties-objectpath)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-sapodatasourceproperties-syntax.yaml"></a>

```
  [ObjectPath](#cfn-appflow-flow-sapodatasourceproperties-objectpath): String
```

## Properties<a name="aws-properties-appflow-flow-sapodatasourceproperties-properties"></a>

`ObjectPath`  <a name="cfn-appflow-flow-sapodatasourceproperties-objectpath"></a>
 The object path specified in the SAPOData flow source\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)