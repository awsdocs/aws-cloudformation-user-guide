# AWS::CE::AnomalySubscription<a name="aws-resource-ce-anomalysubscription"></a>

 The `AWS::CE::AnomalySubscription` resource is a Cost Explorer resource type that associates a monitor, threshold, and list of subscribers\. It delivers notifications about anomalies detected by a monitor that exceeds a threshold\. The content consists of the detailed metadata and the current status of the `AnomalySubscription` object\. 

## Syntax<a name="aws-resource-ce-anomalysubscription-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ce-anomalysubscription-syntax.json"></a>

```
{
  "Type" : "AWS::CE::AnomalySubscription",
  "Properties" : {
      "[Frequency](#cfn-ce-anomalysubscription-frequency)" : String,
      "[MonitorArnList](#cfn-ce-anomalysubscription-monitorarnlist)" : [ String, ... ],
      "[Subscribers](#cfn-ce-anomalysubscription-subscribers)" : [ Subscriber, ... ],
      "[SubscriptionName](#cfn-ce-anomalysubscription-subscriptionname)" : String,
      "[Threshold](#cfn-ce-anomalysubscription-threshold)" : Double
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
  [Subscribers](#cfn-ce-anomalysubscription-subscribers): 
    - Subscriber
  [SubscriptionName](#cfn-ce-anomalysubscription-subscriptionname): String
  [Threshold](#cfn-ce-anomalysubscription-threshold): Double
```

## Properties<a name="aws-resource-ce-anomalysubscription-properties"></a>

`Frequency`  <a name="cfn-ce-anomalysubscription-frequency"></a>
 The frequency at which anomaly reports are sent over email\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAILY | IMMEDIATE | WEEKLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitorArnList`  <a name="cfn-ce-anomalysubscription-monitorarnlist"></a>
 A list of cost anomaly monitors\.   
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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
 The dollar value that triggers a notification if the threshold is exceeded\.   
*Required*: Yes  
*Type*: Double  
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
          "Ref":"CustomAnomalyMonitorWithLinkedAccount",
          "Ref":"AnomalyServiceMonitor"
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

## See also<a name="aws-resource-ce-anomalysubscription--seealso"></a>
+  [AnomalySubscription](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_AnomalySubscription.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [CreateAnomalySubscription](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_CreateAnomalySubscription.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [DeleteAnomalySubscription](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_DeleteAnomalySubscription.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [GetAnomalySubscriptions](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_GetAnomalySubscriptions.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [UpdateAnomalySubscription](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_UpdateAnomalySubscription.html) in the *AWS Billing and Cost Management API Reference*\. 

