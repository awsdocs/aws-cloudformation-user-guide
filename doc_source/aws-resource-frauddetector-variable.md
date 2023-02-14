# AWS::FraudDetector::Variable<a name="aws-resource-frauddetector-variable"></a>

Manages a variable\.

## Syntax<a name="aws-resource-frauddetector-variable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-frauddetector-variable-syntax.json"></a>

```
{
  "Type" : "AWS::FraudDetector::Variable",
  "Properties" : {
      "[DataSource](#cfn-frauddetector-variable-datasource)" : String,
      "[DataType](#cfn-frauddetector-variable-datatype)" : String,
      "[DefaultValue](#cfn-frauddetector-variable-defaultvalue)" : String,
      "[Description](#cfn-frauddetector-variable-description)" : String,
      "[Name](#cfn-frauddetector-variable-name)" : String,
      "[Tags](#cfn-frauddetector-variable-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VariableType](#cfn-frauddetector-variable-variabletype)" : String
    }
}
```

### YAML<a name="aws-resource-frauddetector-variable-syntax.yaml"></a>

```
Type: AWS::FraudDetector::Variable
Properties: 
  [DataSource](#cfn-frauddetector-variable-datasource): String
  [DataType](#cfn-frauddetector-variable-datatype): String
  [DefaultValue](#cfn-frauddetector-variable-defaultvalue): String
  [Description](#cfn-frauddetector-variable-description): String
  [Name](#cfn-frauddetector-variable-name): String
  [Tags](#cfn-frauddetector-variable-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VariableType](#cfn-frauddetector-variable-variabletype): String
```

## Properties<a name="aws-resource-frauddetector-variable-properties"></a>

`DataSource`  <a name="cfn-frauddetector-variable-datasource"></a>
The data source of the variable\.  
Valid values: `EVENT | EXTERNAL_MODEL_SCORE`  
When defining a variable within a detector, you can only use the `EVENT` value for DataSource when the *Inline* property is set to true\. If the *Inline* property is set false, you can use either `EVENT` or `MODEL_SCORE` for DataSource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataType`  <a name="cfn-frauddetector-variable-datatype"></a>
The data type of the variable\.  
Valid data types: `STRING | INTEGER | BOOLEAN | FLOAT`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultValue`  <a name="cfn-frauddetector-variable-defaultvalue"></a>
The default value of the variable\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-frauddetector-variable-description"></a>
The description of the variable\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-frauddetector-variable-name"></a>
The name of the variable\.  
Pattern: `^[0-9a-z_-]+$`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-frauddetector-variable-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VariableType`  <a name="cfn-frauddetector-variable-variabletype"></a>
The type of the variable\. For more information see [Variable types](https://docs.aws.amazon.com/frauddetector/latest/ug/create-a-variable.html#variable-types)\.  
Valid Values: `AUTH_CODE | AVS | BILLING_ADDRESS_L1 | BILLING_ADDRESS_L2 | BILLING_CITY | BILLING_COUNTRY | BILLING_NAME | BILLING_PHONE | BILLING_STATE | BILLING_ZIP | CARD_BIN | CATEGORICAL | CURRENCY_CODE | EMAIL_ADDRESS | FINGERPRINT | FRAUD_LABEL | FREE_FORM_TEXT | IP_ADDRESS | NUMERIC | ORDER_ID | PAYMENT_TYPE | PHONE_NUMBER | PRICE | PRODUCT_CATEGORY | SHIPPING_ADDRESS_L1 | SHIPPING_ADDRESS_L2 | SHIPPING_CITY | SHIPPING_COUNTRY | SHIPPING_NAME | SHIPPING_PHONE | SHIPPING_STATE | SHIPPING_ZIP | USERAGENT `   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-frauddetector-variable-return-values"></a>

### Ref<a name="aws-resource-frauddetector-variable-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the primary identifier for the resource, which is the ARN\.

Example: `{ "Ref": "arn:aws:frauddetector:us-west-2:123123123123:outcome/outcome_name"}`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-frauddetector-variable-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-frauddetector-variable-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the variable\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Timestamp of when variable was created\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Timestamp of when variable was last updated\.

## See also<a name="aws-resource-frauddetector-variable--seealso"></a>
+ [CreateVariable](https://docs.aws.amazon.com/frauddetector/latest/api/API_CreateVariable.html) in the *Amazon Fraud Detector API Reference*
+ [Create a variable](https://docs.aws.amazon.com/frauddetector/latest/ug/create-a-variable.html) in the *Amazon Fraud Detector User Guide*