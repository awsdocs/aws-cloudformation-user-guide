# AWS WAF Regional XssMatchSet XssMatchTuple<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple"></a>

`XssMatchTuple` is a property of the [AWS::WAFRegional::XssMatchSet](aws-resource-wafregional-xssmatchset.md) resource that specifies the part of a web request that you want AWS WAF to inspect for cross\-site scripting attacks\.

## Syntax<a name="w3ab2c21c14e2072b5"></a>

### JSON<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch)" : Field to match,
  "[TextTransformation](#cfn-wafregional-xssmatchset-xssmatchtuple-texttransformation)" : String
}
```

### YAML<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple-syntax.yaml"></a>

```
[FieldToMatch](#cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch):
  Field to match
[TextTransformation](#cfn-wafregional-xssmatchset-xssmatchtuple-texttransformation): String
```

## Properties<a name="w3ab2c21c14e2072b7"></a>

`FieldToMatch`  <a name="cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch"></a>
The part of a web request that you want AWS WAF to search, such as a specific header or a query string\.  
*Required*: Yes  
*Type*: [AWS WAF Regional XssMatchSet XssMatchTuple FieldToMatch](aws-properties-wafregional-xssmatchset-xssmatchtuple-fieldtomatch.md)

`TextTransformation`  <a name="cfn-wafregional-xssmatchset-xssmatchtuple-texttransformation"></a>
Specifies how AWS WAF processes the `FieldToMatch` property before inspecting a request for a match\. Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass AWS WAF\. If you specify a transformation, AWS WAF transforms the`FieldToMatch` parameter before inspecting a web request for a match\.  
For example, AWS WAF can replace white space characters \(such as `\t` and `\n`\) with a single space\. For valid values, see the `TextTransformation` content for the [XssMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_XssMatchTuple.html) data type in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: String