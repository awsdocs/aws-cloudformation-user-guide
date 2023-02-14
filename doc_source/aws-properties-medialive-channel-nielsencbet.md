# AWS::MediaLive::Channel NielsenCBET<a name="aws-properties-medialive-channel-nielsencbet"></a>

Complete these fields only if you want to insert watermarks of type Nielsen CBET

The parent of this entity is NielsenWatermarksSettings

## Syntax<a name="aws-properties-medialive-channel-nielsencbet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-nielsencbet-syntax.json"></a>

```
{
  "[CbetCheckDigitString](#cfn-medialive-channel-nielsencbet-cbetcheckdigitstring)" : String,
  "[CbetStepaside](#cfn-medialive-channel-nielsencbet-cbetstepaside)" : String,
  "[Csid](#cfn-medialive-channel-nielsencbet-csid)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-nielsencbet-syntax.yaml"></a>

```
  [CbetCheckDigitString](#cfn-medialive-channel-nielsencbet-cbetcheckdigitstring): 
    String
  [CbetStepaside](#cfn-medialive-channel-nielsencbet-cbetstepaside): String
  [Csid](#cfn-medialive-channel-nielsencbet-csid): String
```

## Properties<a name="aws-properties-medialive-channel-nielsencbet-properties"></a>

`CbetCheckDigitString`  <a name="cfn-medialive-channel-nielsencbet-cbetcheckdigitstring"></a>
Enter the CBET check digits to use in the watermark\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CbetStepaside`  <a name="cfn-medialive-channel-nielsencbet-cbetstepaside"></a>
Determines the method of CBET insertion mode when prior encoding is detected on the same layer\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Csid`  <a name="cfn-medialive-channel-nielsencbet-csid"></a>
Enter the CBET Source ID \(CSID\) to use in the watermark  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)