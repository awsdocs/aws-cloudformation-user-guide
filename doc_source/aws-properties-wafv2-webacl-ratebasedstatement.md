# AWS::WAFv2::WebACL RateBasedStatement<a name="aws-properties-wafv2-webacl-ratebasedstatement"></a>

A rate\-based rule counts incoming requests and rate limits requests when they are coming at too fast a rate\. The rule categorizes requests according to your aggregation criteria, collects them into aggregation instances, and counts and rate limits the requests for each instance\. 

You can specify individual aggregation keys, like IP address or HTTP method\. You can also specify aggregation key combinations, like IP address and HTTP method, or HTTP method, query argument, and cookie\. 

Each unique set of values for the aggregation keys that you specify is a separate aggregation instance, with the value from each key contributing to the aggregation instance definition\. 

For example, assume the rule evaluates web requests with the following IP address and HTTP method values: 
+ IP address 10\.1\.1\.1, HTTP method POST
+ IP address 10\.1\.1\.1, HTTP method GET
+ IP address 127\.0\.0\.0, HTTP method POST
+ IP address 10\.1\.1\.1, HTTP method GET

The rule would create different aggregation instances according to your aggregation criteria, for example: 
+ If the aggregation criteria is just the IP address, then each individual address is an aggregation instance, and AWS WAF counts requests separately for each\. The aggregation instances and request counts for our example would be the following: 
  + IP address 10\.1\.1\.1: count 3
  + IP address 127\.0\.0\.0: count 1
+ If the aggregation criteria is HTTP method, then each individual HTTP method is an aggregation instance\. The aggregation instances and request counts for our example would be the following: 
  + HTTP method POST: count 2
  + HTTP method GET: count 2
+ If the aggregation criteria is IP address and HTTP method, then each IP address and each HTTP method would contribute to the combined aggregation instance\. The aggregation instances and request counts for our example would be the following: 
  + IP address 10\.1\.1\.1, HTTP method POST: count 1
  + IP address 10\.1\.1\.1, HTTP method GET: count 2
  + IP address 127\.0\.0\.0, HTTP method POST: count 1

For any n\-tuple of aggregation keys, each unique combination of values for the keys defines a separate aggregation instance, which AWS WAF counts and rate\-limits individually\. 

You can optionally nest another statement inside the rate\-based statement, to narrow the scope of the rule so that it only counts and rate limits requests that match the nested statement\. You can use this nested scope\-down statement in conjunction with your aggregation key specifications or you can just count and rate limit all requests that match the scope\-down statement, without additional aggregation\. When you choose to just manage all requests that match a scope\-down statement, the aggregation instance is singular for the rule\. 

You cannot nest a `RateBasedStatement` inside another statement, for example inside a `NotStatement` or `OrStatement`\. You can define a `RateBasedStatement` inside a web ACL and inside a rule group\. 

For additional information about the options, see [Rate limiting web requests using rate\-based rules](https://docs.aws.amazon.com/waf/latest/developerguide/waf-rate-based-rules.html) in the * AWS WAF Developer Guide*\. 

If you only aggregate on the individual IP address or forwarded IP address, you can retrieve the list of IP addresses that AWS WAF is currently rate limiting for a rule through the API call `GetRateBasedStatementManagedKeys`\. This option is not available for other aggregation configurations\.

 AWS WAF tracks and manages web requests separately for each instance of a rate\-based rule that you use\. For example, if you provide the same rate\-based rule settings in two web ACLs, each of the two rule statements represents a separate instance of the rate\-based rule and gets its own tracking and management by AWS WAF\. If you define a rate\-based rule inside a rule group, and then use that rule group in multiple places, each use creates a separate instance of the rate\-based rule that gets its own tracking and management by AWS WAF\. 

## Syntax<a name="aws-properties-wafv2-webacl-ratebasedstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatement-syntax.json"></a>

```
{
  "[AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatement-aggregatekeytype)" : String,
  "[CustomKeys](#cfn-wafv2-webacl-ratebasedstatement-customkeys)" : [ RateBasedStatementCustomKey, ... ],
  "[ForwardedIPConfig](#cfn-wafv2-webacl-ratebasedstatement-forwardedipconfig)" : ForwardedIPConfiguration,
  "[Limit](#cfn-wafv2-webacl-ratebasedstatement-limit)" : Integer,
  "[ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatement-scopedownstatement)" : Statement
}
```

### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatement-syntax.yaml"></a>

```
  [AggregateKeyType](#cfn-wafv2-webacl-ratebasedstatement-aggregatekeytype): String
  [CustomKeys](#cfn-wafv2-webacl-ratebasedstatement-customkeys): 
    - RateBasedStatementCustomKey
  [ForwardedIPConfig](#cfn-wafv2-webacl-ratebasedstatement-forwardedipconfig): 
    ForwardedIPConfiguration
  [Limit](#cfn-wafv2-webacl-ratebasedstatement-limit): Integer
  [ScopeDownStatement](#cfn-wafv2-webacl-ratebasedstatement-scopedownstatement): 
    Statement
```

## Properties<a name="aws-properties-wafv2-webacl-ratebasedstatement-properties"></a>

`AggregateKeyType`  <a name="cfn-wafv2-webacl-ratebasedstatement-aggregatekeytype"></a>
Setting that indicates how to aggregate the request counts\.   
Web requests that are missing any of the components specified in the aggregation keys are omitted from the rate\-based rule evaluation and handling\. 
+  `CONSTANT` \- Count and limit the requests that match the rate\-based rule's scope\-down statement\. With this option, the counted requests aren't further aggregated\. The scope\-down statement is the only specification used\. When the count of all requests that satisfy the scope\-down statement goes over the limit, AWS WAF applies the rule action to all requests that satisfy the scope\-down statement\. 

  With this option, you must configure the `ScopeDownStatement` property\. 
+  `CUSTOM_KEYS` \- Aggregate the request counts using one or more web request components as the aggregate keys\.

  With this option, you must specify the aggregate keys in the `CustomKeys` property\. 

  To aggregate on only the IP address or only the forwarded IP address, don't use custom keys\. Instead, set the aggregate key type to `IP` or `FORWARDED_IP`\.
+  `FORWARDED_IP` \- Aggregate the request counts on the first IP address in an HTTP header\. 

  With this option, you must specify the header to use in the `ForwardedIPConfig` property\. 

  To aggregate on a combination of the forwarded IP address with other aggregate keys, use `CUSTOM_KEYS`\. 
+  `IP` \- Aggregate the request counts on the IP address from the web request origin\.

  To aggregate on a combination of the IP address with other aggregate keys, use `CUSTOM_KEYS`\. 
*Required*: Yes  
*Type*: String  
*Allowed values*: `CONSTANT | CUSTOM_KEYS | FORWARDED_IP | IP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomKeys`  <a name="cfn-wafv2-webacl-ratebasedstatement-customkeys"></a>
Specifies the aggregate keys to use in a rate\-base rule\.   
*Required*: No  
*Type*: List of [RateBasedStatementCustomKey](aws-properties-wafv2-webacl-ratebasedstatementcustomkey.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ForwardedIPConfig`  <a name="cfn-wafv2-webacl-ratebasedstatement-forwardedipconfig"></a>
The configuration for inspecting IP addresses in an HTTP header that you specify, instead of using the IP address that's reported by the web request origin\. Commonly, this is the X\-Forwarded\-For \(XFF\) header, but you can specify any header name\.   
If the specified header isn't present in the request, AWS WAF doesn't apply the rule to the web request at all\.
This is required if you specify a forwarded IP in the rule's aggregate key settings\.   
*Required*: No  
*Type*: [ForwardedIPConfiguration](aws-properties-wafv2-webacl-forwardedipconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Limit`  <a name="cfn-wafv2-webacl-ratebasedstatement-limit"></a>
The limit on requests per 5\-minute period for a single aggregation instance for the rate\-based rule\. If the rate\-based statement includes a `ScopeDownStatement`, this limit is applied only to the requests that match the statement\.  
Examples:   
+ If you aggregate on just the IP address, this is the limit on requests from any single IP address\. 
+ If you aggregate on the HTTP method and the query argument name "city", then this is the limit on requests for any single method, city pair\. 
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScopeDownStatement`  <a name="cfn-wafv2-webacl-ratebasedstatement-scopedownstatement"></a>
An optional nested statement that narrows the scope of the web requests that are evaluated and managed by the rate\-based statement\. When you use a scope\-down statement, the rate\-based rule only tracks and rate limits requests that match the scope\-down statement\. You can use any nestable [Statement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-webacl-notstatement.html#cfn-wafv2-webacl-notstatement-statement) in the scope\-down statement, and you can nest statements at any level, the same as you can for a rule statement\.   
*Required*: No  
*Type*: [Statement](aws-properties-wafv2-webacl-statement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples"></a>

The following rate\-based rule examples are also listed in a web ACL example, under `AWS::WAFv2::WebACL`\. 

### Rate limit all requests that match a scope\-down statement<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_all_requests_that_match_a_scope-down_statement"></a>

The following example listing shows a rate\-based rule statement that counts and rate limits all requests that match a scope\-down statement\. Rate\-based rules that count all requests together are required to include a scope\-down statement\. In this example, the rule counts all requests coming from a specific country, and limits those requests to 100,000 for any five minute period\.

#### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_all_requests_that_match_a_scope-down_statement--yaml"></a>

```
Rules:
- Name: rbrCountAll
  Priority: 0
  Statement:
    RateBasedStatement:
      Limit: 100000
      AggregateKeyType: CONSTANT
      ScopeDownStatement:
        GeoMatchStatement:
          CountryCodes:
          - GB
          ForwardedIPConfig:
            HeaderName: X-Forwarded-For
            FallbackBehavior: MATCH
  Action:
    Block: {}
  VisibilityConfig:
    SampledRequestsEnabled: true
    CloudWatchMetricsEnabled: true
    MetricName: rbrCountAll
```

#### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_all_requests_that_match_a_scope-down_statement--json"></a>

```
 "Rules": [
    {
      "Name": "rbrCountAll",
      "Priority": 0,
      "Statement": {
        "RateBasedStatement": {
          "Limit": 100000,
          "AggregateKeyType": "CONSTANT",
          "ScopeDownStatement": {
            "GeoMatchStatement": {
              "CountryCodes": [
                "GB"
              ],
              "ForwardedIPConfig": {
                "HeaderName": "X-Forwarded-For",
                "FallbackBehavior": "MATCH"
              }
            }
          }
        }
      },
      "Action": {
        "Block": {}
      },
      "VisibilityConfig": {
        "SampledRequestsEnabled": true,
        "CloudWatchMetricsEnabled": true,
        "MetricName": "rbrCountAll"
      }
    }
 ]
```

### Rate limit requests based on an IP address<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_based_on_an_IP_address"></a>

The following example listing shows a rate\-based rule statement that uses the value in a forwarded IP address to aggregate and rate limit requests\. The forwarded IP address used in this example is the one in the header `X-Forwarded-For`\.

When you rate limit on only the IP address or only a forwarded IP address, you specify the aggregation in the aggregate key type and you don't use custom aggregation keys\. 

#### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_based_on_an_IP_address--yaml"></a>

```
Rules:
- Name: rbrNoCustomKeys
  Priority: 1
  Statement:
    RateBasedStatement:
      Limit: 1000
      AggregateKeyType: FORWARDED_IP
      ForwardedIPConfig:
        HeaderName: X-Forwarded-For
        FallbackBehavior: MATCH
  Action:
    Block: {}
  VisibilityConfig:
    SampledRequestsEnabled: true
    CloudWatchMetricsEnabled: true
    MetricName: rbrNoCustomKeys
```

#### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_based_on_an_IP_address--json"></a>

```
 "Rules": [
    {
      "Name": "rbrNoCustomKeys",
      "Priority": 1,
      "Statement": {
        "RateBasedStatement": {
          "Limit": 1000,
          "AggregateKeyType": "FORWARDED_IP",
          "ForwardedIPConfig": {
            "HeaderName": "X-Forwarded-For",
            "FallbackBehavior": "MATCH"
          }
        }
      },
      "Action": {
        "Block": {}
      },
      "VisibilityConfig": {
        "SampledRequestsEnabled": true,
        "CloudWatchMetricsEnabled": true,
        "MetricName": "rbrNoCustomKeys"
      }
    }
 ]
```

### Rate limit requests based on an IP address and a header<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_based_on_an_IP_address_and_a_header_"></a>

The following example listing shows a rate\-based rule statement that aggregates and rate limits requests based on the paired values of a forwarded IP address and a header\. The IP address used is the one in the header `X-Forwarded-For` and the header value used is in the header `Content-Type`\.

To rate limit using a combination of an IP address with one or more other keys, you provide all key specifications in the custom aggregation key settings\. Anytime you use a forwarded IP address, you specify the header name of the address in the rate\-based statement's `ForwardedIPConfig` setting\. 

#### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_based_on_an_IP_address_and_a_header_--yaml"></a>

```
Rules:
- Name: rbrCustomKeysA
  Priority: 2
  Statement:
    RateBasedStatement:
      Limit: 2000
      AggregateKeyType: CUSTOM_KEYS
      ForwardedIPConfig:
        HeaderName: X-Forwarded-For
        FallbackBehavior: MATCH
      CustomKeys:
      - Header:
          Name: Content-Type
          TextTransformations:
          - Priority: 0
            Type: NONE
      - ForwardedIP: {}
  Action:
    Block: {}
  VisibilityConfig:
    SampledRequestsEnabled: true
    CloudWatchMetricsEnabled: true
    MetricName: rbrCustomKeysA
```

#### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_based_on_an_IP_address_and_a_header_--json"></a>

```
 "Rules": [
    {
      "Name": "rbrCustomKeysA",
      "Priority": 2,
      "Statement": {
        "RateBasedStatement": {
          "Limit": 2000,
          "AggregateKeyType": "CUSTOM_KEYS",
          "ForwardedIPConfig": {
            "HeaderName": "X-Forwarded-For",
            "FallbackBehavior": "MATCH"
          },
          "CustomKeys": [
            {
              "Header": {
                "Name": "Content-Type",
                "TextTransformations": [
                  {
                    "Priority": 0,
                    "Type": "NONE"
                  }
                ]
              }
            },
            {
              "ForwardedIP": {}
            }
          ]
        }
      },
      "Action": {
        "Block": {}
      },
      "VisibilityConfig": {
        "SampledRequestsEnabled": true,
        "CloudWatchMetricsEnabled": true,
        "MetricName": "rbrCustomKeysA"
      }
    }
 ]
```

### Rate limit requests based on three custom aggregate keys<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_based_on_three_custom_aggregate_keys_"></a>

The following example listing shows a rate\-based rule statement that aggregates and rate limits requests based on the trio of values from the query string, the HTTP method, and the URI path\. 

#### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_based_on_three_custom_aggregate_keys_--yaml"></a>

```
Rules:
- Name: rbrCustomKeysB
  Priority: 3
  Statement:
    RateBasedStatement:
      Limit: 3000
      AggregateKeyType: CUSTOM_KEYS
      CustomKeys:
      - QueryString:
          TextTransformations:
          - Priority: 0
            Type: NONE
      - HTTPMethod: {}
      - UriPath:
          TextTransformations:
          - Priority: 0
            Type: NONE
  Action:
    Block: {}
  VisibilityConfig:
    SampledRequestsEnabled: true
    CloudWatchMetricsEnabled: true
    MetricName: rbrCustomKeysB
```

#### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_based_on_three_custom_aggregate_keys_--json"></a>

```
 "Rules": [
    {
      "Name": "rbrCustomKeysB",
      "Priority": 3,
      "Statement": {
        "RateBasedStatement": {
          "Limit": 3000,
          "AggregateKeyType": "CUSTOM_KEYS",
          "CustomKeys": [
            {
              "QueryString": {
                "TextTransformations": [
                  {
                    "Priority": 0,
                    "Type": "NONE"
                  }
                ]
              }
            },
            {
              "HTTPMethod": {}
            },
            {
              "UriPath": {
                "TextTransformations": [
                  {
                    "Priority": 0,
                    "Type": "NONE"
                  }
                ]
              }
            }
          ]
        }
      },
      "Action": {
        "Block": {}
      },
      "VisibilityConfig": {
        "SampledRequestsEnabled": true,
        "CloudWatchMetricsEnabled": true,
        "MetricName": "rbrCustomKeysB"
      }
    }
 ]
```

### Rate limit requests from individual states in a country<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_from_individual_states_in_a_country_"></a>

The following example listing combines a geo match statement with a rate based rule, to limit the number of requests coming from any individual U\.S\. state\. 

The geo match statement matches on all requests coming from the U\.S\. and it has its rule action set to Count\. For all matching requets, the geo match statement adds a country label and a region label, so after being evaluated by this rule, requests from the U\.S\. are labeled by state\. For more information, see the `AWS::WAFv2::WebACL` `GeoMatchStatement` property\. 

Following the geo match statement, the rate\-based rule uses a scope\-down statement to also only match on requests from the U\.S\.\. The rate\-based rule aggregates on values for the geo match region label namespace, so the requests from each state are counted in their own aggregation instance\. The rate\-based rule limits each state to 500 requests in any five minute period\. 

#### YAML<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_from_individual_states_in_a_country_--yaml"></a>

```
Rules:
- Name: labelUSStates
  Priority: 4
  Statement:
    GeoMatchStatement:
      CountryCodes:
      - US
  Action:
    Count: {}
  VisibilityConfig:
    SampledRequestsEnabled: true
    CloudWatchMetricsEnabled: true
    MetricName: labelUSStates
- Name: rbrRequestsFromUSStates
  Priority: 5
  Statement:
    RateBasedStatement:
      Limit: 500
      AggregateKeyType: CUSTOM_KEYS
      ScopeDownStatement:
        GeoMatchStatement:
          CountryCodes:
          - US
      CustomKeys:
      - LabelNamespace:
          Namespace: 'awswaf:clientip:geo:region:'
  Action:
    Block: {}
  VisibilityConfig:
    SampledRequestsEnabled: true
    CloudWatchMetricsEnabled: true
    MetricName: rbrRequestsFromUSStates
```

#### JSON<a name="aws-properties-wafv2-webacl-ratebasedstatement--examples--Rate_limit_requests_from_individual_states_in_a_country_--json"></a>

```
 "Rules": [
    {
      "Name": "labelUSStates",
      "Priority": 4,
      "Statement": {
        "GeoMatchStatement": {
          "CountryCodes": [
            "US"
          ]
        }
      },
      "Action": {
        "Count": {}
      },
      "VisibilityConfig": {
        "SampledRequestsEnabled": true,
        "CloudWatchMetricsEnabled": true,
        "MetricName": "labelUSStates"
      }
    },
    {
      "Name": "rbrRequestsFromUSStates",
      "Priority": 5,
      "Statement": {
        "RateBasedStatement": {
          "Limit": 500,
          "AggregateKeyType": "CUSTOM_KEYS",
          "ScopeDownStatement": {
            "GeoMatchStatement": {
              "CountryCodes": [
                "US"
              ]
            }
          },
          "CustomKeys": [
            {
              "LabelNamespace": {
                "Namespace": "awswaf:clientip:geo:region:"
              }
            }
          ]
        }
      },
      "Action": {
        "Block": {}
      },
      "VisibilityConfig": {
        "SampledRequestsEnabled": true,
        "CloudWatchMetricsEnabled": true,
        "MetricName": "rbrRequestsFromUSStates"
      }
    }
 ]
```