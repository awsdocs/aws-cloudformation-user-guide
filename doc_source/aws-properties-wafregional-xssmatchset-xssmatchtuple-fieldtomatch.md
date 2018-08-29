# AWS WAF Regional XssMatchSet XssMatchTuple FieldToMatch<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple-fieldtomatch"></a>

`FieldToMatch` is a property of the [AWS WAF Regional XssMatchSet XssMatchTuple](aws-properties-wafregional-xssmatchset-xssmatchtuple.md) property that specifies the part of a web request that you want AWS WAF to search, such as a specific header or a query string\.

## Syntax<a name="w3ab2c21c14e2076b5"></a>

### JSON<a name="aws-propertie-wafregional-xssmatchset-xssmatchtuple-fieldtomatch-syntax.json"></a>

```
{
  "[Data](#cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch-data)" : String,
  "[Type](#cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch-type)" : String
}
```

### YAML<a name="aws-properties-wafregional-xssmatchset-xssmatchtuple-fieldtomatch-syntax.yaml"></a>

```
[Data](#cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch-data): String
[Type](#cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch-type): String
```

## Properties<a name="w3ab2c21c14e2076b7"></a>

`Data`  <a name="cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch-data"></a>
If you specify `HEADER` for the `Type` property, the name of the header that AWS WAF searches for, such as `User-Agent` or `Referer`\. If you specify any other value for the `Type` property, do not specify this property\.  
*Required*: Conditional  
*Type*: String

`Type`  <a name="cfn-wafregional-xssmatchset-xssmatchtuple-fieldtomatch-type"></a>
The part of the web request in which AWS WAF searches for the target string\. For valid values, see [FieldToMatch](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_FieldToMatch.html) in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: String