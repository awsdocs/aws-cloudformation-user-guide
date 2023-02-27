# AWS::AppFlow::Flow SalesforceDestinationProperties<a name="aws-properties-appflow-flow-salesforcedestinationproperties"></a>

 The properties that are applied when Salesforce is being used as a destination\. 

## Syntax<a name="aws-properties-appflow-flow-salesforcedestinationproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-salesforcedestinationproperties-syntax.json"></a>

```
{
  "[DataTransferApi](#cfn-appflow-flow-salesforcedestinationproperties-datatransferapi)" : String,
  "[ErrorHandlingConfig](#cfn-appflow-flow-salesforcedestinationproperties-errorhandlingconfig)" : ErrorHandlingConfig,
  "[IdFieldNames](#cfn-appflow-flow-salesforcedestinationproperties-idfieldnames)" : [ String, ... ],
  "[Object](#cfn-appflow-flow-salesforcedestinationproperties-object)" : String,
  "[WriteOperationType](#cfn-appflow-flow-salesforcedestinationproperties-writeoperationtype)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-salesforcedestinationproperties-syntax.yaml"></a>

```
  [DataTransferApi](#cfn-appflow-flow-salesforcedestinationproperties-datatransferapi): String
  [ErrorHandlingConfig](#cfn-appflow-flow-salesforcedestinationproperties-errorhandlingconfig): 
    ErrorHandlingConfig
  [IdFieldNames](#cfn-appflow-flow-salesforcedestinationproperties-idfieldnames): 
    - String
  [Object](#cfn-appflow-flow-salesforcedestinationproperties-object): String
  [WriteOperationType](#cfn-appflow-flow-salesforcedestinationproperties-writeoperationtype): String
```

## Properties<a name="aws-properties-appflow-flow-salesforcedestinationproperties-properties"></a>

`DataTransferApi`  <a name="cfn-appflow-flow-salesforcedestinationproperties-datatransferapi"></a>
Specifies which Salesforce API is used by Amazon AppFlow when your flow transfers data to Salesforce\.    
AUTOMATIC  
The default\. Amazon AppFlow selects which API to use based on the number of records that your flow transfers to Salesforce\. If your flow transfers fewer than 1,000 records, Amazon AppFlow uses Salesforce REST API\. If your flow transfers 1,000 records or more, Amazon AppFlow uses Salesforce Bulk API 2\.0\.  
Each of these Salesforce APIs structures data differently\. If Amazon AppFlow selects the API automatically, be aware that, for recurring flows, the data output might vary from one flow run to the next\. For example, if a flow runs daily, it might use REST API on one day to transfer 900 records, and it might use Bulk API 2\.0 on the next day to transfer 1,100 records\. For each of these flow runs, the respective Salesforce API formats the data differently\. Some of the differences include how dates are formatted and null values are represented\. Also, Bulk API 2\.0 doesn't transfer Salesforce compound fields\.  
By choosing this option, you optimize flow performance for both small and large data transfers, but the tradeoff is inconsistent formatting in the output\.  
BULKV2  
Amazon AppFlow uses only Salesforce Bulk API 2\.0\. This API runs asynchronous data transfers, and it's optimal for large sets of data\. By choosing this option, you ensure that your flow writes consistent output, but you optimize performance only for large data transfers\.  
Note that Bulk API 2\.0 does not transfer Salesforce compound fields\.  
REST\_SYNC  
Amazon AppFlow uses only Salesforce REST API\. By choosing this option, you ensure that your flow writes consistent output, but you decrease performance for large data transfers that are better suited for Bulk API 2\.0\. In some cases, if your flow attempts to transfer a vary large set of data, it might fail with a timed out error\.
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | BULKV2 | REST_SYNC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorHandlingConfig`  <a name="cfn-appflow-flow-salesforcedestinationproperties-errorhandlingconfig"></a>
 The settings that determine how Amazon AppFlow handles an error when placing data in the Salesforce destination\. For example, this setting would determine if the flow should fail after one insertion error, or continue and attempt to insert every record regardless of the initial failure\. `ErrorHandlingConfig` is a part of the destination connector details\.   
*Required*: No  
*Type*: [ErrorHandlingConfig](aws-properties-appflow-flow-errorhandlingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdFieldNames`  <a name="cfn-appflow-flow-salesforcedestinationproperties-idfieldnames"></a>
 The name of the field that Amazon AppFlow uses as an ID when performing a write operation such as update or delete\.   
*Required*: No  
*Type*: List of String  
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
*Allowed values*: `DELETE | INSERT | UPDATE | UPSERT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-salesforcedestinationproperties--seealso"></a>
+ [SalesforceDestinationProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_SalesforceDestinationProperties.html) in the *Amazon AppFlow API Reference*\.

