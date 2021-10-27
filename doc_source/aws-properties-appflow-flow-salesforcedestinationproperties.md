# AWS::AppFlow::Flow SalesforceDestinationProperties<a name="aws-properties-appflow-flow-salesforcedestinationproperties"></a>

 The properties that are applied when Salesforce is being used as a destination\. 

## Syntax<a name="aws-properties-appflow-flow-salesforcedestinationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-salesforcedestinationproperties-syntax.json"></a>

```
{
  "[ErrorHandlingConfig](#cfn-appflow-flow-salesforcedestinationproperties-errorhandlingconfig)" : ErrorHandlingConfig,
  "[IdFieldNames](#cfn-appflow-flow-salesforcedestinationproperties-idfieldnames)" : [ String, ... ],
  "[Object](#cfn-appflow-flow-salesforcedestinationproperties-object)" : String,
  "[WriteOperationType](#cfn-appflow-flow-salesforcedestinationproperties-writeoperationtype)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-salesforcedestinationproperties-syntax.yaml"></a>

```
  [ErrorHandlingConfig](#cfn-appflow-flow-salesforcedestinationproperties-errorhandlingconfig): 
    ErrorHandlingConfig
  [IdFieldNames](#cfn-appflow-flow-salesforcedestinationproperties-idfieldnames): 
    - String
  [Object](#cfn-appflow-flow-salesforcedestinationproperties-object): String
  [WriteOperationType](#cfn-appflow-flow-salesforcedestinationproperties-writeoperationtype): String
```

## Properties<a name="aws-properties-appflow-flow-salesforcedestinationproperties-properties"></a>

`ErrorHandlingConfig`  <a name="cfn-appflow-flow-salesforcedestinationproperties-errorhandlingconfig"></a>
 The settings that determine how Amazon AppFlow handles an error when placing data in the Salesforce destination\. For example, this setting would determine if the flow should fail after one insertion error, or continue and attempt to insert every record regardless of the initial failure\. `ErrorHandlingConfig` is a part of the destination connector details\.   
*Required*: No  
*Type*: [ErrorHandlingConfig](aws-properties-appflow-flow-errorhandlingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdFieldNames`  <a name="cfn-appflow-flow-salesforcedestinationproperties-idfieldnames"></a>
 The name of the field that Amazon AppFlow uses as an ID when performing a write operation such as update or delete\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Object`  <a name="cfn-appflow-flow-salesforcedestinationproperties-object"></a>
 The object specified in the Salesforce flow destination\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WriteOperationType`  <a name="cfn-appflow-flow-salesforcedestinationproperties-writeoperationtype"></a>
 This specifies the type of write operation to be performed in Salesforce\. When the value is `UPSERT`, then `idFieldNames` is required\.   
*Required*: No  
*Type*: String  
*Allowed values*: `INSERT | UPDATE | UPSERT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-salesforcedestinationproperties--seealso"></a>
+ [SalesforceDestinationProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_SalesforceDestinationProperties.html) in the *Amazon AppFlow API Reference*\.

