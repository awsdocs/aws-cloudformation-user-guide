# AWS::CustomerProfiles::Integration ConnectorOperator<a name="aws-properties-customerprofiles-integration-connectoroperator"></a>

The operation to be performed on the provided source fields\.

## Syntax<a name="aws-properties-customerprofiles-integration-connectoroperator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-connectoroperator-syntax.json"></a>

```
{
  "[Marketo](#cfn-customerprofiles-integration-connectoroperator-marketo)" : String,
  "[S3](#cfn-customerprofiles-integration-connectoroperator-s3)" : String,
  "[Salesforce](#cfn-customerprofiles-integration-connectoroperator-salesforce)" : String,
  "[ServiceNow](#cfn-customerprofiles-integration-connectoroperator-servicenow)" : String,
  "[Zendesk](#cfn-customerprofiles-integration-connectoroperator-zendesk)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-integration-connectoroperator-syntax.yaml"></a>

```
  [Marketo](#cfn-customerprofiles-integration-connectoroperator-marketo): String
  [S3](#cfn-customerprofiles-integration-connectoroperator-s3): String
  [Salesforce](#cfn-customerprofiles-integration-connectoroperator-salesforce): String
  [ServiceNow](#cfn-customerprofiles-integration-connectoroperator-servicenow): String
  [Zendesk](#cfn-customerprofiles-integration-connectoroperator-zendesk): String
```

## Properties<a name="aws-properties-customerprofiles-integration-connectoroperator-properties"></a>

`Marketo`  <a name="cfn-customerprofiles-integration-connectoroperator-marketo"></a>
The operation to be performed on the provided Marketo source fields\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | DIVISION | GREATER_THAN | LESS_THAN | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3`  <a name="cfn-customerprofiles-integration-connectoroperator-s3"></a>
The operation to be performed on the provided Amazon S3 source fields\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | DIVISION | EQUAL_TO | GREATER_THAN | GREATER_THAN_OR_EQUAL_TO | LESS_THAN | LESS_THAN_OR_EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | NOT_EQUAL_TO | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Salesforce`  <a name="cfn-customerprofiles-integration-connectoroperator-salesforce"></a>
The operation to be performed on the provided Salesforce source fields\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | CONTAINS | DIVISION | EQUAL_TO | GREATER_THAN | GREATER_THAN_OR_EQUAL_TO | LESS_THAN | LESS_THAN_OR_EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | NOT_EQUAL_TO | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNow`  <a name="cfn-customerprofiles-integration-connectoroperator-servicenow"></a>
The operation to be performed on the provided ServiceNow source fields\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | BETWEEN | CONTAINS | DIVISION | EQUAL_TO | GREATER_THAN | GREATER_THAN_OR_EQUAL_TO | LESS_THAN | LESS_THAN_OR_EQUAL_TO | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | NOT_EQUAL_TO | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Zendesk`  <a name="cfn-customerprofiles-integration-connectoroperator-zendesk"></a>
The operation to be performed on the provided Zendesk source fields\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ADDITION | DIVISION | GREATER_THAN | MASK_ALL | MASK_FIRST_N | MASK_LAST_N | MULTIPLICATION | NO_OP | PROJECTION | SUBTRACTION | VALIDATE_NON_NEGATIVE | VALIDATE_NON_NULL | VALIDATE_NON_ZERO | VALIDATE_NUMERIC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)