# AWS::IoTWireless::ServiceProfile<a name="aws-resource-iotwireless-serviceprofile"></a>

Creates a new service profile\.

## Syntax<a name="aws-resource-iotwireless-serviceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-serviceprofile-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::ServiceProfile",
  "Properties" : {
      "[LoRaWAN](#cfn-iotwireless-serviceprofile-lorawan)" : LoRaWANServiceProfile,
      "[Name](#cfn-iotwireless-serviceprofile-name)" : String,
      "[Tags](#cfn-iotwireless-serviceprofile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotwireless-serviceprofile-syntax.yaml"></a>

```
Type: AWS::IoTWireless::ServiceProfile
Properties: 
  [LoRaWAN](#cfn-iotwireless-serviceprofile-lorawan): 
    LoRaWANServiceProfile
  [Name](#cfn-iotwireless-serviceprofile-name): String
  [Tags](#cfn-iotwireless-serviceprofile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotwireless-serviceprofile-properties"></a>

`LoRaWAN`  <a name="cfn-iotwireless-serviceprofile-lorawan"></a>
LoRaWAN service profile object\.  
*Required*: No  
*Type*: [LoRaWANServiceProfile](aws-properties-iotwireless-serviceprofile-lorawanserviceprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-serviceprofile-name"></a>
The name of the new resource\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-serviceprofile-tags"></a>
The tags are an array of key\-value pairs to attach to the specified resource\. Tags can have a minimum of 0 and a maximum of 50 items\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-serviceprofile-return-values"></a>

### Ref<a name="aws-resource-iotwireless-serviceprofile-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the service profile ID\.

### Fn::GetAtt<a name="aws-resource-iotwireless-serviceprofile-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-serviceprofile-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the service profile created\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the service profile created\.

`LoRaWAN.ChannelMask`  <a name="LoRaWAN.ChannelMask-fn::getatt"></a>
The ChannelMask value\.

`LoRaWAN.DevStatusReqFreq`  <a name="LoRaWAN.DevStatusReqFreq-fn::getatt"></a>
The DevStatusReqFreq value\.

`LoRaWAN.DlBucketSize`  <a name="LoRaWAN.DlBucketSize-fn::getatt"></a>
The DLBucketSize value\.

`LoRaWAN.DlRate`  <a name="LoRaWAN.DlRate-fn::getatt"></a>
The DLRate value\.

`LoRaWAN.DlRatePolicy`  <a name="LoRaWAN.DlRatePolicy-fn::getatt"></a>
The DLRatePolicy value\.

`LoRaWAN.DrMax`  <a name="LoRaWAN.DrMax-fn::getatt"></a>
The DRMax value\.

`LoRaWAN.DrMin`  <a name="LoRaWAN.DrMin-fn::getatt"></a>
The DRMin value\.

`LoRaWAN.HrAllowed`  <a name="LoRaWAN.HrAllowed-fn::getatt"></a>
The HRAllowed value that describes whether handover roaming is allowed\.

`LoRaWAN.MinGwDiversity`  <a name="LoRaWAN.MinGwDiversity-fn::getatt"></a>
The MinGwDiversity value\.

`LoRaWAN.NwkGeoLoc`  <a name="LoRaWAN.NwkGeoLoc-fn::getatt"></a>
The NwkGeoLoc value\.

`LoRaWAN.PrAllowed`  <a name="LoRaWAN.PrAllowed-fn::getatt"></a>
The PRAllowed value that describes whether passive roaming is allowed\.

`LoRaWAN.RaAllowed`  <a name="LoRaWAN.RaAllowed-fn::getatt"></a>
The RAAllowed value that describes whether roaming activation is allowed\.

`LoRaWAN.ReportDevStatusBattery`  <a name="LoRaWAN.ReportDevStatusBattery-fn::getatt"></a>
The ReportDevStatusBattery value\.

`LoRaWAN.ReportDevStatusMargin`  <a name="LoRaWAN.ReportDevStatusMargin-fn::getatt"></a>
The ReportDevStatusMargin value\.

`LoRaWAN.TargetPer`  <a name="LoRaWAN.TargetPer-fn::getatt"></a>
The TargetPer value\.

`LoRaWAN.UlBucketSize`  <a name="LoRaWAN.UlBucketSize-fn::getatt"></a>
The UlBucketSize value\.

`LoRaWAN.UlRate`  <a name="LoRaWAN.UlRate-fn::getatt"></a>
The ULRate value\.

`LoRaWAN.UlRatePolicy`  <a name="LoRaWAN.UlRatePolicy-fn::getatt"></a>
The ULRatePolicy value\.