# AWS WAF ByteMatchSet ByteMatchTuples<a name="aws-properties-waf-bytematchset-bytematchtuples"></a>

`ByteMatchTuples` is a property of the [AWS::WAF::ByteMatchSet](aws-resource-waf-bytematchset.md) resource that specifies settings for an AWS WAF `ByteMatchSet` resource, such as the bytes \(typically a string that corresponds with ASCII characters\) that you want AWS WAF to search for in web requests\.

## Syntax<a name="w3ab2c21c14e1991b5"></a>

### JSON<a name="aws-properties-waf-bytematchset-bytematchtuples-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-waf-bytematchset-bytematchtuples-fieldtomatch)" : Field to match,
  "[PositionalConstraint](#cfn-waf-bytematchset-bytematchtuples-positionalconstraint)" : String,
  "[TargetString](#cfn-waf-bytematchset-bytematchtuples-targetstring)" : String,
  "[TargetStringBase64](#cfn-waf-bytematchset-bytematchtuples-targetstringbase64)" : String,
  "[TextTransformation](#cfn-waf-bytematchset-bytematchtuples-texttransformation)" : String
}
```

### YAML<a name="aws-properties-waf-bytematchset-bytematchtuples-syntax.yaml"></a>

```
[FieldToMatch](#cfn-waf-bytematchset-bytematchtuples-fieldtomatch):
  Field to match
[PositionalConstraint](#cfn-waf-bytematchset-bytematchtuples-positionalconstraint): String
[TargetString](#cfn-waf-bytematchset-bytematchtuples-targetstring): String
[TargetStringBase64](#cfn-waf-bytematchset-bytematchtuples-targetstringbase64): String
[TextTransformation](#cfn-waf-bytematchset-bytematchtuples-texttransformation): String
```

## Properties<a name="w3ab2c21c14e1991b7"></a>

`FieldToMatch`  <a name="cfn-waf-bytematchset-bytematchtuples-fieldtomatch"></a>
The part of a web request that you want AWS WAF to search, such as a specific header or a query string\.  
*Required*: Yes  
*Type*: [AWS WAF ByteMatchSet ByteMatchTuples FieldToMatch](aws-properties-waf-bytematchset-bytematchtuples-fieldtomatch.md)

`PositionalConstraint`  <a name="cfn-waf-bytematchset-bytematchtuples-positionalconstraint"></a>
How AWS WAF finds matches within the web request part in which you are searching\. For valid values, see the `PositionalConstraint` content for the [ByteMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_ByteMatchTuple.html) data type in the *AWS WAF API Reference*\.  
*Required*: Yes  
*Type*: String

`TargetString`  <a name="cfn-waf-bytematchset-bytematchtuples-targetstring"></a>
The value that AWS WAF searches for\. AWS CloudFormation base64 encodes this value before sending it to AWS WAF\.  
AWS WAF searches for this value in a specific part of web requests, which you define in the `FieldToMatch` property\.  
Valid values depend on the `Type` value in the `FieldToMatch` property\. For example, for a `METHOD` type, you must specify HTTP methods such as `DELETE, GET, HEAD, OPTIONS, PATCH, POST,` and `PUT`\. For more information, see the `TargetString` content for the [ByteMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_ByteMatchTuple.html) data type in the *AWS WAF API Reference*\.  
*Required*: Conditional\. You must specify this property or the `TargetStringBase64` property\.  
*Type*: String

`TargetStringBase64`  <a name="cfn-waf-bytematchset-bytematchtuples-targetstringbase64"></a>
The base64\-encoded value that AWS WAF searches for\. AWS CloudFormation sends this value to AWS WAF without encoding it\.  
AWS WAF searches for this value in a specific part of web requests, which you define in the `FieldToMatch` property\.  
Valid values depend on the `Type` value in the `FieldToMatch` property\. For example, for a `METHOD` type, you must specify HTTP methods such as `DELETE, GET, HEAD, OPTIONS, PATCH, POST,` and `PUT`\. For more information, see the `TargetString` content for the [ByteMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_ByteMatchTuple.html) data type in the *AWS WAF API Reference*\.  
*Required*: Conditional\. You must specify this property or the `TargetString` property\.  
*Type*: String

`TextTransformation`  <a name="cfn-waf-bytematchset-bytematchtuples-texttransformation"></a>
Specifies how AWS WAF processes the target string value\. Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass AWS WAF\. If you specify a transformation, AWS WAF transforms the target string value before inspecting a web request for a match\.  
For example, AWS WAF can replace whitespace characters \(such as `\t` and `\n`\) with a single space\. For valid values, see the `TextTransformation` content for the [ByteMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_ByteMatchTuple.html) data type in the *AWS WAF API Reference*\.  
*Required*: Yes  
*Type*: String