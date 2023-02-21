# AWS::IoTFleetWise::Campaign<a name="aws-resource-iotfleetwise-campaign"></a>

Creates an orchestration of data collection rules\. The AWS IoT FleetWise Edge Agent software running in vehicles uses campaigns to decide how to collect and transfer data to the cloud\. You create campaigns in the cloud\. After you or your team approve campaigns, AWS IoT FleetWise automatically deploys them to vehicles\. 

For more information, see [Collect and transfer data with campaigns](https://docs.aws.amazon.com/iot-fleetwise/latest/developerguide/campaigns.html) in the *AWS IoT FleetWise Developer Guide*\.

## Syntax<a name="aws-resource-iotfleetwise-campaign-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotfleetwise-campaign-syntax.json"></a>

```
{
  "Type" : "AWS::IoTFleetWise::Campaign",
  "Properties" : {
      "[Action](#cfn-iotfleetwise-campaign-action)" : String,
      "[CollectionScheme](#cfn-iotfleetwise-campaign-collectionscheme)" : CollectionScheme,
      "[Compression](#cfn-iotfleetwise-campaign-compression)" : String,
      "[DataExtraDimensions](#cfn-iotfleetwise-campaign-dataextradimensions)" : [ String, ... ],
      "[Description](#cfn-iotfleetwise-campaign-description)" : String,
      "[DiagnosticsMode](#cfn-iotfleetwise-campaign-diagnosticsmode)" : String,
      "[ExpiryTime](#cfn-iotfleetwise-campaign-expirytime)" : String,
      "[Name](#cfn-iotfleetwise-campaign-name)" : String,
      "[PostTriggerCollectionDuration](#cfn-iotfleetwise-campaign-posttriggercollectionduration)" : Double,
      "[Priority](#cfn-iotfleetwise-campaign-priority)" : Integer,
      "[SignalCatalogArn](#cfn-iotfleetwise-campaign-signalcatalogarn)" : String,
      "[SignalsToCollect](#cfn-iotfleetwise-campaign-signalstocollect)" : [ SignalInformation, ... ],
      "[SpoolingMode](#cfn-iotfleetwise-campaign-spoolingmode)" : String,
      "[StartTime](#cfn-iotfleetwise-campaign-starttime)" : String,
      "[Tags](#cfn-iotfleetwise-campaign-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetArn](#cfn-iotfleetwise-campaign-targetarn)" : String
    }
}
```

### YAML<a name="aws-resource-iotfleetwise-campaign-syntax.yaml"></a>

```
Type: AWS::IoTFleetWise::Campaign
Properties: 
  [Action](#cfn-iotfleetwise-campaign-action): String
  [CollectionScheme](#cfn-iotfleetwise-campaign-collectionscheme): 
    CollectionScheme
  [Compression](#cfn-iotfleetwise-campaign-compression): String
  [DataExtraDimensions](#cfn-iotfleetwise-campaign-dataextradimensions): 
    - String
  [Description](#cfn-iotfleetwise-campaign-description): String
  [DiagnosticsMode](#cfn-iotfleetwise-campaign-diagnosticsmode): String
  [ExpiryTime](#cfn-iotfleetwise-campaign-expirytime): String
  [Name](#cfn-iotfleetwise-campaign-name): String
  [PostTriggerCollectionDuration](#cfn-iotfleetwise-campaign-posttriggercollectionduration): Double
  [Priority](#cfn-iotfleetwise-campaign-priority): Integer
  [SignalCatalogArn](#cfn-iotfleetwise-campaign-signalcatalogarn): String
  [SignalsToCollect](#cfn-iotfleetwise-campaign-signalstocollect): 
    - SignalInformation
  [SpoolingMode](#cfn-iotfleetwise-campaign-spoolingmode): String
  [StartTime](#cfn-iotfleetwise-campaign-starttime): String
  [Tags](#cfn-iotfleetwise-campaign-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetArn](#cfn-iotfleetwise-campaign-targetarn): String
```

## Properties<a name="aws-resource-iotfleetwise-campaign-properties"></a>

`Action`  <a name="cfn-iotfleetwise-campaign-action"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CollectionScheme`  <a name="cfn-iotfleetwise-campaign-collectionscheme"></a>
Property description not available\.  
*Required*: Yes  
*Type*: [CollectionScheme](aws-properties-iotfleetwise-campaign-collectionscheme.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Compression`  <a name="cfn-iotfleetwise-campaign-compression"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataExtraDimensions`  <a name="cfn-iotfleetwise-campaign-dataextradimensions"></a>
Property description not available\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iotfleetwise-campaign-description"></a>
The description of the campaign\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[^\u0000-\u001F\u007F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DiagnosticsMode`  <a name="cfn-iotfleetwise-campaign-diagnosticsmode"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExpiryTime`  <a name="cfn-iotfleetwise-campaign-expirytime"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-iotfleetwise-campaign-name"></a>
The name of a campaign\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[a-zA-Z\d\-_:]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PostTriggerCollectionDuration`  <a name="cfn-iotfleetwise-campaign-posttriggercollectionduration"></a>
Property description not available\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Priority`  <a name="cfn-iotfleetwise-campaign-priority"></a>
Property description not available\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SignalCatalogArn`  <a name="cfn-iotfleetwise-campaign-signalcatalogarn"></a>
The ARN of the signal catalog associated with the campaign\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SignalsToCollect`  <a name="cfn-iotfleetwise-campaign-signalstocollect"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [SignalInformation](aws-properties-iotfleetwise-campaign-signalinformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpoolingMode`  <a name="cfn-iotfleetwise-campaign-spoolingmode"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StartTime`  <a name="cfn-iotfleetwise-campaign-starttime"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iotfleetwise-campaign-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-iotfleetwise-campaign-targetarn"></a>
The ARN of a vehicle or fleet to which the campaign is deployed\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iotfleetwise-campaign-return-values"></a>

### Ref<a name="aws-resource-iotfleetwise-campaign-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-iotfleetwise-campaign-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotfleetwise-campaign-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
Property description not available\.

`LastModificationTime`  <a name="LastModificationTime-fn::getatt"></a>
Property description not available\.

`Status`  <a name="Status-fn::getatt"></a>
Property description not available\.