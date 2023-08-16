# AWS::Connect::Rule Reference<a name="aws-properties-connect-rule-reference"></a>

Information about the reference when the `referenceType` is `URL`\. Otherwise, null\. \(Supports variable injection in the `Value` field\.\)

## Syntax<a name="aws-properties-connect-rule-reference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-rule-reference-syntax.json"></a>

```
{
  "[Type](#cfn-connect-rule-reference-type)" : String,
  "[Value](#cfn-connect-rule-reference-value)" : String
}
```

### YAML<a name="aws-properties-connect-rule-reference-syntax.yaml"></a>

```
  [Type](#cfn-connect-rule-reference-type): String
  [Value](#cfn-connect-rule-reference-value): String
```

## Properties<a name="aws-properties-connect-rule-reference-properties"></a>

`Type`  <a name="cfn-connect-rule-reference-type"></a>
The type of the reference\. `DATE` must be of type Epoch timestamp\.   
*Allowed values*: `URL` \| `ATTACHMENT` \| `NUMBER` \| `STRING` \| `DATE` \| `EMAIL`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-connect-rule-reference-value"></a>
 A valid value for the reference\. For example, for a URL reference, a formatted URL that is displayed to an agent in the Contact Control Panel \(CCP\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)