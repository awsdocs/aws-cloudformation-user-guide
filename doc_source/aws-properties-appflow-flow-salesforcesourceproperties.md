# AWS::AppFlow::Flow SalesforceSourceProperties<a name="aws-properties-appflow-flow-salesforcesourceproperties"></a>

 The properties that are applied when Salesforce is being used as a source\. 

## Syntax<a name="aws-properties-appflow-flow-salesforcesourceproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-salesforcesourceproperties-syntax.json"></a>

```
{
  "[DataTransferApi](#cfn-appflow-flow-salesforcesourceproperties-datatransferapi)" : String,
  "[EnableDynamicFieldUpdate](#cfn-appflow-flow-salesforcesourceproperties-enabledynamicfieldupdate)" : Boolean,
  "[IncludeDeletedRecords](#cfn-appflow-flow-salesforcesourceproperties-includedeletedrecords)" : Boolean,
  "[Object](#cfn-appflow-flow-salesforcesourceproperties-object)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-salesforcesourceproperties-syntax.yaml"></a>

```
  [DataTransferApi](#cfn-appflow-flow-salesforcesourceproperties-datatransferapi): String
  [EnableDynamicFieldUpdate](#cfn-appflow-flow-salesforcesourceproperties-enabledynamicfieldupdate): Boolean
  [IncludeDeletedRecords](#cfn-appflow-flow-salesforcesourceproperties-includedeletedrecords): Boolean
  [Object](#cfn-appflow-flow-salesforcesourceproperties-object): String
```

## Properties<a name="aws-properties-appflow-flow-salesforcesourceproperties-properties"></a>

`DataTransferApi`  <a name="cfn-appflow-flow-salesforcesourceproperties-datatransferapi"></a>
Specifies which Salesforce API is used by Amazon AppFlow when your flow transfers data from Salesforce\.    
AUTOMATIC  
The default\. Amazon AppFlow selects which API to use based on the number of records that your flow transfers from Salesforce\. If your flow transfers fewer than 1,000,000 records, Amazon AppFlow uses Salesforce REST API\. If your flow transfers 1,000,000 records or more, Amazon AppFlow uses Salesforce Bulk API 2\.0\.  
Each of these Salesforce APIs structures data differently\. If Amazon AppFlow selects the API automatically, be aware that, for recurring flows, the data output might vary from one flow run to the next\. For example, if a flow runs daily, it might use REST API on one day to transfer 900,000 records, and it might use Bulk API 2\.0 on the next day to transfer 1,100,000 records\. For each of these flow runs, the respective Salesforce API formats the data differently\. Some of the differences include how dates are formatted and null values are represented\. Also, Bulk API 2\.0 doesn't transfer Salesforce compound fields\.  
By choosing this option, you optimize flow performance for both small and large data transfers, but the tradeoff is inconsistent formatting in the output\.  
BULKV2  
Amazon AppFlow uses only Salesforce Bulk API 2\.0\. This API runs asynchronous data transfers, and it's optimal for large sets of data\. By choosing this option, you ensure that your flow writes consistent output, but you optimize performance only for large data transfers\.  
Note that Bulk API 2\.0 does not transfer Salesforce compound fields\.  
REST\_SYNC  
Amazon AppFlow uses only Salesforce REST API\. By choosing this option, you ensure that your flow writes consistent output, but you decrease performance for large data transfers that are better suited for Bulk API 2\.0\. In some cases, if your flow attempts to transfer a vary large set of data, it might fail wituh a timed out error\.
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | BULKV2 | REST_SYNC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableDynamicFieldUpdate`  <a name="cfn-appflow-flow-salesforcesourceproperties-enabledynamicfieldupdate"></a>
 The flag that enables dynamic fetching of new \(recently added\) fields in the Salesforce objects while running a flow\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeDeletedRecords`  <a name="cfn-appflow-flow-salesforcesourceproperties-includedeletedrecords"></a>
 Indicates whether Amazon AppFlow includes deleted files in the flow run\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Object`  <a name="cfn-appflow-flow-salesforcesourceproperties-object"></a>
 The object specified in the Salesforce flow source\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `\S+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-salesforcesourceproperties--seealso"></a>
+ [SalesforceSourceProperties](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_SalesforceSourceProperties.html) in the *Amazon AppFlow API Reference*\.

