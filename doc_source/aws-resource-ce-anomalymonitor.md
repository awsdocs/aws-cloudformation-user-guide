# AWS::CE::AnomalyMonitor<a name="aws-resource-ce-anomalymonitor"></a>

 The `AWS::CE::AnomalyMonitor` resource is a Cost Explorer resource type that continuously inspects your account's cost data for anomalies, based on `MonitorType` and `MonitorSpecification`\. The content consists of detailed metadata and the current status of the monitor object\. 

## Syntax<a name="aws-resource-ce-anomalymonitor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ce-anomalymonitor-syntax.json"></a>

```
{
  "Type" : "AWS::CE::AnomalyMonitor",
  "Properties" : {
      "[MonitorDimension](#cfn-ce-anomalymonitor-monitordimension)" : String,
      "[MonitorName](#cfn-ce-anomalymonitor-monitorname)" : String,
      "[MonitorSpecification](#cfn-ce-anomalymonitor-monitorspecification)" : String,
      "[MonitorType](#cfn-ce-anomalymonitor-monitortype)" : String,
      "[ResourceTags](#cfn-ce-anomalymonitor-resourcetags)" : [ ResourceTag, ... ]
    }
}
```

### YAML<a name="aws-resource-ce-anomalymonitor-syntax.yaml"></a>

```
Type: AWS::CE::AnomalyMonitor
Properties: 
  [MonitorDimension](#cfn-ce-anomalymonitor-monitordimension): String
  [MonitorName](#cfn-ce-anomalymonitor-monitorname): String
  [MonitorSpecification](#cfn-ce-anomalymonitor-monitorspecification): String
  [MonitorType](#cfn-ce-anomalymonitor-monitortype): String
  [ResourceTags](#cfn-ce-anomalymonitor-resourcetags): 
    - ResourceTag
```

## Properties<a name="aws-resource-ce-anomalymonitor-properties"></a>

`MonitorDimension`  <a name="cfn-ce-anomalymonitor-monitordimension"></a>
The dimensions to evaluate\.   
*Required*: No  
*Type*: String  
*Allowed values*: `SERVICE`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MonitorName`  <a name="cfn-ce-anomalymonitor-monitorname"></a>
The name of the monitor\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Pattern*: `[\S\s]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MonitorSpecification`  <a name="cfn-ce-anomalymonitor-monitorspecification"></a>
The array of `MonitorSpecification` in JSON array format\. For instance, you can use `MonitorSpecification` to specify a tag, Cost Category, or linked account for your custom anomaly monitor\. For further information, see the [Examples](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ce-anomalymonitor.html#aws-resource-ce-anomalymonitor--examples) section of this page\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MonitorType`  <a name="cfn-ce-anomalymonitor-monitortype"></a>
The possible type values\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `CUSTOM | DIMENSIONAL`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceTags`  <a name="cfn-ce-anomalymonitor-resourcetags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [ResourceTag](aws-properties-ce-anomalymonitor-resourcetag.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ce-anomalymonitor-return-values"></a>

### Ref<a name="aws-resource-ce-anomalymonitor-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns `MonitorArn`\. For example:

            `{ "Ref": "myAnomalySubscriptionLogicalName" }`        

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ce-anomalymonitor-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ce-anomalymonitor-return-values-fn--getatt-fn--getatt"></a>

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
The date when the monitor was created\.

`DimensionalValueCount`  <a name="DimensionalValueCount-fn::getatt"></a>
The value for evaluated dimensions\. 

`LastEvaluatedDate`  <a name="LastEvaluatedDate-fn::getatt"></a>
The date when the monitor last evaluated for anomalies\. 

`LastUpdatedDate`  <a name="LastUpdatedDate-fn::getatt"></a>
The date when the monitor was last updated\.

`MonitorArn`  <a name="MonitorArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) value for the monitor\. 

## Examples<a name="aws-resource-ce-anomalymonitor--examples"></a>



### Service monitor<a name="aws-resource-ce-anomalymonitor--examples--Service_monitor_"></a>

The following example creates a service anomaly monitor\.

#### JSON<a name="aws-resource-ce-anomalymonitor--examples--Service_monitor_--json"></a>

```
{
  "Resources": {
    "AnomalyServiceMonitor": {
      "Type": "AWS::CE::AnomalyMonitor",
      "Properties": {
        "MonitorName": "MonitorName",
        "MonitorType": "DIMENSIONAL",
        "MonitorDimension": "SERVICE"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ce-anomalymonitor--examples--Service_monitor_--yaml"></a>

```
Resources:
  AnomalyServiceMonitor:
    Type: 'AWS::CE::AnomalyMonitor'
    Properties:
      MonitorName: 'MonitorName'
      MonitorType: 'DIMENSIONAL'
      MonitorDimension: 'SERVICE'
```

### Anomaly monitor with tags<a name="aws-resource-ce-anomalymonitor--examples--Anomaly_monitor_with_tags"></a>

The following example creates a custom anomaly monitor with tags\.

#### JSON<a name="aws-resource-ce-anomalymonitor--examples--Anomaly_monitor_with_tags--json"></a>

```
{
  "Resources": {
    "CustomAnomalyMonitorWithTags": {
      "Type": "AWS::CE::AnomalyMonitor",
      "Properties": {
        "MonitorName": "MonitorName",
        "MonitorType": "CUSTOM",
        "MonitorSpecification": " { \"Tags\" : { \"Key\" : \"Tag Key\", \"Values\" : [ \"TagValue1\", \"TagValue2\" ] } }"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ce-anomalymonitor--examples--Anomaly_monitor_with_tags--yaml"></a>

```
Resources:
  CustomAnomalyMonitorWithTags:
    Type: 'AWS::CE::AnomalyMonitor'
    Properties:
      MonitorName: "MonitorName"
      MonitorType: "CUSTOM"
      MonitorSpecification: '
            {
              "Tags" : {
                "Key" : "Tag Key",
                "Values" : [ "TagValue1", "TagValue2" ]
              }
            }'
```

### Anomaly monitor with Cost Category<a name="aws-resource-ce-anomalymonitor--examples--Anomaly_monitor_with_Cost_Category"></a>

The following example creates a custom anomaly monitor with a Cost Category\.

#### JSON<a name="aws-resource-ce-anomalymonitor--examples--Anomaly_monitor_with_Cost_Category--json"></a>

```
{
  "Resources": {
    "CustomAnomalyMonitorWithCC": {
      "Type": "AWS::CE::AnomalyMonitor",
      "Properties": {
        "MonitorName": "MonitorName",
        "MonitorType": "CUSTOM",
        "MonitorSpecification": " { \"CostCategories\" : { \"Key\" : \"CostCategoryKey\", \"Values\" : [ \"CostCategoryValue\" ] } }"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ce-anomalymonitor--examples--Anomaly_monitor_with_Cost_Category--yaml"></a>

```
Resources:
   CustomAnomalyMonitorWithCC:
    Type: 'AWS::CE::AnomalyMonitor'
    Properties:
      MonitorName: "MonitorName"
      MonitorType: "CUSTOM"
      MonitorSpecification: '
            {
              "CostCategories" : {
                "Key" : "CostCategoryKey",
                "Values" : [ "CostCategoryValue" ]
              }
            }'
```

### Anomaly monitor with linked account<a name="aws-resource-ce-anomalymonitor--examples--Anomaly_monitor_with_linked_account"></a>

The following example creates a custom anomaly monitor with a linked account\.

#### JSON<a name="aws-resource-ce-anomalymonitor--examples--Anomaly_monitor_with_linked_account--json"></a>

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
    }
  }
}
```

#### YAML<a name="aws-resource-ce-anomalymonitor--examples--Anomaly_monitor_with_linked_account--yaml"></a>

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
```

### Attaching subscriptions to monitors<a name="aws-resource-ce-anomalymonitor--examples--Attaching_subscriptions_to_monitors_"></a>

The following example shows two anomaly monitors attached to an anomaly subscription\.

#### JSON<a name="aws-resource-ce-anomalymonitor--examples--Attaching_subscriptions_to_monitors_--json"></a>

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
         { “Ref”: "CustomAnomalyMonitorWithLinkedAccount"},
         { "Ref": "AnomalyServiceMonitor"}
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

#### YAML<a name="aws-resource-ce-anomalymonitor--examples--Attaching_subscriptions_to_monitors_--yaml"></a>

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

## See also<a name="aws-resource-ce-anomalymonitor--seealso"></a>
+  [AnomalyMonitor](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_AnomalyMonitor.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [CreateAnomalyMonitor](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_CreateAnomalyMonitor.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [DeleteAnomalyMonitor](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_DeleteAnomalyMonitor.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [GetAnomalyMonitors](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_GetAnomalyMonitors.html) in the *AWS Billing and Cost Management API Reference*\. 
+  [UpdateAnomalyMonitor](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_UpdateAnomalyMonitor.html) in the *AWS Billing and Cost Management API Reference*\. 

