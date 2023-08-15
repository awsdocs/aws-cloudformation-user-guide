# AWS::WAFv2::WebACL FieldIdentifier<a name="aws-properties-wafv2-webacl-fieldidentifier"></a>

The identifier of a field in the web request payload that contains customer data\. 

This data type is used to specify fields in the `RequestInspection` and `RequestInspectionACFP` configurations, which are used in the managed rule group configurations `AWSManagedRulesATPRuleSet` and `AWSManagedRulesACFPRuleSet`, respectively\. 

## Syntax<a name="aws-properties-wafv2-webacl-fieldidentifier-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-fieldidentifier-syntax.json"></a>

```
{
  "[Identifier](#cfn-wafv2-webacl-fieldidentifier-identifier)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-fieldidentifier-syntax.yaml"></a>

```
  [Identifier](#cfn-wafv2-webacl-fieldidentifier-identifier): String
```

## Properties<a name="aws-properties-wafv2-webacl-fieldidentifier-properties"></a>

`Identifier`  <a name="cfn-wafv2-webacl-fieldidentifier-identifier"></a>
The name of the field\.   
When the `PayloadType` in the request inspection is `JSON`, this identifier must be in JSON pointer syntax\. For example `/form/username`\. For information about the JSON Pointer syntax, see the Internet Engineering Task Force \(IETF\) documentation [JavaScript Object Notation \(JSON\) Pointer](https://tools.ietf.org/html/rfc6901)\.   
When the `PayloadType` is `FORM_ENCODED`, use the HTML form names\. For example, `username`\.   
For more information, see the descriptions for each field type in the request inspection properties\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)