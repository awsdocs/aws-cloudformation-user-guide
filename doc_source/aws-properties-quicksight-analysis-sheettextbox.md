# AWS::QuickSight::Analysis SheetTextBox<a name="aws-properties-quicksight-analysis-sheettextbox"></a>

A text box\.

## Syntax<a name="aws-properties-quicksight-analysis-sheettextbox-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-sheettextbox-syntax.json"></a>

```
{
  "[Content](#cfn-quicksight-analysis-sheettextbox-content)" : String,
  "[SheetTextBoxId](#cfn-quicksight-analysis-sheettextbox-sheettextboxid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-sheettextbox-syntax.yaml"></a>

```
  [Content](#cfn-quicksight-analysis-sheettextbox-content): String
  [SheetTextBoxId](#cfn-quicksight-analysis-sheettextbox-sheettextboxid): String
```

## Properties<a name="aws-properties-quicksight-analysis-sheettextbox-properties"></a>

`Content`  <a name="cfn-quicksight-analysis-sheettextbox-content"></a>
The content that is displayed in the text box\.  
*Required*: No  
*Type*: String  
*Maximum*: `150000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SheetTextBoxId`  <a name="cfn-quicksight-analysis-sheettextbox-sheettextboxid"></a>
The unique identifier for a text box\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have text boxes that share identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)