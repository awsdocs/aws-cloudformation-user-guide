# AWS::QuickSight::Analysis WordCloudOptions<a name="aws-properties-quicksight-analysis-wordcloudoptions"></a>

The word cloud options for a word cloud visual\.

## Syntax<a name="aws-properties-quicksight-analysis-wordcloudoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-wordcloudoptions-syntax.json"></a>

```
{
  "[CloudLayout](#cfn-quicksight-analysis-wordcloudoptions-cloudlayout)" : String,
  "[MaximumStringLength](#cfn-quicksight-analysis-wordcloudoptions-maximumstringlength)" : Double,
  "[WordCasing](#cfn-quicksight-analysis-wordcloudoptions-wordcasing)" : String,
  "[WordOrientation](#cfn-quicksight-analysis-wordcloudoptions-wordorientation)" : String,
  "[WordPadding](#cfn-quicksight-analysis-wordcloudoptions-wordpadding)" : String,
  "[WordScaling](#cfn-quicksight-analysis-wordcloudoptions-wordscaling)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-wordcloudoptions-syntax.yaml"></a>

```
  [CloudLayout](#cfn-quicksight-analysis-wordcloudoptions-cloudlayout): String
  [MaximumStringLength](#cfn-quicksight-analysis-wordcloudoptions-maximumstringlength): Double
  [WordCasing](#cfn-quicksight-analysis-wordcloudoptions-wordcasing): String
  [WordOrientation](#cfn-quicksight-analysis-wordcloudoptions-wordorientation): String
  [WordPadding](#cfn-quicksight-analysis-wordcloudoptions-wordpadding): String
  [WordScaling](#cfn-quicksight-analysis-wordcloudoptions-wordscaling): String
```

## Properties<a name="aws-properties-quicksight-analysis-wordcloudoptions-properties"></a>

`CloudLayout`  <a name="cfn-quicksight-analysis-wordcloudoptions-cloudlayout"></a>
The cloud layout options \(fluid, normal\) of a word cloud\.  
*Required*: No  
*Type*: String  
*Allowed values*: `FLUID | NORMAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumStringLength`  <a name="cfn-quicksight-analysis-wordcloudoptions-maximumstringlength"></a>
The length limit of each word from 1\-100\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WordCasing`  <a name="cfn-quicksight-analysis-wordcloudoptions-wordcasing"></a>
The word casing options \(lower\_case, existing\_case\) for the words in a word cloud\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EXISTING_CASE | LOWER_CASE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WordOrientation`  <a name="cfn-quicksight-analysis-wordcloudoptions-wordorientation"></a>
The word orientation options \(horizontal, horizontal\_and\_vertical\) for the words in a word cloud\.  
*Required*: No  
*Type*: String  
*Allowed values*: `HORIZONTAL | HORIZONTAL_AND_VERTICAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WordPadding`  <a name="cfn-quicksight-analysis-wordcloudoptions-wordpadding"></a>
The word padding options \(none, small, medium, large\) for the words in a word cloud\.  
*Required*: No  
*Type*: String  
*Allowed values*: `LARGE | MEDIUM | NONE | SMALL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WordScaling`  <a name="cfn-quicksight-analysis-wordcloudoptions-wordscaling"></a>
The word scaling options \(emphasize, normal\) for the words in a word cloud\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EMPHASIZE | NORMAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)