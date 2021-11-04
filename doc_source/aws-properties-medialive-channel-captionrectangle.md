# AWS::MediaLive::Channel CaptionRectangle<a name="aws-properties-medialive-channel-captionrectangle"></a>

Settings to configure the caption rectangle for an output captions that will be created using this Teletext source captions\.

The parent of this entity is TeletextSourceSettings\.

## Syntax<a name="aws-properties-medialive-channel-captionrectangle-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-captionrectangle-syntax.json"></a>

```
{
  "[Height](#cfn-medialive-channel-captionrectangle-height)" : Double,
  "[LeftOffset](#cfn-medialive-channel-captionrectangle-leftoffset)" : Double,
  "[TopOffset](#cfn-medialive-channel-captionrectangle-topoffset)" : Double,
  "[Width](#cfn-medialive-channel-captionrectangle-width)" : Double
}
```

### YAML<a name="aws-properties-medialive-channel-captionrectangle-syntax.yaml"></a>

```
  [Height](#cfn-medialive-channel-captionrectangle-height): Double
  [LeftOffset](#cfn-medialive-channel-captionrectangle-leftoffset): Double
  [TopOffset](#cfn-medialive-channel-captionrectangle-topoffset): Double
  [Width](#cfn-medialive-channel-captionrectangle-width): Double
```

## Properties<a name="aws-properties-medialive-channel-captionrectangle-properties"></a>

`Height`  <a name="cfn-medialive-channel-captionrectangle-height"></a>
See the description in leftOffset\.  
 For height, specify the entire height of the rectangle as a percentage of the underlying frame height\. For example, \\"80\\" means the rectangle height is 80% of the underlying frame height\. The topOffset and rectangleHeight must add up to 100% or less\. This field corresponds to tts:extent \- Y in the TTML standard\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LeftOffset`  <a name="cfn-medialive-channel-captionrectangle-leftoffset"></a>
Applies only if you plan to convert these source captions to EBU\-TT\-D or TTML in an output\. \(Make sure to leave the default if you don't have either of these formats in the output\.\) You can define a display rectangle for the captions that is smaller than the underlying video frame\. You define the rectangle by specifying the position of the left edge, top edge, bottom edge, and right edge of the rectangle, all within the underlying video frame\. The units for the measurements are percentages\. If you specify a value for one of these fields, you must specify a value for all of them\.  
 For leftOffset, specify the position of the left edge of the rectangle, as a percentage of the underlying frame width, and relative to the left edge of the frame\. For example, \\"10\\" means the measurement is 10% of the underlying frame width\. The rectangle left edge starts at that position from the left edge of the frame\. This field corresponds to tts:origin \- X in the TTML standard\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopOffset`  <a name="cfn-medialive-channel-captionrectangle-topoffset"></a>
See the description in leftOffset\.  
 For topOffset, specify the position of the top edge of the rectangle, as a percentage of the underlying frame height, and relative to the top edge of the frame\. For example, \\"10\\" means the measurement is 10% of the underlying frame height\. The rectangle top edge starts at that position from the top edge of the frame\. This field corresponds to tts:origin \- Y in the TTML standard\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Width`  <a name="cfn-medialive-channel-captionrectangle-width"></a>
See the description in leftOffset\.  
 For width, specify the entire width of the rectangle as a percentage of the underlying frame width\. For example, \\"80\\" means the rectangle width is 80% of the underlying frame width\. The leftOffset and rectangleWidth must add up to 100% or less\. This field corresponds to tts:extent \- X in the TTML standard\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)