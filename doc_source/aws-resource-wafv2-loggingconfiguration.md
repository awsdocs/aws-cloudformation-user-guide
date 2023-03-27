# AWS::WAFv2::LoggingConfiguration<a name="aws-resource-wafv2-loggingconfiguration"></a>

Defines an association between logging destinations and a web ACL resource, for logging from AWS WAF\. As part of the association, you can specify parts of the standard logging fields to keep out of the logs and you can specify filters so that you log only a subset of the logging records\. 

**Note**  
You can define one logging destination per web ACL\.

You can access information about the traffic that AWS WAF inspects using the following steps:

1. Create your logging destination\. You can use an Amazon CloudWatch Logs log group, an Amazon Simple Storage Service \(Amazon S3\) bucket, or an Amazon Kinesis Data Firehose\. 

   The name that you give the destination must start with `aws-waf-logs-`\. Depending on the type of destination, you might need to configure additional settings or permissions\. 

   For configuration requirements and pricing information for each destination type, see [Logging web ACL traffic](https://docs.aws.amazon.com/waf/latest/developerguide/logging.html) in the * AWS WAF Developer Guide*\.

1. Associate your logging destination to your web ACL using a `PutLoggingConfiguration` request\.

When you successfully enable logging using a `PutLoggingConfiguration` request, AWS WAF creates an additional role or policy that is required to write logs to the logging destination\. For an Amazon CloudWatch Logs log group, AWS WAF creates a resource policy on the log group\. For an Amazon S3 bucket, AWS WAF creates a bucket policy\. For an Amazon Kinesis Data Firehose, AWS WAF creates a service\-linked role\.

For additional information about web ACL logging, see [Logging web ACL traffic information](https://docs.aws.amazon.com/waf/latest/developerguide/logging.html) in the * AWS WAF Developer Guide*\.

## Syntax<a name="aws-resource-wafv2-loggingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafv2-loggingconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::WAFv2::LoggingConfiguration",
  "Properties" : {
      "[LogDestinationConfigs](#cfn-wafv2-loggingconfiguration-logdestinationconfigs)" : [ String, ... ],
      "[LoggingFilter](#cfn-wafv2-loggingconfiguration-loggingfilter)" : LoggingFilter,
      "[RedactedFields](#cfn-wafv2-loggingconfiguration-redactedfields)" : [ FieldToMatch, ... ],
      "[ResourceArn](#cfn-wafv2-loggingconfiguration-resourcearn)" : String
    }
}
```

### YAML<a name="aws-resource-wafv2-loggingconfiguration-syntax.yaml"></a>

```
Type: AWS::WAFv2::LoggingConfiguration
Properties: 
  [LogDestinationConfigs](#cfn-wafv2-loggingconfiguration-logdestinationconfigs): 
    - String
  [LoggingFilter](#cfn-wafv2-loggingconfiguration-loggingfilter): 
    LoggingFilter
  [RedactedFields](#cfn-wafv2-loggingconfiguration-redactedfields): 
    - FieldToMatch
  [ResourceArn](#cfn-wafv2-loggingconfiguration-resourcearn): String
```

## Properties<a name="aws-resource-wafv2-loggingconfiguration-properties"></a>

`LogDestinationConfigs`  <a name="cfn-wafv2-loggingconfiguration-logdestinationconfigs"></a>
The logging destination configuration that you want to associate with the web ACL\.  
You can associate one logging destination to a web ACL\.
*Required*: Yes  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingFilter`  <a name="cfn-wafv2-loggingconfiguration-loggingfilter"></a>
Filtering that specifies which web requests are kept in the logs and which are dropped\. You can filter on the rule action and on the web request labels that were applied by matching rules during web ACL evaluation\.   
*Required*: No  
*Type*: [LoggingFilter](aws-properties-wafv2-loggingconfiguration-loggingfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RedactedFields`  <a name="cfn-wafv2-loggingconfiguration-redactedfields"></a>
The parts of the request that you want to keep out of the logs\. For example, if you redact the `SingleHeader` field, the `HEADER` field in the logs will be `REDACTED`\.   
You can specify only the following fields for redaction: `UriPath`, `QueryString`, `SingleHeader`, `Method`, and `JsonBody`\.
*Required*: No  
*Type*: List of [FieldToMatch](aws-properties-wafv2-loggingconfiguration-fieldtomatch.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceArn`  <a name="cfn-wafv2-loggingconfiguration-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the web ACL that you want to associate with `LogDestinationConfigs`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-wafv2-loggingconfiguration-return-values"></a>

### Ref<a name="aws-resource-wafv2-loggingconfiguration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the web ACL\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-wafv2-loggingconfiguration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-wafv2-loggingconfiguration-return-values-fn--getatt-fn--getatt"></a>

`ManagedByFirewallManager`  <a name="ManagedByFirewallManager-fn::getatt"></a>
Indicates whether the logging configuration was created by AWS Firewall Manager, as part of an AWS WAF policy configuration\. If true, only Firewall Manager can modify or delete the configuration\. 

## Examples<a name="aws-resource-wafv2-loggingconfiguration--examples"></a>



### Create a logging configuration with redacted fields<a name="aws-resource-wafv2-loggingconfiguration--examples--Create_a_logging_configuration_with_redacted_fields"></a>

The following shows an example logging configuration with redacted fields\. 

#### YAML<a name="aws-resource-wafv2-loggingconfiguration--examples--Create_a_logging_configuration_with_redacted_fields--yaml"></a>

```
  LoggingConfiguration:
    Type: AWS::WAFv2::LoggingConfiguration
    Properties:
      ResourceArn: arn:aws:wafv2:us-east-1:123456789000:regional/webacl/test-webaclv2/abcd1234-123b-1234-1234-123456789abc
      LogDestinationConfigs:
      - arn:aws:firehose:us-east-1:123456789000:deliverystream/aws-waf-logs-firehose
      RedactedFields:
      - JsonBody:
          InvalidFallbackBehavior: EVALUATE_AS_STRING
          MatchPattern:
            IncludedPaths:
            - "/path/0/name"
            - "/path/1/name"
          MatchScope: ALL
      - Method: {}
      - QueryString: {}
      - SingleHeader:
          Name: password
      - UriPath: {}
```

#### JSON<a name="aws-resource-wafv2-loggingconfiguration--examples--Create_a_logging_configuration_with_redacted_fields--json"></a>

```
  "LoggingConfiguration": {
    "Type": "AWS::WAFv2::LoggingConfiguration",
    "Properties": {
      "ResourceArn": "arn:aws:wafv2:us-east-1:123456789000:regional/webacl/test-webaclv2/abcd1234-123b-1234-1234-123456789abc",
      "LogDestinationConfigs": [
        "arn:aws:firehose:us-east-1:123456789000:deliverystream/aws-waf-logs-firehose"
      ],
      "RedactedFields": [
      {
        "JsonBody": {
          "InvalidFallbackBehavior": "EVALUATE_AS_STRING",
          "MatchPattern": {
            "IncludedPaths": [
              "/path/0/name",
              "/path/1/name"
            ]
          },
          "MatchScope": "ALL"
        }
      },
      {
        "Method": {}
      },
      {
        "QueryString": {}
      },
      {
        "SingleHeader": {
          "Name": "password"
        }
      },
      {
        "UriPath": {}
      } ]
    }
  }
```

### Create a logging configuration with a filter<a name="aws-resource-wafv2-loggingconfiguration--examples--Create_a_logging_configuration_with_a_filter"></a>

The following shows an example logging configuration with a logging filter\. 

#### YAML<a name="aws-resource-wafv2-loggingconfiguration--examples--Create_a_logging_configuration_with_a_filter--yaml"></a>

```
  LoggingConfiguration:
    Type: AWS::WAFv2::LoggingConfiguration
    Properties:
      ResourceArn: arn:aws:wafv2:us-east-1:123456789000:regional/webacl/test-webaclv2/abcd1234-123b-1234-1234-123456789abc
      LogDestinationConfigs:
      - arn:aws:firehose:us-east-1:123456789000:deliverystream/aws-waf-logs-firehose
      RedactedFields:
      - JsonBody:
          InvalidFallbackBehavior: EVALUATE_AS_STRING
          MatchPattern:
            IncludedPaths:
            - "/path/0/name"
            - "/path/1/name"
          MatchScope: ALL
      - Method: {}
      - QueryString: {}
      - SingleHeader:
          Name: password
      - UriPath: {}
      LoggingFilter:
        DefaultBehavior: KEEP
        Filters:
        - Behavior: KEEP
          Conditions:
          - ActionCondition:
              Action: BLOCK
          - LabelNameCondition:
              LabelName: fooLabel
          Requirement: MEETS_ANY
```

#### JSON<a name="aws-resource-wafv2-loggingconfiguration--examples--Create_a_logging_configuration_with_a_filter--json"></a>

```
  "LoggingConfiguration": {
      "Type": "AWS::WAFv2::LoggingConfiguration",
      "Properties": {
        "ResourceArn": "arn:aws:wafv2:us-east-1:123456789000:regional/webacl/test-webaclv2/abcd1234-123b-1234-1234-123456789abc",
        "LogDestinationConfigs": [
          "arn:aws:firehose:us-east-1:123456789000:deliverystream/aws-waf-logs-firehose"
        ],
        "RedactedFields": [
          {
            "JsonBody": {
              "InvalidFallbackBehavior": "EVALUATE_AS_STRING",
              "MatchPattern": {
                "IncludedPaths": [
                  "/path/0/name",
                  "/path/1/name"
                ]
              },
              "MatchScope": "ALL"
            }
          },
          {
            "Method": {}
          },
          {
            "QueryString": {}
          },
          {
            "SingleHeader": {
              "Name": "password"
            }
          },
          {
            "UriPath": {}
          }
        ],
        "LoggingFilter": {
          "DefaultBehavior": "KEEP",
          "Filters": [
            {
              "Behavior": "KEEP",
              "Conditions": [
                {
                  "ActionCondition": {
                    "Action": "BLOCK"
                  }
                },
                {
                  "LabelNameCondition": {
                    "LabelName": "fooLabel"
                  }
                }
              ],
              "Requirement": "MEETS_ANY"
            }
          ]
        }
      }
    }
```