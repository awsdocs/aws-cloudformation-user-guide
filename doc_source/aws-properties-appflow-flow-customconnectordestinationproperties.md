# AWS::AppFlow::Flow CustomConnectorDestinationProperties<a name="aws-properties-appflow-flow-customconnectordestinationproperties"></a>

The properties that are applied when the custom connector is being used as a destination\.

## Syntax<a name="aws-properties-appflow-flow-customconnectordestinationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-customconnectordestinationproperties-syntax.json"></a>

```
{
  "[CustomProperties](#cfn-appflow-flow-customconnectordestinationproperties-customproperties)" : {Key : Value, ...},
  "[EntityName](#cfn-appflow-flow-customconnectordestinationproperties-entityname)" : String,
  "[ErrorHandlingConfig](#cfn-appflow-flow-customconnectordestinationproperties-errorhandlingconfig)" : ErrorHandlingConfig,
  "[IdFieldNames](#cfn-appflow-flow-customconnectordestinationproperties-idfieldnames)" : [ String, ... ],
  "[WriteOperationType](#cfn-appflow-flow-customconnectordestinationproperties-writeoperationtype)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-customconnectordestinationproperties-syntax.yaml"></a>

```
  [CustomProperties](#cfn-appflow-flow-customconnectordestinationproperties-customproperties): 
    Key : Value
  [EntityName](#cfn-appflow-flow-customconnectordestinationproperties-entityname): String
  [ErrorHandlingConfig](#cfn-appflow-flow-customconnectordestinationproperties-errorhandlingconfig): 
    ErrorHandlingConfig
  [IdFieldNames](#cfn-appflow-flow-customconnectordestinationproperties-idfieldnames): 
    - String
  [WriteOperationType](#cfn-appflow-flow-customconnectordestinationproperties-writeoperationtype): String
```

## Properties<a name="aws-properties-appflow-flow-customconnectordestinationproperties-properties"></a>

`CustomProperties`  <a name="cfn-appflow-flow-customconnectordestinationproperties-customproperties"></a>
The custom properties that are specific to the connector when it's used as a destination in the flow\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EntityName`  <a name="cfn-appflow-flow-customconnectordestinationproperties-entityname"></a>
The entity specified in the custom connector as a destination in the flow\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorHandlingConfig`  <a name="cfn-appflow-flow-customconnectordestinationproperties-errorhandlingconfig"></a>
The settings that determine how Amazon AppFlow handles an error when placing data in the custom connector as destination\.  
*Required*: No  
*Type*: [ErrorHandlingConfig](aws-properties-appflow-flow-errorhandlingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdFieldNames`  <a name="cfn-appflow-flow-customconnectordestinationproperties-idfieldnames"></a>
The name of the field that Amazon AppFlow uses as an ID when performing a write operation such as update, delete, or upsert\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WriteOperationType`  <a name="cfn-appflow-flow-customconnectordestinationproperties-writeoperationtype"></a>
Specifies the type of write operation to be performed in the custom connector when it's used as destination\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DELETE | INSERT | UPDATE | UPSERT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)