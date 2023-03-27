# AWS::IoTFleetWise::Vehicle<a name="aws-resource-iotfleetwise-vehicle"></a>

 Creates a vehicle, which is an instance of a vehicle model \(model manifest\)\. Vehicles created from the same vehicle model consist of the same signals inherited from the vehicle model\.

**Note**  
 If you have an existing AWS IoT Thing, you can use AWS IoT FleetWise to create a vehicle and collect data from your thing\. 

For more information, see [Create a vehicle \(CLI\)](https://docs.aws.amazon.com/iot-fleetwise/latest/developerguide/create-vehicle-cli.html) in the *AWS IoT FleetWise Developer Guide*\.

## Syntax<a name="aws-resource-iotfleetwise-vehicle-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotfleetwise-vehicle-syntax.json"></a>

```
{
  "Type" : "AWS::IoTFleetWise::Vehicle",
  "Properties" : {
      "[AssociationBehavior](#cfn-iotfleetwise-vehicle-associationbehavior)" : String,
      "[Attributes](#cfn-iotfleetwise-vehicle-attributes)" : {Key : Value, ...},
      "[DecoderManifestArn](#cfn-iotfleetwise-vehicle-decodermanifestarn)" : String,
      "[ModelManifestArn](#cfn-iotfleetwise-vehicle-modelmanifestarn)" : String,
      "[Name](#cfn-iotfleetwise-vehicle-name)" : String,
      "[Tags](#cfn-iotfleetwise-vehicle-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotfleetwise-vehicle-syntax.yaml"></a>

```
Type: AWS::IoTFleetWise::Vehicle
Properties: 
  [AssociationBehavior](#cfn-iotfleetwise-vehicle-associationbehavior): String
  [Attributes](#cfn-iotfleetwise-vehicle-attributes): 
    Key : Value
  [DecoderManifestArn](#cfn-iotfleetwise-vehicle-decodermanifestarn): String
  [ModelManifestArn](#cfn-iotfleetwise-vehicle-modelmanifestarn): String
  [Name](#cfn-iotfleetwise-vehicle-name): String
  [Tags](#cfn-iotfleetwise-vehicle-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotfleetwise-vehicle-properties"></a>

`AssociationBehavior`  <a name="cfn-iotfleetwise-vehicle-associationbehavior"></a>
An option to create a new AWS IoT thing when creating a vehicle, or to validate an existing thing as a vehicle\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CreateIotThing | ValidateIotThingExists`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Attributes`  <a name="cfn-iotfleetwise-vehicle-attributes"></a>
Static information about a vehicle in a key\-value pair\. For example: `"engine Type"` : `"v6"`  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DecoderManifestArn`  <a name="cfn-iotfleetwise-vehicle-decodermanifestarn"></a>
The Amazon Resource Name \(ARN\) of a decoder manifest associated with the vehicle to create\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModelManifestArn`  <a name="cfn-iotfleetwise-vehicle-modelmanifestarn"></a>
The ARN of the vehicle model \(model manifest\) to create the vehicle from\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotfleetwise-vehicle-name"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-iotfleetwise-vehicle-tags"></a>
Metadata which can be used to manage the vehicle\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotfleetwise-vehicle-return-values"></a>

### Ref<a name="aws-resource-iotfleetwise-vehicle-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-iotfleetwise-vehicle-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotfleetwise-vehicle-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
Property description not available\.

`LastModificationTime`  <a name="LastModificationTime-fn::getatt"></a>
Property description not available\.