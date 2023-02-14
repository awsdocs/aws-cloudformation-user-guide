# AWS::IoTWireless::ServiceProfile LoRaWANServiceProfile<a name="aws-properties-iotwireless-serviceprofile-lorawanserviceprofile"></a>

LoRaWANServiceProfile object\.

## Syntax<a name="aws-properties-iotwireless-serviceprofile-lorawanserviceprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotwireless-serviceprofile-lorawanserviceprofile-syntax.json"></a>

```
{
  "[AddGwMetadata](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-addgwmetadata)" : Boolean,
  "[ChannelMask](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-channelmask)" : String,
  "[DevStatusReqFreq](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-devstatusreqfreq)" : Integer,
  "[DlBucketSize](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-dlbucketsize)" : Integer,
  "[DlRate](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-dlrate)" : Integer,
  "[DlRatePolicy](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-dlratepolicy)" : String,
  "[DrMax](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-drmax)" : Integer,
  "[DrMin](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-drmin)" : Integer,
  "[HrAllowed](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-hrallowed)" : Boolean,
  "[MinGwDiversity](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-mingwdiversity)" : Integer,
  "[NwkGeoLoc](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-nwkgeoloc)" : Boolean,
  "[PrAllowed](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-prallowed)" : Boolean,
  "[RaAllowed](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-raallowed)" : Boolean,
  "[ReportDevStatusBattery](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-reportdevstatusbattery)" : Boolean,
  "[ReportDevStatusMargin](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-reportdevstatusmargin)" : Boolean,
  "[TargetPer](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-targetper)" : Integer,
  "[UlBucketSize](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-ulbucketsize)" : Integer,
  "[UlRate](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-ulrate)" : Integer,
  "[UlRatePolicy](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-ulratepolicy)" : String
}
```

### YAML<a name="aws-properties-iotwireless-serviceprofile-lorawanserviceprofile-syntax.yaml"></a>

```
  [AddGwMetadata](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-addgwmetadata): Boolean
  [ChannelMask](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-channelmask): String
  [DevStatusReqFreq](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-devstatusreqfreq): Integer
  [DlBucketSize](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-dlbucketsize): Integer
  [DlRate](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-dlrate): Integer
  [DlRatePolicy](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-dlratepolicy): String
  [DrMax](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-drmax): Integer
  [DrMin](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-drmin): Integer
  [HrAllowed](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-hrallowed): Boolean
  [MinGwDiversity](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-mingwdiversity): Integer
  [NwkGeoLoc](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-nwkgeoloc): Boolean
  [PrAllowed](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-prallowed): Boolean
  [RaAllowed](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-raallowed): Boolean
  [ReportDevStatusBattery](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-reportdevstatusbattery): Boolean
  [ReportDevStatusMargin](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-reportdevstatusmargin): Boolean
  [TargetPer](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-targetper): Integer
  [UlBucketSize](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-ulbucketsize): Integer
  [UlRate](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-ulrate): Integer
  [UlRatePolicy](#cfn-iotwireless-serviceprofile-lorawanserviceprofile-ulratepolicy): String
```

## Properties<a name="aws-properties-iotwireless-serviceprofile-lorawanserviceprofile-properties"></a>

`AddGwMetadata`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-addgwmetadata"></a>
The AddGWMetaData value\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ChannelMask`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-channelmask"></a>
The ChannelMask value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DevStatusReqFreq`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-devstatusreqfreq"></a>
The DevStatusReqFreq value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DlBucketSize`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-dlbucketsize"></a>
The DLBucketSize value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DlRate`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-dlrate"></a>
The DLRate value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DlRatePolicy`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-dlratepolicy"></a>
The DLRatePolicy value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DrMax`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-drmax"></a>
The DRMax value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `15`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DrMin`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-drmin"></a>
The DRMin value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `15`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HrAllowed`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-hrallowed"></a>
The HRAllowed value that describes whether handover roaming is allowed\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinGwDiversity`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-mingwdiversity"></a>
The MinGwDiversity value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NwkGeoLoc`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-nwkgeoloc"></a>
The NwkGeoLoc value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PrAllowed`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-prallowed"></a>
The PRAllowed value that describes whether passive roaming is allowed\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RaAllowed`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-raallowed"></a>
The RAAllowed value that describes whether roaming activation is allowed\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportDevStatusBattery`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-reportdevstatusbattery"></a>
The ReportDevStatusBattery value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportDevStatusMargin`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-reportdevstatusmargin"></a>
The ReportDevStatusMargin value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetPer`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-targetper"></a>
The TargetPer value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UlBucketSize`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-ulbucketsize"></a>
The UlBucketSize value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UlRate`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-ulrate"></a>
The ULRate value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UlRatePolicy`  <a name="cfn-iotwireless-serviceprofile-lorawanserviceprofile-ulratepolicy"></a>
The ULRatePolicy value\.  
This property is `ReadOnly` and can't be inputted for create\. It's returned with `Fn::GetAtt`  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)