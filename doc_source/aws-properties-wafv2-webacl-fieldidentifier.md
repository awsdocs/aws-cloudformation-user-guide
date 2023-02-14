# AWS::WAFv2::WebACL FieldIdentifier<a name="aws-properties-wafv2-webacl-fieldidentifier"></a>

The identifier of the username or password field, used in the `ManagedRuleGroupConfig` settings\. 

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
The name of the username or password field, used in the `ManagedRuleGroupConfig` settings\.   
When the `PayloadType` is `JSON`, the identifier must be in JSON pointer syntax\. For example `/form/username`\. For information about the JSON Pointer syntax, see the Internet Engineering Task Force \(IETF\) documentation [JavaScript Object Notation \(JSON\) Pointer](https://tools.ietf.org/html/rfc6901)\.   
When the `PayloadType` is `FORM_ENCODED`, use the HTML form names\. For example, `username`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)