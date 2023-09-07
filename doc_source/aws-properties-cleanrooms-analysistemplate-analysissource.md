# AWS::CleanRooms::AnalysisTemplate AnalysisSource<a name="aws-properties-cleanrooms-analysistemplate-analysissource"></a>

The structure that defines the body of the analysis template\.

## Syntax<a name="aws-properties-cleanrooms-analysistemplate-analysissource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-analysistemplate-analysissource-syntax.json"></a>

```
{
  "[Text](#cfn-cleanrooms-analysistemplate-analysissource-text)" : String
}
```

### YAML<a name="aws-properties-cleanrooms-analysistemplate-analysissource-syntax.yaml"></a>

```
  [Text](#cfn-cleanrooms-analysistemplate-analysissource-text): String
```

## Properties<a name="aws-properties-cleanrooms-analysistemplate-analysissource-properties"></a>

`Text`  <a name="cfn-cleanrooms-analysistemplate-analysissource-text"></a>
The query text\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `15000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)