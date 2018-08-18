# AWS WAF Regional ByteMatchSet ByteMatchTuples<a name="aws-properties-wafregional-bytematchset-bytematchtuples"></a>

`ByteMatchTuples` is a property of the [AWS::WAFRegional::ByteMatchSet](aws-resource-wafregional-bytematchset.md) resource that specifies settings for an AWS WAF Regional `ByteMatchSet` resource, such as the bytes \(typically a string that corresponds with ASCII characters\) that you want AWS WAF to search for in web requests\.

## Syntax<a name="w3ab2c21c14e2040b5"></a>

### JSON<a name="aws-properties-wafregional-bytematchset-bytematchtuples-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafregional-bytematchset-bytematchtuples-fieldtomatch)" : Field to match,
  "[PositionalConstraint](#cfn-wafregional-bytematchset-bytematchtuples-positionalconstraint)" : String,
  "[TargetString](#cfn-wafregional-bytematchset-bytematchtuples-targetstring)" : String,
  "[TargetStringBase64](#cfn-wafregional-bytematchset-bytematchtuples-targetstringbase64)" : String,
  "[TextTransformation](#cfn-wafregional-bytematchset-bytematchtuples-texttransformation)" : String
}
```

### YAML<a name="aws-properties-wafregional-bytematchset-bytematchtuples-syntax.yaml"></a>

```
[FieldToMatch](#cfn-wafregional-bytematchset-bytematchtuples-fieldtomatch):
  Field to match
[PositionalConstraint](#cfn-wafregional-bytematchset-bytematchtuples-positionalconstraint): String
[TargetString](#cfn-wafregional-bytematchset-bytematchtuples-targetstring): String
[TargetStringBase64](#cfn-wafregional-bytematchset-bytematchtuples-targetstringbase64): String
[TextTransformation](#cfn-wafregional-bytematchset-bytematchtuples-texttransformation): String
```

## Properties<a name="w3ab2c21c14e2040b7"></a>

`FieldToMatch`  <a name="cfn-wafregional-bytematchset-bytematchtuples-fieldtomatch"></a>
The part of a web request that you want AWS WAF to search, such as a specific header or a query string\.  
*Required*: Yes  
*Type*: [AWS WAF Regional ByteMatchSet ByteMatchTuples FieldToMatch](aws-properties-wafregional-bytematchset-bytematchtuples-fieldtomatch.md)

`PositionalConstraint`  <a name="cfn-wafregional-bytematchset-bytematchtuples-positionalconstraint"></a>
How AWS WAF finds matches within the part of the web request in which you are searching\. For valid values, see the `PositionalConstraint` content for the [ByteMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_ByteMatchTuple.html) data type in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: String

`TargetString`  <a name="cfn-wafregional-bytematchset-bytematchtuples-targetstring"></a>
The value that AWS WAF searches for\. AWS CloudFormation encodes in base64 this value before sending it to AWS WAF\.  
AWS WAF searches for this value in a specific part of web requests, which you define in the `FieldToMatch` property\.  
Valid values depend on the `Type` value in the `FieldToMatch` property\. For example, for a `METHOD` type, you must specify HTTP methods, such as `DELETE, GET, HEAD, OPTIONS, PATCH, POST,` and `PUT`\. For more information, see the `TargetString` content for the [ByteMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_ByteMatchTuple.html) data type in the *AWS WAF Regional API Reference*\.  
*Required*: Conditional\. You must specify this property or the `TargetStringBase64` property\.  
*Type*: String

`TargetStringBase64`  <a name="cfn-wafregional-bytematchset-bytematchtuples-targetstringbase64"></a>
The base64\-encoded value that AWS WAF searches for\. AWS CloudFormation sends this value to AWS WAF without encoding it\.  
AWS WAF searches for this value in a specific part of web requests, which you define in the `FieldToMatch` property\.  
Valid values depend on the `Type` value in the `FieldToMatch` property\. For example, for a `METHOD` type, you must specify HTTP methods, such as `DELETE, GET, HEAD, OPTIONS, PATCH, POST,` and `PUT`\. For more information, see the `TargetString` content for the [ByteMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_ByteMatchTuple.html) data type in the *AWS WAF Regional API Reference*\.  
*Required*: Conditional\. You must specify this property or the `TargetString` property\.  
*Type*: String

`TextTransformation`  <a name="cfn-wafregional-bytematchset-bytematchtuples-texttransformation"></a>
Specifies how AWS WAF processes the target string value\. Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass AWS WAF\. If you specify a transformation, AWS WAF transforms the target string value before inspecting a web request for a match\.  
For example, AWS WAF can replace whitespace characters \(such as `\t` and `\n`\) with a single space\. For valid values, see the `TextTransformation` content for the [ByteMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_ByteMatchTuple.html) data type in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: String