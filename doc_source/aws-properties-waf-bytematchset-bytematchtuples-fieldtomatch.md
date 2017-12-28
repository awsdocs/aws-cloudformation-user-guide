# AWS WAF ByteMatchSet ByteMatchTuples FieldToMatch<a name="aws-properties-waf-bytematchset-bytematchtuples-fieldtomatch"></a>

`FieldToMatch` is a property of the [AWS WAF ByteMatchSet ByteMatchTuples](aws-properties-waf-bytematchset-bytematchtuples.md) property that specifies the part of a web request that you want AWS WAF to search, such as a specific header or a query string\.

## Syntax<a name="w3ab2c21c14e1633b5"></a>

### JSON<a name="aws-properties-waf-bytematchset-bytematchtuples-fieldtomatch-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-bytematchset-bytematchtuples-fieldtomatch-data)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-bytematchset-bytematchtuples-fieldtomatch-type)" : String
}
```

### YAML<a name="aws-properties-waf-bytematchset-bytematchtuples-fieldtomatch-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-bytematchset-bytematchtuples-fieldtomatch-data): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-waf-bytematchset-bytematchtuples-fieldtomatch-type): String
```

## Properties<a name="w3ab2c21c14e1633b7"></a>

`Data`  
If you specify `HEADER` for the `Type` property, the name of the header that AWS WAF searches for, such as `User-Agent` or `Referer`\. If you specify any other value for the `Type` property, do not specify this property\.  
*Required: *Conditional  
*Type*: String

`Type`  
The part of the web request in which AWS WAF searches for the target string\. For valid values, see [FieldToMatch](http://docs.aws.amazon.com/waf/latest/APIReference/API_FieldToMatch.html) in the *AWS WAF API Reference*\.  
*Required: *Yes  
*Type*: String