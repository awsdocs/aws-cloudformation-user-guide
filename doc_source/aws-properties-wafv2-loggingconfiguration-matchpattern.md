# AWS::WAFv2::LoggingConfiguration MatchPattern<a name="aws-properties-wafv2-loggingconfiguration-matchpattern"></a>

The patterns to look for in the JSON body\. AWS WAF inspects the results of these pattern matches against the rule inspection criteria\. 

## Syntax<a name="aws-properties-wafv2-loggingconfiguration-matchpattern-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-loggingconfiguration-matchpattern-syntax.json"></a>

```
{
  "[All](#cfn-wafv2-loggingconfiguration-matchpattern-all)" : Json,
  "[IncludedPaths](#cfn-wafv2-loggingconfiguration-matchpattern-includedpaths)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-wafv2-loggingconfiguration-matchpattern-syntax.yaml"></a>

```
  [All](#cfn-wafv2-loggingconfiguration-matchpattern-all): Json
  [IncludedPaths](#cfn-wafv2-loggingconfiguration-matchpattern-includedpaths): 
    - String
```

## Properties<a name="aws-properties-wafv2-loggingconfiguration-matchpattern-properties"></a>

`All`  <a name="cfn-wafv2-loggingconfiguration-matchpattern-all"></a>
Match all of the elements\.   
You must specify either this setting or the `IncludedPaths` setting, but not both\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludedPaths`  <a name="cfn-wafv2-loggingconfiguration-matchpattern-includedpaths"></a>
Match only the specified include paths\.   
Provide the include paths using JSON Pointer syntax\. For example, `"IncludedPaths": ["/dogs/0/name", "/dogs/1/name"]`\. For information about this syntax, see the Internet Engineering Task Force \(IETF\) documentation [JavaScript Object Notation \(JSON\) Pointer](https://tools.ietf.org/html/rfc6901)\.   
You must specify either this setting or the `All` setting, but not both\.  
Don't use this option to include all paths\. Instead, use the `All` setting\. 
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)