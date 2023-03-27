# AWS::IoTFleetWise::ModelManifest<a name="aws-resource-iotfleetwise-modelmanifest"></a>

 Creates a vehicle model \(model manifest\) that specifies signals \(attributes, branches, sensors, and actuators\)\. 

For more information, see [Vehicle models](https://docs.aws.amazon.com/iot-fleetwise/latest/developerguide/vehicle-models.html) in the *AWS IoT FleetWise Developer Guide*\.

## Syntax<a name="aws-resource-iotfleetwise-modelmanifest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotfleetwise-modelmanifest-syntax.json"></a>

```
{
  "Type" : "AWS::IoTFleetWise::ModelManifest",
  "Properties" : {
      "[Description](#cfn-iotfleetwise-modelmanifest-description)" : String,
      "[Name](#cfn-iotfleetwise-modelmanifest-name)" : String,
      "[Nodes](#cfn-iotfleetwise-modelmanifest-nodes)" : [ String, ... ],
      "[SignalCatalogArn](#cfn-iotfleetwise-modelmanifest-signalcatalogarn)" : String,
      "[Status](#cfn-iotfleetwise-modelmanifest-status)" : String,
      "[Tags](#cfn-iotfleetwise-modelmanifest-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotfleetwise-modelmanifest-syntax.yaml"></a>

```
Type: AWS::IoTFleetWise::ModelManifest
Properties: 
  [Description](#cfn-iotfleetwise-modelmanifest-description): String
  [Name](#cfn-iotfleetwise-modelmanifest-name): String
  [Nodes](#cfn-iotfleetwise-modelmanifest-nodes): 
    - String
  [SignalCatalogArn](#cfn-iotfleetwise-modelmanifest-signalcatalogarn): String
  [Status](#cfn-iotfleetwise-modelmanifest-status): String
  [Tags](#cfn-iotfleetwise-modelmanifest-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotfleetwise-modelmanifest-properties"></a>

`Description`  <a name="cfn-iotfleetwise-modelmanifest-description"></a>
A brief description of the vehicle model\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[^\u0000-\u001F\u007F]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotfleetwise-modelmanifest-name"></a>
The name of the vehicle model\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Nodes`  <a name="cfn-iotfleetwise-modelmanifest-nodes"></a>
Property description not available\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SignalCatalogArn`  <a name="cfn-iotfleetwise-modelmanifest-signalcatalogarn"></a>
The ARN of the signal catalog associated with the vehicle model\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-iotfleetwise-modelmanifest-status"></a>
The state of the vehicle model\. If the status is `ACTIVE`, the vehicle model can't be edited\. If the status is `DRAFT`, you can edit the vehicle model\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ACTIVE | DRAFT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotfleetwise-modelmanifest-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotfleetwise-modelmanifest-return-values"></a>

### Ref<a name="aws-resource-iotfleetwise-modelmanifest-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-iotfleetwise-modelmanifest-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotfleetwise-modelmanifest-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
Property description not available\.

`LastModificationTime`  <a name="LastModificationTime-fn::getatt"></a>
Property description not available\.