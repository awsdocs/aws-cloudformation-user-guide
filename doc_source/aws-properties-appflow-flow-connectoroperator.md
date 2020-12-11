# AWS::AppFlow::Flow ConnectorOperator<a name="aws-properties-appflow-flow-connectoroperator"></a>

 The operation to be performed on the provided source fields\. 

## Syntax<a name="aws-properties-appflow-flow-connectoroperator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-connectoroperator-syntax.json"></a>

```
{
  "[Amplitude](#cfn-appflow-flow-connectoroperator-amplitude)" : String,
  "[Datadog](#cfn-appflow-flow-connectoroperator-datadog)" : String,
  "[Dynatrace](#cfn-appflow-flow-connectoroperator-dynatrace)" : String,
  "[GoogleAnalytics](#cfn-appflow-flow-connectoroperator-googleanalytics)" : String,
  "[InforNexus](#cfn-appflow-flow-connectoroperator-infornexus)" : String,
  "[Marketo](#cfn-appflow-flow-connectoroperator-marketo)" : String,
  "[S3](#cfn-appflow-flow-connectoroperator-s3)" : String,
  "[Salesforce](#cfn-appflow-flow-connectoroperator-salesforce)" : String,
  "[ServiceNow](#cfn-appflow-flow-connectoroperator-servicenow)" : String,
  "[Singular](#cfn-appflow-flow-connectoroperator-singular)" : String,
  "[Slack](#cfn-appflow-flow-connectoroperator-slack)" : String,
  "[Trendmicro](#cfn-appflow-flow-connectoroperator-trendmicro)" : String,
  "[Veeva](#cfn-appflow-flow-connectoroperator-veeva)" : String,
  "[Zendesk](#cfn-appflow-flow-connectoroperator-zendesk)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-connectoroperator-syntax.yaml"></a>

```
  [Amplitude](#cfn-appflow-flow-connectoroperator-amplitude): String
  [Datadog](#cfn-appflow-flow-connectoroperator-datadog): String
  [Dynatrace](#cfn-appflow-flow-connectoroperator-dynatrace): String
  [GoogleAnalytics](#cfn-appflow-flow-connectoroperator-googleanalytics): String
  [InforNexus](#cfn-appflow-flow-connectoroperator-infornexus): String
  [Marketo](#cfn-appflow-flow-connectoroperator-marketo): String
  [S3](#cfn-appflow-flow-connectoroperator-s3): String
  [Salesforce](#cfn-appflow-flow-connectoroperator-salesforce): String
  [ServiceNow](#cfn-appflow-flow-connectoroperator-servicenow): String
  [Singular](#cfn-appflow-flow-connectoroperator-singular): String
  [Slack](#cfn-appflow-flow-connectoroperator-slack): String
  [Trendmicro](#cfn-appflow-flow-connectoroperator-trendmicro): String
  [Veeva](#cfn-appflow-flow-connectoroperator-veeva): String
  [Zendesk](#cfn-appflow-flow-connectoroperator-zendesk): String
```

## Properties<a name="aws-properties-appflow-flow-connectoroperator-properties"></a>

`Amplitude`  <a name="cfn-appflow-flow-connectoroperator-amplitude"></a>
 The operation to be performed on the provided Amplitude source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `BETWEEN`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Datadog`  <a name="cfn-appflow-flow-connectoroperator-datadog"></a>
 The operation to be performed on the provided Datadog source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | DIVISION | EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Dynatrace`  <a name="cfn-appflow-flow-connectoroperator-dynatrace"></a>
 The operation to be performed on the provided Dynatrace source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | DIVISION | EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GoogleAnalytics`  <a name="cfn-appflow-flow-connectoroperator-googleanalytics"></a>
 The operation to be performed on the provided Google Analytics source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `BETWEEN | PROJECTION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InforNexus`  <a name="cfn-appflow-flow-connectoroperator-infornexus"></a>
 The operation to be performed on the provided Infor Nexus source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | DIVISION | EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Marketo`  <a name="cfn-appflow-flow-connectoroperator-marketo"></a>
 The operation to be performed on the provided Marketo source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | DIVISION | GREATER_THAN | LESS_THAN | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-appflow-flow-connectoroperator-s3"></a>
 The operation to be performed on the provided Amazon S3 source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | DIVISION | EQUAL_TO | GREATER_THAN | GREATER_THAN_OR_EQUAL_TO | LESS_THAN | LESS_THAN_OR_EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | NOT_EQUAL_TO | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Salesforce`  <a name="cfn-appflow-flow-connectoroperator-salesforce"></a>
 The operation to be performed on the provided Salesforce source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | CONTAINS | DIVISION | EQUAL_TO | GREATER_THAN | GREATER_THAN_OR_EQUAL_TO | LESS_THAN | LESS_THAN_OR_EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | NOT_EQUAL_TO | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNow`  <a name="cfn-appflow-flow-connectoroperator-servicenow"></a>
 The operation to be performed on the provided ServiceNow source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | CONTAINS | DIVISION | EQUAL_TO | GREATER_THAN | GREATER_THAN_OR_EQUAL_TO | LESS_THAN | LESS_THAN_OR_EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | NOT_EQUAL_TO | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Singular`  <a name="cfn-appflow-flow-connectoroperator-singular"></a>
 The operation to be performed on the provided Singular source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | DIVISION | EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Slack`  <a name="cfn-appflow-flow-connectoroperator-slack"></a>
 The operation to be performed on the provided Slack source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | DIVISION | EQUAL_TO | GREATER_THAN | GREATER_THAN_OR_EQUAL_TO | LESS_THAN | LESS_THAN_OR_EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Trendmicro`  <a name="cfn-appflow-flow-connectoroperator-trendmicro"></a>
 The operation to be performed on the provided Trend Micro source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | DIVISION | EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Veeva`  <a name="cfn-appflow-flow-connectoroperator-veeva"></a>
 The operation to be performed on the provided Veeva source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | CONTAINS | DIVISION | EQUAL_TO | GREATER_THAN | GREATER_THAN_OR_EQUAL_TO | LESS_THAN | LESS_THAN_OR_EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | NOT_EQUAL_TO | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Zendesk`  <a name="cfn-appflow-flow-connectoroperator-zendesk"></a>
 The operation to be performed on the provided Zendesk source fields\.   
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | DIVISION | GREATER_THAN | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-appflow-flow-connectoroperator--seealso"></a>
+ [ConnectorOperator](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_ConnectorOperator.html) in the *Amazon AppFlow API Reference*\.

