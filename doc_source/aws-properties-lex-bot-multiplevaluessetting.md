# AWS::Lex::Bot MultipleValuesSetting<a name="aws-properties-lex-bot-multiplevaluessetting"></a>

Indicates whether a slot can return multiple values\.

## Syntax<a name="aws-properties-lex-bot-multiplevaluessetting-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lex-bot-multiplevaluessetting-syntax.json"></a>

```
{
  "[AllowMultipleValues](#cfn-lex-bot-multiplevaluessetting-allowmultiplevalues)" : Boolean
}
```

### YAML<a name="aws-properties-lex-bot-multiplevaluessetting-syntax.yaml"></a>

```
  [AllowMultipleValues](#cfn-lex-bot-multiplevaluessetting-allowmultiplevalues): Boolean
```

## Properties<a name="aws-properties-lex-bot-multiplevaluessetting-properties"></a>

`AllowMultipleValues`  <a name="cfn-lex-bot-multiplevaluessetting-allowmultiplevalues"></a>
Indicates whether a slot can return multiple values\. When `true`, the slot may return more than one value in a response\. When `false`, the slot returns only a single value\.  
Multi\-value slots are only available in the en\-US locale\. If you set this value to `true` in any other locale, Amazon Lex throws a `ValidationException`\.  
If the `allowMutlipleValues` is not set, the default value is `false`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)