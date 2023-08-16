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
      "[DataDestinationConfigs](#cfn-iotfleetwise-campaign-datadestinationconfigs)" : [ DataDestinationConfig, ... ],
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
  [DataDestinationConfigs](#cfn-iotfleetwise-campaign-datadestinationconfigs): 
    - DataDestinationConfig
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
 Specifies how to update a campaign\. The action can be one of the following:  
+  `APPROVE` \- To approve delivering a data collection scheme to vehicles\. 
+  `SUSPEND` \- To suspend collecting signal data\. The campaign is deleted from vehicles and all vehicles in the suspended campaign will stop sending data\.
+  `RESUME` \- To reactivate the `SUSPEND` campaign\. The campaign is redeployed to all vehicles and the vehicles will resume sending data\.
+  `UPDATE` \- To update a campaign\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `APPROVE | RESUME | SUSPEND | UPDATE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CollectionScheme`  <a name="cfn-iotfleetwise-campaign-collectionscheme"></a>
 The data collection scheme associated with the campaign\. You can specify a scheme that collects data based on time or an event\.  
*Required*: Yes  
*Type*: [CollectionScheme](aws-properties-iotfleetwise-campaign-collectionscheme.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Compression`  <a name="cfn-iotfleetwise-campaign-compression"></a>
 \(Optional\) Whether to compress signals before transmitting data to AWS IoT FleetWise\. If you don't want to compress the signals, use `OFF`\. If it's not specified, `SNAPPY` is used\.   
Default: `SNAPPY`  
*Required*: No  
*Type*: String  
*Allowed values*: `OFF | SNAPPY`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataDestinationConfigs`  <a name="cfn-iotfleetwise-campaign-datadestinationconfigs"></a>
\(Optional\) The destination where the campaign sends data\. You can choose to send data to be stored in Amazon S3 or Amazon Timestream\.  
Amazon S3 optimizes the cost of data storage and provides additional mechanisms to use vehicle data, such as data lakes, centralized data storage, data processing pipelines, and analytics\. AWS IoT FleetWise supports at\-least\-once file delivery to S3\. Your vehicle data is stored on multiple AWS IoT FleetWise servers for redundancy and high availability\.  
You can use Amazon Timestream to access and analyze time series data, and Timestream to query vehicle data so that you can identify trends and patterns\.  
*Required*: No  
*Type*: List of [DataDestinationConfig](aws-properties-iotfleetwise-campaign-datadestinationconfig.md)  
*Maximum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataExtraDimensions`  <a name="cfn-iotfleetwise-campaign-dataextradimensions"></a>
 \(Optional\) A list of vehicle attributes to associate with a campaign\.   
Enrich the data with specified vehicle attributes\. For example, add `make` and `model` to the campaign, and AWS IoT FleetWise will associate the data with those attributes as dimensions in Amazon Timestream\. You can then query the data against `make` and `model`\.  
Default: An empty array  
*Required*: No  
*Type*: List of String  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iotfleetwise-campaign-description"></a>
\(Optional\) The description of the campaign\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[^\u0000-\u001F\u007F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DiagnosticsMode`  <a name="cfn-iotfleetwise-campaign-diagnosticsmode"></a>
 \(Optional\) Option for a vehicle to send diagnostic trouble codes to AWS IoT FleetWise\. If you want to send diagnostic trouble codes, use `SEND_ACTIVE_DTCS`\. If it's not specified, `OFF` is used\.  
Default: `OFF`  
*Required*: No  
*Type*: String  
*Allowed values*: `OFF | SEND_ACTIVE_DTCS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExpiryTime`  <a name="cfn-iotfleetwise-campaign-expirytime"></a>
 \(Optional\) The time the campaign expires, in seconds since epoch \(January 1, 1970 at midnight UTC time\)\. Vehicle data isn't collected after the campaign expires\.   
Default: 253402214400 \(December 31, 9999, 00:00:00 UTC\)  
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
 \(Optional\) How long \(in milliseconds\) to collect raw data after a triggering event initiates the collection\. If it's not specified, `0` is used\.  
Default: `0`  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Priority`  <a name="cfn-iotfleetwise-campaign-priority"></a>
\(Optional\) A number indicating the priority of one campaign over another campaign for a certain vehicle or fleet\. A campaign with the lowest value is deployed to vehicles before any other campaigns\. If it's not specified, `0` is used\.   
Default: `0`  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SignalCatalogArn`  <a name="cfn-iotfleetwise-campaign-signalcatalogarn"></a>
The Amazon Resource Name \(ARN\) of the signal catalog associated with the campaign\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SignalsToCollect`  <a name="cfn-iotfleetwise-campaign-signalstocollect"></a>
\(Optional\) A list of information about signals to collect\.   
*Required*: No  
*Type*: List of [SignalInformation](aws-properties-iotfleetwise-campaign-signalinformation.md)  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpoolingMode`  <a name="cfn-iotfleetwise-campaign-spoolingmode"></a>
\(Optional\) Whether to store collected data after a vehicle lost a connection with the cloud\. After a connection is re\-established, the data is automatically forwarded to AWS IoT FleetWise\. If you want to store collected data when a vehicle loses connection with the cloud, use `TO_DISK`\. If it's not specified, `OFF` is used\.  
Default: `OFF`  
*Required*: No  
*Type*: String  
*Allowed values*: `OFF | TO_DISK`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StartTime`  <a name="cfn-iotfleetwise-campaign-starttime"></a>
\(Optional\) The time, in milliseconds, to deliver a campaign after it was approved\. If it's not specified, `0` is used\.  
Default: `0`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iotfleetwise-campaign-tags"></a>
\(Optional\) Metadata that can be used to manage the campaign\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-iotfleetwise-campaign-targetarn"></a>
The Amazon Resource Name \(ARN\) of a vehicle or fleet to which the campaign is deployed\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iotfleetwise-campaign-return-values"></a>

### Ref<a name="aws-resource-iotfleetwise-campaign-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the Name\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-iotfleetwise-campaign-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iotfleetwise-campaign-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the campaign\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
 The time the campaign was created in seconds since epoch \(January 1, 1970 at midnight UTC time\)\. 

`LastModificationTime`  <a name="LastModificationTime-fn::getatt"></a>
The last time the campaign was modified\.

`Status`  <a name="Status-fn::getatt"></a>
The state of the campaign\. The status can be one of: `CREATING`, `WAITING_FOR_APPROVAL`, `RUNNING`, and `SUSPENDED`\. 