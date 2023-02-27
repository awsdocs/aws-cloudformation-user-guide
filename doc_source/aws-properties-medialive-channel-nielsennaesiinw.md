# AWS::MediaLive::Channel NielsenNaesIiNw<a name="aws-properties-medialive-channel-nielsennaesiinw"></a>

Complete these fields only if you want to insert watermarks of type Nielsen NAES II \(N2\) and Nielsen NAES VI \(NW\)\.

The parent of this entity is NielsenWatermarksSettings\.

## Syntax<a name="aws-properties-medialive-channel-nielsennaesiinw-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-nielsennaesiinw-syntax.json"></a>

```
{
  "[CheckDigitString](#cfn-medialive-channel-nielsennaesiinw-checkdigitstring)" : String,
  "[Sid](#cfn-medialive-channel-nielsennaesiinw-sid)" : Double
}
```

### YAML<a name="aws-properties-medialive-channel-nielsennaesiinw-syntax.yaml"></a>

```
  [CheckDigitString](#cfn-medialive-channel-nielsennaesiinw-checkdigitstring): 
    String
  [Sid](#cfn-medialive-channel-nielsennaesiinw-sid): Double
```

## Properties<a name="aws-properties-medialive-channel-nielsennaesiinw-properties"></a>

`CheckDigitString`  <a name="cfn-medialive-channel-nielsennaesiinw-checkdigitstring"></a>
Enter the check digit string for the watermark  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Sid`  <a name="cfn-medialive-channel-nielsennaesiinw-sid"></a>
Enter the Nielsen Source ID \(SID\) to include in the watermark  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)