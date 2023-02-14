# AWS::QuickSight::Analysis AnalysisSourceEntity<a name="aws-properties-quicksight-analysis-analysissourceentity"></a>

The source entity of an analysis\.

## Syntax<a name="aws-properties-quicksight-analysis-analysissourceentity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-analysissourceentity-syntax.json"></a>

```
{
  "[SourceTemplate](#cfn-quicksight-analysis-analysissourceentity-sourcetemplate)" : AnalysisSourceTemplate
}
```

### YAML<a name="aws-properties-quicksight-analysis-analysissourceentity-syntax.yaml"></a>

```
  [SourceTemplate](#cfn-quicksight-analysis-analysissourceentity-sourcetemplate): 
    AnalysisSourceTemplate
```

## Properties<a name="aws-properties-quicksight-analysis-analysissourceentity-properties"></a>

`SourceTemplate`  <a name="cfn-quicksight-analysis-analysissourceentity-sourcetemplate"></a>
The source template for the source entity of the analysis\.  
*Required*: No  
*Type*: [AnalysisSourceTemplate](aws-properties-quicksight-analysis-analysissourcetemplate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)