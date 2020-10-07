# AWS::MediaLive::Channel InputLossBehavior<a name="aws-properties-medialive-channel-inputlossbehavior"></a>

Changes the default behavior of the input loss behavior feature\. This element belongs to GlobalConfiguration\.

## Syntax<a name="aws-properties-medialive-channel-inputlossbehavior-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-inputlossbehavior-syntax.json"></a>

```
{
  "[BlackFrameMsec](#cfn-medialive-channel-inputlossbehavior-blackframemsec)" : Integer,
  "[InputLossImageColor](#cfn-medialive-channel-inputlossbehavior-inputlossimagecolor)" : String,
  "[InputLossImageSlate](#cfn-medialive-channel-inputlossbehavior-inputlossimageslate)" : InputLocation,
  "[InputLossImageType](#cfn-medialive-channel-inputlossbehavior-inputlossimagetype)" : String,
  "[RepeatFrameMsec](#cfn-medialive-channel-inputlossbehavior-repeatframemsec)" : Integer
}
```

### YAML<a name="aws-properties-medialive-channel-inputlossbehavior-syntax.yaml"></a>

```
  [BlackFrameMsec](#cfn-medialive-channel-inputlossbehavior-blackframemsec): Integer
  [InputLossImageColor](#cfn-medialive-channel-inputlossbehavior-inputlossimagecolor): String
  [InputLossImageSlate](#cfn-medialive-channel-inputlossbehavior-inputlossimageslate): 
    InputLocation
  [InputLossImageType](#cfn-medialive-channel-inputlossbehavior-inputlossimagetype): String
  [RepeatFrameMsec](#cfn-medialive-channel-inputlossbehavior-repeatframemsec): Integer
```

## Properties<a name="aws-properties-medialive-channel-inputlossbehavior-properties"></a>

`BlackFrameMsec`  <a name="cfn-medialive-channel-inputlossbehavior-blackframemsec"></a>
On input loss, the number of milliseconds to substitute black into the output before switching to the frame specified by inputLossImageType\. A value x, where 0 <= x <= 1,000,000 and a value of 1,000,000 will be interpreted as infinite\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputLossImageColor`  <a name="cfn-medialive-channel-inputlossbehavior-inputlossimagecolor"></a>
When input loss image type is "color" this field specifies the color to use\. Value: 6 hex characters representing the values of RGB\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputLossImageSlate`  <a name="cfn-medialive-channel-inputlossbehavior-inputlossimageslate"></a>
When input loss image type is "slate" these fields specify the parameters for accessing the slate\.  
*Required*: No  
*Type*: [InputLocation](aws-properties-medialive-channel-inputlocation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputLossImageType`  <a name="cfn-medialive-channel-inputlossbehavior-inputlossimagetype"></a>
Indicates whether to substitute a solid color or a slate into the output after input loss exceeds blackFrameMsec\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepeatFrameMsec`  <a name="cfn-medialive-channel-inputlossbehavior-repeatframemsec"></a>
On input loss, the number of milliseconds to repeat the previous picture before substituting black into the output\. A value x, where 0 <= x <= 1,000,000 and a value of 1,000,000 will be interpreted as infinite\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)