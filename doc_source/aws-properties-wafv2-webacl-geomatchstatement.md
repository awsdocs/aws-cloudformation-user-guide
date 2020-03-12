# AWS::WAFv2::WebACL GeoMatchStatement<a name="aws-properties-wafv2-webacl-geomatchstatement"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

A rule statement used to identify web requests based on country of origin\. 

## Syntax<a name="aws-properties-wafv2-webacl-geomatchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-geomatchstatement-syntax.json"></a>

```
{
  "[CountryCodes](#cfn-wafv2-webacl-geomatchstatement-countrycodes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-geomatchstatement-syntax.yaml"></a>

```
  [CountryCodes](#cfn-wafv2-webacl-geomatchstatement-countrycodes): 
    - String
```

## Properties<a name="aws-properties-wafv2-webacl-geomatchstatement-properties"></a>

`CountryCodes`  <a name="cfn-wafv2-webacl-geomatchstatement-countrycodes"></a>
An array of two\-character country codes, for example, `[ "US", "CN" ]`, from the alpha\-2 country ISO codes of the ISO 3166 international standard\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)