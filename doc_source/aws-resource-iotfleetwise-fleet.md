# AWS::IoTFleetWise::Fleet<a name="aws-resource-iotfleetwise-fleet"></a>

 Creates a fleet that represents a group of vehicles\. 

**Note**  
You must create both a signal catalog and vehicles before you can create a fleet\. 

For more information, see [Fleets](https://docs.aws.amazon.com/iot-fleetwise/latest/developerguide/fleets.html) in the *AWS IoT FleetWise Developer Guide*\.

## Syntax<a name="aws-resource-iotfleetwise-fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotfleetwise-fleet-syntax.json"></a>

```
{
  "Type" : "AWS::IoTFleetWise::Fleet",
  "Properties" : {
      "[Description](#cfn-iotfleetwise-fleet-description)" : String,
      "[Id](#cfn-iotfleetwise-fleet-id)" : String,
      "[SignalCatalogArn](#cfn-iotfleetwise-fleet-signalcatalogarn)" : String,
      "[Tags](#cfn-iotfleetwise-fleet-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotfleetwise-fleet-syntax.yaml"></a>

```
Type: AWS::IoTFleetWise::Fleet
Properties: 
  [Description](#cfn-iotfleetwise-fleet-description): String
  [Id](#cfn-iotfleetwise-fleet-id): String
  [SignalCatalogArn](#cfn-iotfleetwise-fleet-signalcatalogarn): String
  [Tags](#cfn-iotfleetwise-fleet-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotfleetwise-fleet-properties"></a>

`Description`  <a name="cfn-iotfleetwise-fleet-description"></a>
A brief description of the fleet\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[^\u0000-\u001F\u007F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-iotfleetwise-fleet-id"></a>
The unique ID of the fleet\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[a-zA-Z0-9:_-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SignalCatalogArn`  <a name="cfn-iotfleetwise-fleet-signalcatalogarn"></a>
The ARN of the signal catalog associated with the fleet\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iotfleetwise-fleet-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotfleetwise-fleet-return-values"></a>

### Ref<a name="aws-resource-iotfleetwise-fleet-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-iotfleetwise-fleet-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotfleetwise-fleet-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
Property description not available\.

`LastModificationTime`  <a name="LastModificationTime-fn::getatt"></a>
Property description not available\.