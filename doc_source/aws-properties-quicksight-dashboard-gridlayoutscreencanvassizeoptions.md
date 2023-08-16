# AWS::QuickSight::Dashboard GridLayoutScreenCanvasSizeOptions<a name="aws-properties-quicksight-dashboard-gridlayoutscreencanvassizeoptions"></a>

The options that determine the sizing of the canvas used in a grid layout\.

## Syntax<a name="aws-properties-quicksight-dashboard-gridlayoutscreencanvassizeoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-gridlayoutscreencanvassizeoptions-syntax.json"></a>

```
{
  "[OptimizedViewPortWidth](#cfn-quicksight-dashboard-gridlayoutscreencanvassizeoptions-optimizedviewportwidth)" : String,
  "[ResizeOption](#cfn-quicksight-dashboard-gridlayoutscreencanvassizeoptions-resizeoption)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-gridlayoutscreencanvassizeoptions-syntax.yaml"></a>

```
  [OptimizedViewPortWidth](#cfn-quicksight-dashboard-gridlayoutscreencanvassizeoptions-optimizedviewportwidth): String
  [ResizeOption](#cfn-quicksight-dashboard-gridlayoutscreencanvassizeoptions-resizeoption): String
```

## Properties<a name="aws-properties-quicksight-dashboard-gridlayoutscreencanvassizeoptions-properties"></a>

`OptimizedViewPortWidth`  <a name="cfn-quicksight-dashboard-gridlayoutscreencanvassizeoptions-optimizedviewportwidth"></a>
The width that the view port will be optimized for when the layout renders\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResizeOption`  <a name="cfn-quicksight-dashboard-gridlayoutscreencanvassizeoptions-resizeoption"></a>
This value determines the layout behavior when the viewport is resized\.  
+  `FIXED`: A fixed width will be used when optimizing the layout\. In the Amazon QuickSight console, this option is called `Classic`\.
+  `RESPONSIVE`: The width of the canvas will be responsive and optimized to the view port\. In the Amazon QuickSight console, this option is called `Tiled`\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `FIXED | RESPONSIVE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)