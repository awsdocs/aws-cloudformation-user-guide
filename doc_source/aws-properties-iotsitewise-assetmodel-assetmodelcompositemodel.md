# AWS::IoTSiteWise::AssetModel AssetModelCompositeModel<a name="aws-properties-iotsitewise-assetmodel-assetmodelcompositemodel"></a>

Contains information about a composite model in an asset model\. This object contains the asset property definitions that you define in the composite model\. You can use composite asset models to define alarms on this asset model\.

If you use the `AssetModelCompositeModel` property to create an alarm, you must use the following information to define three asset model properties:
+ Use an asset model property to specify the alarm type\.
  + The name must be `AWS/ALARM_TYPE`\.
  + The data type must be `STRING`\.
  + For the `Type` property, the type name must be `Attribute` and the default value must be `IOT_EVENTS`\.
+ Use an asset model property to specify the alarm source\.
  + The name must be `AWS/ALARM_SOURCE`\.
  + The data type must be `STRING`\.
  + For the `Type` property, the type name must be `Attribute` and the default value must be the ARN of the alarm model that you created in AWS IoT Events\.
**Note**  
For the ARN of the alarm model, you can use the `Fn::Sub` intrinsic function to substitute the `AWS::Partition`, `AWS::Region`, and `AWS::AccountId` variables in an input string with values that you specify\.   
For example, `Fn::Sub: "arn:${AWS::Partition}:iotevents:${AWS::Region}:${AWS::AccountId}:alarmModel/TestAlarmModel"`\.  
Replace `TestAlarmModel` with the name of your alarm model\.  
For more information about using the `Fn::Sub` intrinsic function, see [Fn::Sub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-sub.html)\.
+ Use an asset model property to specify the state of the alarm\.
  + The name must be `AWS/ALARM_STATE`\.
  + The data type must be `STRUCT`\.
  + The `DataTypeSpec` value must be `AWS/ALARM_STATE`\.
  + For the `Type` property, the type name must be `Measurement`\.

At the bottom of this page, we provide a YAML example that you can modify to create an alarm\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-assetmodelcompositemodel-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-assetmodelcompositemodel-syntax.json"></a>

```
{
  "[CompositeModelProperties](#cfn-iotsitewise-assetmodel-assetmodelcompositemodel-compositemodelproperties)" : [ AssetModelProperty, ... ],
  "[Description](#cfn-iotsitewise-assetmodel-assetmodelcompositemodel-description)" : String,
  "[Name](#cfn-iotsitewise-assetmodel-assetmodelcompositemodel-name)" : String,
  "[Type](#cfn-iotsitewise-assetmodel-assetmodelcompositemodel-type)" : String
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-assetmodelcompositemodel-syntax.yaml"></a>

```
  [CompositeModelProperties](#cfn-iotsitewise-assetmodel-assetmodelcompositemodel-compositemodelproperties): 
    - AssetModelProperty
  [Description](#cfn-iotsitewise-assetmodel-assetmodelcompositemodel-description): String
  [Name](#cfn-iotsitewise-assetmodel-assetmodelcompositemodel-name): String
  [Type](#cfn-iotsitewise-assetmodel-assetmodelcompositemodel-type): String
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-assetmodelcompositemodel-properties"></a>

`CompositeModelProperties`  <a name="cfn-iotsitewise-assetmodel-assetmodelcompositemodel-compositemodelproperties"></a>
The asset property definitions for this composite model\.  
*Required*: No  
*Type*: List of [AssetModelProperty](aws-properties-iotsitewise-assetmodel-assetmodelproperty.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-iotsitewise-assetmodel-assetmodelcompositemodel-description"></a>
The description of the composite model\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotsitewise-assetmodel-assetmodelcompositemodel-name"></a>
The name of the composite model\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iotsitewise-assetmodel-assetmodelcompositemodel-type"></a>
The type of the composite model\. For alarm composite models, this type is `AWS/ALARM`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-iotsitewise-assetmodel-assetmodelcompositemodel--examples"></a>



### Create an alarm model<a name="aws-properties-iotsitewise-assetmodel-assetmodelcompositemodel--examples--Create_an_alarm_model"></a>

You can modify the following example to create an alarm model\.

**Note**  
Replace `TestAlarmModel` with the name of your alarm model\.

#### YAML<a name="aws-properties-iotsitewise-assetmodel-assetmodelcompositemodel--examples--Create_an_alarm_model--yaml"></a>

```
Resources:
  AssetModelWithAlarmCompositeModel:
    Type: AWS::IoTSiteWise::AssetModel
    Properties:
      AssetModelName: AssetModelWithValidAlarmCompositeModel
      AssetModelDescription: AssetModelWithValidAlarmCompositeModel
      AssetModelCompositeModels:
        - Description: compositeModel created by cfn
          Name: TestAlarmCompositeModel
          Type: AWS/ALARM
          CompositeModelProperties:
            - LogicalId: MyLogicalId_for_ALARM_TYPE_1
              Name: AWS/ALARM_TYPE
              DataType: STRING
              Type:
                TypeName: Attribute
                Attribute:
                  DefaultValue: IOT_EVENTS
            - LogicalId: MyLogicalId_for_ALARM_SOURCE_1
              Name: AWS/ALARM_SOURCE
              DataType: STRING
              Type:
                TypeName: Attribute
                Attribute:
                DefaultValue:
                  Fn::Sub: "arn:${AWS::Partition}:iotevents:${AWS::Region}:${AWS::AccountId}:alarmModel/TestAlarmModel"
            - LogicalId: MyLogicalId_for_ALARM_STATE_1
              Name: AWS/ALARM_STATE
              DataType: STRUCT
              DataTypeSpec: AWS/ALARM_STATE
              Type:
                TypeName: Measurement
```