# AWS::Synthetics::Canary BaseScreenshot<a name="aws-properties-synthetics-canary-basescreenshot"></a>

A structure representing a screenshot that is used as a baseline during visual monitoring comparisons made by the canary\.

## Syntax<a name="aws-properties-synthetics-canary-basescreenshot-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-synthetics-canary-basescreenshot-syntax.json"></a>

```
{
  "[IgnoreCoordinates](#cfn-synthetics-canary-basescreenshot-ignorecoordinates)" : [ String, ... ],
  "[ScreenshotName](#cfn-synthetics-canary-basescreenshot-screenshotname)" : String
}
```

### YAML<a name="aws-properties-synthetics-canary-basescreenshot-syntax.yaml"></a>

```
  [IgnoreCoordinates](#cfn-synthetics-canary-basescreenshot-ignorecoordinates): 
    - String
  [ScreenshotName](#cfn-synthetics-canary-basescreenshot-screenshotname): String
```

## Properties<a name="aws-properties-synthetics-canary-basescreenshot-properties"></a>

`IgnoreCoordinates`  <a name="cfn-synthetics-canary-basescreenshot-ignorecoordinates"></a>
Coordinates that define the part of a screen to ignore during screenshot comparisons\. To obtain the coordinates to use here, use the CloudWatch Logs console to draw the boundaries on the screen\. For more information, see \{LINK\}  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScreenshotName`  <a name="cfn-synthetics-canary-basescreenshot-screenshotname"></a>
The name of the screenshot\. This is generated the first time the canary is run after the `UpdateCanary` operation that specified for this canary to perform visual monitoring\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)