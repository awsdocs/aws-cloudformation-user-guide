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
LoRaWANServiceProfile object\.  
*Required*: No  
*Type*: [LoRaWANServiceProfile](aws-properties-iotwireless-serviceprofile-lorawanserviceprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-serviceprofile-name"></a>
The name of the new resource\. The maximum length is 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-serviceprofile-tags"></a>
An array of key\-value pairs to apply to this resource\. Tags can have a minimum of 0 and a maximum of 50 items\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-serviceprofile-return-values"></a>

### Ref<a name="aws-resource-iotwireless-serviceprofile-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the service profile ID\.

### Fn::GetAtt<a name="aws-resource-iotwireless-serviceprofile-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-serviceprofile-return-values-fn--getatt-fn--getatt"></a>

`AddGwMetadata`  <a name="AddGwMetadata-fn::getatt"></a>
The AddGWMetaData value\.

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the service profile created\.

`ChannelMask`  <a name="ChannelMask-fn::getatt"></a>
The ChannelMask value\. It has a maximum length of 2048 characters\.

`DevStatusReqFreq`  <a name="DevStatusReqFreq-fn::getatt"></a>
The DevStatusReqFreq value\. The minimum value is 0 and maximum value is 2147483647\.

`DlBucketSize`  <a name="DlBucketSize-fn::getatt"></a>
The DLBucketSize value\. The minimum value is 0 and maximum value is 2147483647\.

`DlRate`  <a name="DlRate-fn::getatt"></a>
The DLRate value\. The minimum value is 0 and maximum value is 2147483647\.

`DlRatePolicy`  <a name="DlRatePolicy-fn::getatt"></a>
The DLRatePolicy value\. Maximum length is 256 characters\.

`DrMax`  <a name="DrMax-fn::getatt"></a>
The DRMax value\. The minimum value is 0 and maximum value is 15\.

`DrMin`  <a name="DrMin-fn::getatt"></a>
The DRMin value\. The minimum value is 0 and maximum value is 15\.

`HrAllowed`  <a name="HrAllowed-fn::getatt"></a>
The HRAllowed value that describes whether handover roaming is allowed\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the service profile created\.

`MinGwDiversity`  <a name="MinGwDiversity-fn::getatt"></a>
The MinGwDiversity value\. The minimum value is 1 and maximum value is 100\.

`NwkGeoLoc`  <a name="NwkGeoLoc-fn::getatt"></a>
The NwkGeoLoc value\.

`PrAllowed`  <a name="PrAllowed-fn::getatt"></a>
The PRAllowed value that describes whether passive roaming is allowed\.

`RaAllowed`  <a name="RaAllowed-fn::getatt"></a>
The RAAllowed value that describes whether roaming activation is allowed\.

`ReportDevStatusBattery`  <a name="ReportDevStatusBattery-fn::getatt"></a>
The ReportDevStatusBattery value\.

`ReportDevStatusMargin`  <a name="ReportDevStatusMargin-fn::getatt"></a>
The ReportDevStatusMargin value\.

`TargetPer`  <a name="TargetPer-fn::getatt"></a>
The TargetPer value\. The minimum value is 0 and maximum value is 100\.

`UlBucketSize`  <a name="UlBucketSize-fn::getatt"></a>
The UlBucketSize value\. The minimum value is 0 and maximum value is 2147483647\.

`UlRate`  <a name="UlRate-fn::getatt"></a>
The ULRate value\. The minimum value is 0 and maximum value is 2147483647\.

`UlRatePolicy`  <a name="UlRatePolicy-fn::getatt"></a>
The ULRatePolicy value\. Maximum length is 256 characters\.