# AWS::IoT::FleetMetric<a name="aws-resource-iot-fleetmetric"></a>

Use the `AWS::IoT::FleetMetric` resource to declare a fleet metric\.

## Syntax<a name="aws-resource-iot-fleetmetric-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-fleetmetric-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::FleetMetric",
  "Properties" : {
      "[AggregationField](#cfn-iot-fleetmetric-aggregationfield)" : String,
      "[AggregationType](#cfn-iot-fleetmetric-aggregationtype)" : AggregationType,
      "[Description](#cfn-iot-fleetmetric-description)" : String,
      "[IndexName](#cfn-iot-fleetmetric-indexname)" : String,
      "[MetricName](#cfn-iot-fleetmetric-metricname)" : String,
      "[Period](#cfn-iot-fleetmetric-period)" : Integer,
      "[QueryString](#cfn-iot-fleetmetric-querystring)" : String,
      "[QueryVersion](#cfn-iot-fleetmetric-queryversion)" : String,
      "[Tags](#cfn-iot-fleetmetric-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Unit](#cfn-iot-fleetmetric-unit)" : String
    }
}
```

### YAML<a name="aws-resource-iot-fleetmetric-syntax.yaml"></a>

```
Type: AWS::IoT::FleetMetric
Properties: 
  [AggregationField](#cfn-iot-fleetmetric-aggregationfield): String
  [AggregationType](#cfn-iot-fleetmetric-aggregationtype): 
    AggregationType
  [Description](#cfn-iot-fleetmetric-description): String
  [IndexName](#cfn-iot-fleetmetric-indexname): String
  [MetricName](#cfn-iot-fleetmetric-metricname): String
  [Period](#cfn-iot-fleetmetric-period): Integer
  [QueryString](#cfn-iot-fleetmetric-querystring): 
    String
  [QueryVersion](#cfn-iot-fleetmetric-queryversion): String
  [Tags](#cfn-iot-fleetmetric-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Unit](#cfn-iot-fleetmetric-unit): String
```

## Properties<a name="aws-resource-iot-fleetmetric-properties"></a>

`AggregationField`  <a name="cfn-iot-fleetmetric-aggregationfield"></a>
The field to aggregate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AggregationType`  <a name="cfn-iot-fleetmetric-aggregationtype"></a>
The type of the aggregation query\.  
*Required*: No  
*Type*: [AggregationType](aws-properties-iot-fleetmetric-aggregationtype.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iot-fleetmetric-description"></a>
The fleet metric description\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IndexName`  <a name="cfn-iot-fleetmetric-indexname"></a>
The name of the index to search\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-iot-fleetmetric-metricname"></a>
The name of the fleet metric to create\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Period`  <a name="cfn-iot-fleetmetric-period"></a>
The time in seconds between fleet metric emissions\. Range \[60\(1 min\), 86400\(1 day\)\] and must be multiple of 60\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryString`  <a name="cfn-iot-fleetmetric-querystring"></a>
The search query string\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryVersion`  <a name="cfn-iot-fleetmetric-queryversion"></a>
The query version\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iot-fleetmetric-tags"></a>
Metadata which can be used to manage the fleet metric\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Unit`  <a name="cfn-iot-fleetmetric-unit"></a>
Used to support unit transformation such as milliseconds to seconds\. Must be a unit supported by CW metric\. Default to null\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-fleetmetric-return-values"></a>

### Ref<a name="aws-resource-iot-fleetmetric-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the fleet metric name\.

### Fn::GetAtt<a name="aws-resource-iot-fleetmetric-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-fleetmetric-return-values-fn--getatt-fn--getatt"></a>

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
The time the fleet metric was created\.

`LastModifiedDate`  <a name="LastModifiedDate-fn::getatt"></a>
The time the fleet metric was last modified\.

`MetricArn`  <a name="MetricArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the fleet metric\.

`Version`  <a name="Version-fn::getatt"></a>
The fleet metric version\.