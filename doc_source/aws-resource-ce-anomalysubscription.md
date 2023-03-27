# AWS::CE::AnomalySubscription<a name="aws-resource-ce-anomalysubscription"></a>

The `AWS::CE::AnomalySubscription` resource \(also referred to as an alert subscription\) is a Cost Explorer resource type that sends notifications about specific anomalies that meet an alerting criteria defined by you\.

You can specify the frequency of the alerts and the subscribers to notify\.

Anomaly subscriptions can be associated with one or more [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ce-anomalymonitor.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ce-anomalymonitor.html) resources, and they only send notifications about anomalies detected by those associated monitors\. You can also configure a threshold to further control which anomalies are included in the notifications\.

Anomalies that don’t exceed the chosen threshold and therefore don’t trigger notifications from an anomaly subscription will still be available on the console and from the [https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_GetAnomalies.html](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_GetAnomalies.html) API\.

## Syntax<a name="aws-resource-ce-anomalysubscription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ce-anomalysubscription-syntax.json"></a>

```
{
  "Type" : "AWS::CE::AnomalySubscription",
  "Properties" : {
      "[Frequency](#cfn-ce-anomalysubscription-frequency)" : String,
      "[MonitorArnList](#cfn-ce-anomalysubscription-monitorarnlist)" : [ String, ... ],
      "[ResourceTags](#cfn-ce-anomalysubscription-resourcetags)" : [ ResourceTag, ... ],
      "[Subscribers](#cfn-ce-anomalysubscription-subscribers)" : [ Subscriber, ... ],
      "[SubscriptionName](#cfn-ce-anomalysubscription-subscriptionname)" : String,
      "[Threshold](#cfn-ce-anomalysubscription-threshold)" : Double,
      "[ThresholdExpression](#cfn-ce-anomalysubscription-thresholdexpression)" : String
    }
}
```

### YAML<a name="aws-resource-ce-anomalysubscription-syntax.yaml"></a>

```
Type: AWS::CE::AnomalySubscription
Properties: 
  [Frequency](#cfn-ce-anomalysubscription-frequency): String
  [MonitorArnList](#cfn-ce-anomalysubscription-monitorarnlist): 
    - String
  [ResourceTags](#cfn-ce-anomalysubscription-resourcetags): 
    - ResourceTag
  [Subscribers](#cfn-ce-anomalysubscription-subscribers): 
    - Subscriber
  [SubscriptionName](#cfn-ce-anomalysubscription-subscriptionname): String
  [Threshold](#cfn-ce-anomalysubscription-threshold): Double
  [ThresholdExpression](#cfn-ce-anomalysubscription-thresholdexpression): String
```

## Properties<a name="aws-resource-ce-anomalysubscription-properties"></a>

`Frequency`  <a name="cfn-ce-anomalysubscription-frequency"></a>
The frequency that anomaly notifications are sent\. Notifications are sent either over email \(for DAILY and WEEKLY frequencies\) or SNS \(for IMMEDIATE frequency\)\. For more information, see [Creating an Amazon SNS topic for anomaly notifications](https://docs.aws.amazon.com/cost-management/latest/userguide/ad-SNS.html)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAILY | IMMEDIATE | WEEKLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitorArnList`  <a name="cfn-ce-anomalysubscription-monitorarnlist"></a>
A list of cost anomaly monitors\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTags`  <a name="cfn-ce-anomalysubscription-resourcetags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [ResourceTag](aws-properties-ce-anomalysubscription-resourcetag.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Subscribers`  <a name="cfn-ce-anomalysubscription-subscribers"></a>
A list of subscribers to notify\.   
*Required*: Yes  
*Type*: List of [Subscriber](aws-properties-ce-anomalysubscription-subscriber.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubscriptionName`  <a name="cfn-ce-anomalysubscription-subscriptionname"></a>
The name for the subscription\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Pattern*: `[\S\s]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Threshold`  <a name="cfn-ce-anomalysubscription-threshold"></a>
\(deprecated\)  
An absolute dollar value that must be exceeded by the anomaly's total impact \(see [Impact](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_Impact.html) for more details\) for an anomaly notification to be generated\.  
This field has been deprecated\. To specify a threshold, use ThresholdExpression\. Continued use of Threshold will be treated as shorthand syntax for a ThresholdExpression\.  
One of Threshold or ThresholdExpression is required for `AWS::CE::AnomalySubscription`\. You cannot specify both\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThresholdExpression`  <a name="cfn-ce-anomalysubscription-thresholdexpression"></a>
An [Expression](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_Expression.html) object in JSON string format used to specify the anomalies that you want to generate alerts for\. This supports dimensions and nested expressions\. The supported dimensions are `ANOMALY_TOTAL_IMPACT_ABSOLUTE` and `ANOMALY_TOTAL_IMPACT_PERCENTAGE`, corresponding to an anomaly’s TotalImpact and TotalImpactPercentage, respectively \(see [Impact](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_Impact.html) for more details\)\. The supported nested expression types are `AND` and `OR`\. The match option `GREATER_THAN_OR_EQUAL` is required\. Values must be numbers between 0 and 10,000,000,000 in string format\.  
One of Threshold or ThresholdExpression is required for `AWS::CE::AnomalySubscription`\. You cannot specify both\.  
For further information, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ce-anomalysubscription.html#aws-resource-ce-anomalysubscription--examples) section of this page\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ce-anomalysubscription-return-values"></a>

### Ref<a name="aws-resource-ce-anomalysubscription-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns `SubscriptionArn`\. For example:

            `{ "Ref": "myAnomalyMonitorLogicalName" }`        

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ce-anomalysubscription-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ce-anomalysubscription-return-values-fn--getatt-fn--getatt"></a>

`AccountId`  <a name="AccountId-fn::getatt"></a>
Your unique account identifier\. 

`SubscriptionArn`  <a name="SubscriptionArn-fn::getatt"></a>
The `AnomalySubscription` Amazon Resource Name \(ARN\)\.

## Examples<a name="aws-resource-ce-anomalysubscription--examples"></a>



### Attaching subscriptions to monitors<a name="aws-resource-ce-anomalysubscription--examples--Attaching_subscriptions_to_monitors"></a>

The following example shows two monitors attached to a subscription\.

#### JSON<a name="aws-resource-ce-anomalysubscription--examples--Attaching_subscriptions_to_monitors--json"></a>

```
{
  "Resources": {
    "CustomAnomalyMonitorWithLinkedAccount": {
      "Type": "AWS::CE::AnomalyMonitor",
      "Properties": {
        "MonitorName": "MonitorName",
        "MonitorType": "CUSTOM",
        "MonitorSpecification": " { \"Dimensions\" : { \"Key\" : \"LINKED_ACCOUNT\", \"Values\" : [ \"123456789012\", \"123456789013\" ] } }"
      }
    },
    "AnomalyServiceMonitor": {
      "Type": "AWS::CE::AnomalyMonitor",
      "Properties": {
        "MonitorName": "MonitorName",
        "MonitorType": "DIMENSIONAL",
        "MonitorDimension": "SERVICE"
      }
    },
    "AnomalySubscription": {
      "Type": "AWS::CE::AnomalySubscription",
      "Properties": {
        "SubscriptionName": "SubscriptionName",
        "Threshold": 100,
        "Frequency": "DAILY",
        "MonitorArnList": [
          {"Ref": "CustomAnomalyMonitorWithLinkedAccount"},
          {"Ref": "AnomalyServiceMonitor"}
        ],
        "Subscribers": [
          {
            "Type": "EMAIL",
            "Address": "abc@def.com"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ce-anomalysubscription--examples--Attaching_subscriptions_to_monitors--yaml"></a>

```
Resources:
   CustomAnomalyMonitorWithLinkedAccount:
    Type: 'AWS::CE::AnomalyMonitor'
    Properties:
      MonitorName: "MonitorName"
      MonitorType: "CUSTOM"
      MonitorSpecification: '
            {
              "Dimensions" : {
                "Key" : "LINKED_ACCOUNT",
                "Values" : [ "123456789012", "123456789013" ]
              }
            }' 
            
   AnomalyServiceMonitor:
    Type: 'AWS::CE::AnomalyMonitor'
    Properties:
      MonitorName: 'MonitorName'
      MonitorType: 'DIMENSIONAL'
      MonitorDimension: 'SERVICE' 

   AnomalySubscription:
    Type: 'AWS::CE::AnomalySubscription'
    Properties:
      SubscriptionName: "SubscriptionName"
      Threshold: 100
      Frequency: "DAILY"
      MonitorArnList: [
         !Ref CustomAnomalyMonitorWithLinkedAccount,
         !Ref AnomalyServiceMonitor
      ]
      Subscribers: [
        {
          "Type": "EMAIL",
          "Address": "abc@def.com"
        }
      ]
```

### Using a percentage\-based threshold<a name="aws-resource-ce-anomalysubscription--examples--Using_a_percentage-based_threshold"></a>

The following example creates a subscription using a percentage\-based threshold\.

#### JSON<a name="aws-resource-ce-anomalysubscription--examples--Using_a_percentage-based_threshold--json"></a>

```
{
  "Resources": {
    "AnomalySubscription": {
      "Type": "AWS::CE::AnomalySubscription",
      "Properties": {
        "SubscriptionName": "SubscriptionName",
        "ThresholdExpression": "{ \"Dimensions\": { \"Key\": \"ANOMALY_TOTAL_IMPACT_PERCENTAGE\", \"Values\": [ \"100\" ], \"MatchOptions\": [ \"GREATER_THAN_OR_EQUAL\" ] } }",
        "MonitorArnList": [],
        "Subscribers": [
          {
            "Address": "abc@def.com",
            "Type": "EMAIL"
          }
        ],
        "Frequency": "DAILY"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ce-anomalysubscription--examples--Using_a_percentage-based_threshold--yaml"></a>

```
Resources:
   AnomalySubscription:
    Type: 'AWS::CE::AnomalySubscription'
    Properties:
      SubscriptionName: "Subscription 1"
      ThresholdExpression: '{
        "Dimensions": {
          "Key": "ANOMALY_TOTAL_IMPACT_PERCENTAGE",
          "MatchOptions": [ "GREATER_THAN_OR_EQUAL" ],
          "Values": [ "100" ]
        }
      }'
      Frequency: "DAILY"
      MonitorArnList: [ ]
      Subscribers: [
        {
          "Type": "EMAIL",
          "Address": "abc@def.com"
        }
      ]
```

### Using a percentage\-based threshold and absolute threshold combined with AND<a name="aws-resource-ce-anomalysubscription--examples--Using_a_percentage-based_threshold_and_absolute_threshold_combined_with_AND"></a>

The following example creates a subscription using a percentage\-based threshold and absolute threshold combined with AND\.

#### JSON<a name="aws-resource-ce-anomalysubscription--examples--Using_a_percentage-based_threshold_and_absolute_threshold_combined_with_AND--json"></a>

```
{
  "Resources": {
    "AnomalySubscription": {
      "Type": "AWS::CE::AnomalySubscription",
      "Properties": {
        "SubscriptionName": "SubscriptionName",
        "ThresholdExpression": "{ \"And\": [ { \"Dimensions\": { \"Key\": \"ANOMALY_TOTAL_IMPACT_PERCENTAGE\", \"MatchOptions\": [ \"GREATER_THAN_OR_EQUAL\" ], \"Values\": [ \"100\" ] } }, { \"Dimensions\": { \"Key\": \"ANOMALY_TOTAL_IMPACT_ABSOLUTE\", \"MatchOptions\": [ \"GREATER_THAN_OR_EQUAL\" ], \"Values\": [ \"200\" ] } } ] }",
        "MonitorArnList": [],
        "Subscribers": [
          {
            "Address": "abc@def.com",
            "Type": "EMAIL"
          }
        ],
        "Frequency": "DAILY"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ce-anomalysubscription--examples--Using_a_percentage-based_threshold_and_absolute_threshold_combined_with_AND--yaml"></a>

```
Resources:
  AnomalySubscription:
    Type: 'AWS::CE::AnomalySubscription'
    Properties:
      SubscriptionName: "SubscriptionName"
      ThresholdExpression: '{
        "And": [
          {
            "Dimensions": {
              "Key": "ANOMALY_TOTAL_IMPACT_PERCENTAGE",
              "MatchOptions": [ "GREATER_THAN_OR_EQUAL" ],
              "Values": [ "100" ]
            }
          },
          {
            "Dimensions": {
              "Key": "ANOMALY_TOTAL_IMPACT_ABSOLUTE",
              "MatchOptions": [ "GREATER_THAN_OR_EQUAL" ],
              "Values": [ "200" ]
            }
          }
        ]
      }'
      Frequency: "DAILY"
      MonitorArnList: [ ]
      Subscribers: [
        {
          "Type": "EMAIL",
          "Address": "abc@def.com"
        }
      ]
```

### Using a percentage\-based threshold and absolute threshold combined with OR<a name="aws-resource-ce-anomalysubscription--examples--Using_a_percentage-based_threshold_and_absolute_threshold_combined_with_OR"></a>

The following example creates a subscription using a percentage\-based threshold and absolute threshold combined with OR\.

#### JSON<a name="aws-resource-ce-anomalysubscription--examples--Using_a_percentage-based_threshold_and_absolute_threshold_combined_with_OR--json"></a>

```
{
  "Resources": {
    "AnomalySubscription": {
      "Type": "AWS::CE::AnomalySubscription",
      "Properties": {
        "SubscriptionName": "SubscriptionName",
        "ThresholdExpression": "{ \"Or\": [ { \"Dimensions\": { \"Key\": \"ANOMALY_TOTAL_IMPACT_PERCENTAGE\", \"MatchOptions\": [ \"GREATER_THAN_OR_EQUAL\" ], \"Values\": [ \"100\" ] } }, { \"Dimensions\": { \"Key\": \"ANOMALY_TOTAL_IMPACT_ABSOLUTE\", \"MatchOptions\": [ \"GREATER_THAN_OR_EQUAL\" ], \"Values\": [ \"200\" ] } } ] }",
        "MonitorArnList": [],
        "Subscribers": [
          {
            "Address": "abc@def.com",
            "Type": "EMAIL"
          }
        ],
        "Frequency": "DAILY"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ce-anomalysubscription--examples--Using_a_percentage-based_threshold_and_absolute_threshold_combined_with_OR--yaml"></a>

```
Resources:
  AnomalySubscription:
    Type: 'AWS::CE::AnomalySubscription'
    Properties:
      SubscriptionName: "SubscriptionName"
      ThresholdExpression: '{
        "Or": [
          {
            "Dimensions": {
              "Key": "ANOMALY_TOTAL_IMPACT_PERCENTAGE",
              "MatchOptions": [ "GREATER_THAN_OR_EQUAL" ],
              "Values": [ "100" ]
            }
          },
          {
            "Dimensions": {
              "Key": "ANOMALY_TOTAL_IMPACT_ABSOLUTE",
              "MatchOptions": [ "GREATER_THAN_OR_EQUAL" ],
              "Values": [ "200" ]
            }
          }
        ]
      }'
      Frequency: "DAILY"
      MonitorArnList: [ ]
      Subscribers: [
        {
          "Type": "EMAIL",
          "Address": "abc@def.com"
        }
      ]
```

## See also<a name="aws-resource-ce-anomalysubscription--seealso"></a>
+  [AnomalySubscription](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_AnomalySubscription.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [CreateAnomalySubscription](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_CreateAnomalySubscription.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [DeleteAnomalySubscription](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_DeleteAnomalySubscription.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [GetAnomalySubscriptions](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_GetAnomalySubscriptions.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [UpdateAnomalySubscription](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_UpdateAnomalySubscription.html) in the *AWS Billing and Cost Management API Reference*\. 

