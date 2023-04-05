# AWS::QuickSight::Template EmptyVisual<a name="aws-properties-quicksight-template-emptyvisual"></a>

An empty visual\.

Empty visuals are used in layouts but have not been configured to show any data\. A new visual created in the Amazon QuickSight console is considered an `EmptyVisual` until a visual type is selected\.

## Syntax<a name="aws-properties-quicksight-template-emptyvisual-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-emptyvisual-syntax.json"></a>

```
{
  "[Actions](#cfn-quicksight-template-emptyvisual-actions)" : [ VisualCustomAction, ... ],
  "[DataSetIdentifier](#cfn-quicksight-template-emptyvisual-datasetidentifier)" : String,
  "[VisualId](#cfn-quicksight-template-emptyvisual-visualid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-emptyvisual-syntax.yaml"></a>

```
  [Actions](#cfn-quicksight-template-emptyvisual-actions): 
    - VisualCustomAction
  [DataSetIdentifier](#cfn-quicksight-template-emptyvisual-datasetidentifier): String
  [VisualId](#cfn-quicksight-template-emptyvisual-visualid): String
```

## Properties<a name="aws-properties-quicksight-template-emptyvisual-properties"></a>

`Actions`  <a name="cfn-quicksight-template-emptyvisual-actions"></a>
The list of custom actions that are configured for a visual\.  
*Required*: No  
*Type*: List of [VisualCustomAction](aws-properties-quicksight-template-visualcustomaction.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSetIdentifier`  <a name="cfn-quicksight-template-emptyvisual-datasetidentifier"></a>
The data set that is used in the empty visual\. Every visual requires a dataset to render\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VisualId`  <a name="cfn-quicksight-template-emptyvisual-visualid"></a>
The unique identifier of a visual\. This identifier must be unique within the context of a dashboard, template, or analysis\. Two dashboards, analyses, or templates can have visuals with the same identifiers\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)