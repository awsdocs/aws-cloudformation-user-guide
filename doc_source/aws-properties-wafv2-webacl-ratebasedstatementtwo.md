# AWS::WAFv2::WebACL RateBasedStatementTwo<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo"></a>

Rules statement\. 

## Syntax<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo-syntax.json"></a>

```
{
  "[AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatementtwo-aggregatekeytype)" : String,
  "[Limit](#cfn-wafv2-webacl-ratebasedstatementtwo-limit)" : Integer,
  "[ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatementtwo-scopedownstatement)" : [StatementThree](aws-properties-wafv2-webacl-statementthree.md)
}
```

### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo-syntax.yaml"></a>

```
  [AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatementtwo-aggregatekeytype): String
  [Limit](#cfn-wafv2-webacl-ratebasedstatementtwo-limit): Integer
  [ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatementtwo-scopedownstatement): 
    [StatementThree](aws-properties-wafv2-webacl-statementthree.md)
```

## Properties<a name="aws-properties-wafv2-webacl-ratebasedstatementtwo-properties"></a>

`AggregateKeyType`  <a name="cfn-wafv2-webacl-ratebasedstatementtwo-aggregatekeytype"></a>
Setting that indicates how to aggregate the request counts\. Currently, you must set this to IP\. The request counts are aggregated on IP addresses\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Limit`  <a name="cfn-wafv2-webacl-ratebasedstatementtwo-limit"></a>
Limit on the web request that match any nested statement criteria in any 5 minute period\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScopeDownStatement`  <a name="cfn-wafv2-webacl-ratebasedstatementtwo-scopedownstatement"></a>
Statement nested inside a rate\-based statement to narrow the scope of the requests that AWS WAF counts\.  
*Required*: No  
*Type*: [StatementThree](aws-properties-wafv2-webacl-statementthree.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)