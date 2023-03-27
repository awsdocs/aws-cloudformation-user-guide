# AWS::IoTFleetWise::Campaign CollectionScheme<a name="aws-properties-iotfleetwise-campaign-collectionscheme"></a>

Specifies what data to collect and how often or when to collect it\.

## Syntax<a name="aws-properties-iotfleetwise-campaign-collectionscheme-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-campaign-collectionscheme-syntax.json"></a>

```
{
  "[ConditionBasedCollectionScheme](#cfn-iotfleetwise-campaign-collectionscheme-conditionbasedcollectionscheme)" : ConditionBasedCollectionScheme,
  "[TimeBasedCollectionScheme](#cfn-iotfleetwise-campaign-collectionscheme-timebasedcollectionscheme)" : TimeBasedCollectionScheme
}
```

### YAML<a name="aws-properties-iotfleetwise-campaign-collectionscheme-syntax.yaml"></a>

```
  [ConditionBasedCollectionScheme](#cfn-iotfleetwise-campaign-collectionscheme-conditionbasedcollectionscheme): 
    ConditionBasedCollectionScheme
  [TimeBasedCollectionScheme](#cfn-iotfleetwise-campaign-collectionscheme-timebasedcollectionscheme): 
    TimeBasedCollectionScheme
```

## Properties<a name="aws-properties-iotfleetwise-campaign-collectionscheme-properties"></a>

`ConditionBasedCollectionScheme`  <a name="cfn-iotfleetwise-campaign-collectionscheme-conditionbasedcollectionscheme"></a>
Information about a collection scheme that uses a simple logical expression to recognize what data to collect\.  
*Required*: No  
*Type*: [ConditionBasedCollectionScheme](aws-properties-iotfleetwise-campaign-conditionbasedcollectionscheme.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TimeBasedCollectionScheme`  <a name="cfn-iotfleetwise-campaign-collectionscheme-timebasedcollectionscheme"></a>
Information about a collection scheme that uses a time period to decide how often to collect data\.  
*Required*: No  
*Type*: [TimeBasedCollectionScheme](aws-properties-iotfleetwise-campaign-timebasedcollectionscheme.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)