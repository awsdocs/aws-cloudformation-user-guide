# AWS::Rekognition::StreamProcessor BoundingBox<a name="aws-properties-rekognition-streamprocessor-boundingbox"></a>

Identifies the bounding box around the label, face, text, or personal protective equipment\. The `left` \(x\-coordinate\) and `top` \(y\-coordinate\) are coordinates representing the top and left sides of the bounding box\. Note that the upper\-left corner of the image is the origin \(0,0\)\. 

The `top` and `left` values returned are ratios of the overall image size\. For example, if the input image is 700x200 pixels, and the top\-left coordinate of the bounding box is 350x50 pixels, the API returns a `left` value of 0\.5 \(350/700\) and a `top` value of 0\.25 \(50/200\)\.

The `width` and `height` values represent the dimensions of the bounding box as a ratio of the overall image dimension\. For example, if the input image is 700x200 pixels, and the bounding box width is 70 pixels, the width returned is 0\.1\. For more information, see [BoundingBox](https://docs.aws.amazon.com/rekognition/latest/APIReference/API_BoundingBox)\.

**Note**  
 The bounding box coordinates can have negative values\. For example, if Amazon Rekognition is able to detect a face that is at the image edge and is only partially visible, the service can return coordinates that are outside the image bounds and, depending on the image edge, you might get negative values or values greater than 1 for the `left` or `top` values\. 

## Syntax<a name="aws-properties-rekognition-streamprocessor-boundingbox-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-rekognition-streamprocessor-boundingbox-syntax.json"></a>

```
{
  "[Height](#cfn-rekognition-streamprocessor-boundingbox-height)" : Double,
  "[Left](#cfn-rekognition-streamprocessor-boundingbox-left)" : Double,
  "[Top](#cfn-rekognition-streamprocessor-boundingbox-top)" : Double,
  "[Width](#cfn-rekognition-streamprocessor-boundingbox-width)" : Double
}
```

### YAML<a name="aws-properties-rekognition-streamprocessor-boundingbox-syntax.yaml"></a>

```
  [Height](#cfn-rekognition-streamprocessor-boundingbox-height): Double
  [Left](#cfn-rekognition-streamprocessor-boundingbox-left): Double
  [Top](#cfn-rekognition-streamprocessor-boundingbox-top): Double
  [Width](#cfn-rekognition-streamprocessor-boundingbox-width): Double
```

## Properties<a name="aws-properties-rekognition-streamprocessor-boundingbox-properties"></a>

`Height`  <a name="cfn-rekognition-streamprocessor-boundingbox-height"></a>
Height of the bounding box as a ratio of the overall image height\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Left`  <a name="cfn-rekognition-streamprocessor-boundingbox-left"></a>
Left coordinate of the bounding box as a ratio of overall image width\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Top`  <a name="cfn-rekognition-streamprocessor-boundingbox-top"></a>
Top coordinate of the bounding box as a ratio of overall image height\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Width`  <a name="cfn-rekognition-streamprocessor-boundingbox-width"></a>
Width of the bounding box as a ratio of the overall image width\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)