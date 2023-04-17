# AWS::QuickSight::Dashboard SectionAfterPageBreak<a name="aws-properties-quicksight-dashboard-sectionafterpagebreak"></a>

The configuration of a page break after a section\.

## Syntax<a name="aws-properties-quicksight-dashboard-sectionafterpagebreak-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-sectionafterpagebreak-syntax.json"></a>

```
{
  "[Status](#cfn-quicksight-dashboard-sectionafterpagebreak-status)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-sectionafterpagebreak-syntax.yaml"></a>

```
  [Status](#cfn-quicksight-dashboard-sectionafterpagebreak-status): String
```

## Properties<a name="aws-properties-quicksight-dashboard-sectionafterpagebreak-properties"></a>

`Status`  <a name="cfn-quicksight-dashboard-sectionafterpagebreak-status"></a>
The option that enables or disables a page break at the end of a section\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)