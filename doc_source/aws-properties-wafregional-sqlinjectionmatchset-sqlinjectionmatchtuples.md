# AWS WAF Regional SqlInjectionMatchSet SqlInjectionMatchTuples<a name="aws-properties-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples"></a>

`SqlInjectionMatchTuples` is a property of the [AWS::WAFRegional::SqlInjectionMatchSet](aws-resource-wafregional-sqlinjectionmatchset.md) resource that specifies the parts of web requests that AWS WAF inspects for SQL code\.

## Syntax<a name="w3ab2c21c14e2064b5"></a>

### JSON<a name="aws-properties-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples-fieldtomatch)" : Field to match,
  "[TextTransformation](#cfn-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples-texttransformation)" : String
}
```

### YAML<a name="aws-properties-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples-syntax.yaml"></a>

```
[FieldToMatch](#cfn-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples-fieldtomatch):
  Field to match
[TextTransformation](#cfn-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples-texttransformation): String
```

## Properties<a name="w3ab2c21c14e2064b7"></a>

`FieldToMatch`  <a name="cfn-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples-fieldtomatch"></a>
The part of a web request that you want AWS WAF to search, such as a specific header or a query string\.  
*Required*: Yes  
*Type*: [AWS WAF Regional ByteMatchSet ByteMatchTuples FieldToMatch](aws-properties-wafregional-bytematchset-bytematchtuples-fieldtomatch.md)

`TextTransformation`  <a name="cfn-wafregional-sqlinjectionmatchset-sqlinjectionmatchtuples-texttransformation"></a>
Specifies how AWS WAF processes the `FieldToMatch` property before inspecting a request for a match\.  
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass AWS WAF\. If you specify a transformation, AWS WAF transforms the target string value before inspecting a web request for a match\. For valid values, see the `TextTransformation` content for the [SqlInjectionMatchTuple](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_SqlInjectionMatchTuple.html) data type in the *AWS WAF Regional API Reference*\.
*Required*: Yes  
*Type*: String