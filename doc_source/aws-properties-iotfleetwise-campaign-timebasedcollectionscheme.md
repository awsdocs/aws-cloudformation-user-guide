# AWS::IoTFleetWise::Campaign TimeBasedCollectionScheme<a name="aws-properties-iotfleetwise-campaign-timebasedcollectionscheme"></a>

Information about a collection scheme that uses a time period to decide how often to collect data\.

## Syntax<a name="aws-properties-iotfleetwise-campaign-timebasedcollectionscheme-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-campaign-timebasedcollectionscheme-syntax.json"></a>

```
{
  "[PeriodMs](#cfn-iotfleetwise-campaign-timebasedcollectionscheme-periodms)" : Double
}
```

### YAML<a name="aws-properties-iotfleetwise-campaign-timebasedcollectionscheme-syntax.yaml"></a>

```
  [PeriodMs](#cfn-iotfleetwise-campaign-timebasedcollectionscheme-periodms): Double
```

## Properties<a name="aws-properties-iotfleetwise-campaign-timebasedcollectionscheme-properties"></a>

`PeriodMs`  <a name="cfn-iotfleetwise-campaign-timebasedcollectionscheme-periodms"></a>
The time period \(in milliseconds\) to decide how often to collect data\. For example, if the time period is `60000`, the Edge Agent software collects data once every minute\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)