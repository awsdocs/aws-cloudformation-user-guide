# AWS::AppFlow::Flow ZendeskDestinationProperties<a name="aws-properties-appflow-flow-zendeskdestinationproperties"></a>

The properties that are applied when Zendesk is used as a destination\.

## Syntax<a name="aws-properties-appflow-flow-zendeskdestinationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-zendeskdestinationproperties-syntax.json"></a>

```
{
  "[ErrorHandlingConfig](#cfn-appflow-flow-zendeskdestinationproperties-errorhandlingconfig)" : ErrorHandlingConfig,
  "[IdFieldNames](#cfn-appflow-flow-zendeskdestinationproperties-idfieldnames)" : [ String, ... ],
  "[Object](#cfn-appflow-flow-zendeskdestinationproperties-object)" : String,
  "[WriteOperationType](#cfn-appflow-flow-zendeskdestinationproperties-writeoperationtype)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-zendeskdestinationproperties-syntax.yaml"></a>

```
  [ErrorHandlingConfig](#cfn-appflow-flow-zendeskdestinationproperties-errorhandlingconfig): 
    ErrorHandlingConfig
  [IdFieldNames](#cfn-appflow-flow-zendeskdestinationproperties-idfieldnames): 
    - String
  [Object](#cfn-appflow-flow-zendeskdestinationproperties-object): String
  [WriteOperationType](#cfn-appflow-flow-zendeskdestinationproperties-writeoperationtype): String
```

## Properties<a name="aws-properties-appflow-flow-zendeskdestinationproperties-properties"></a>

`ErrorHandlingConfig`  <a name="cfn-appflow-flow-zendeskdestinationproperties-errorhandlingconfig"></a>
 The settings that determine how Amazon AppFlow handles an error when placing data in the destination\. For example, this setting would determine if the flow should fail after one insertion error, or continue and attempt to insert every record regardless of the initial failure\. `ErrorHandlingConfig` is a part of the destination connector details\.   
*Required*: No  
*Type*: [ErrorHandlingConfig](aws-properties-appflow-flow-errorhandlingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdFieldNames`  <a name="cfn-appflow-flow-zendeskdestinationproperties-idfieldnames"></a>
 A list of field names that can be used as an ID field when performing a write operation\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Object`  <a name="cfn-appflow-flow-zendeskdestinationproperties-object"></a>
The object specified in the Zendesk flow destination\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WriteOperationType`  <a name="cfn-appflow-flow-zendeskdestinationproperties-writeoperationtype"></a>
 The possible write operations in the destination connector\. When this value is not provided, this defaults to the `INSERT` operation\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)