# AWS::QuickSight::Template Entity<a name="aws-properties-quicksight-template-entity"></a>

An object, structure, or sub\-structure of an analysis, template, or dashboard\.

## Syntax<a name="aws-properties-quicksight-template-entity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-entity-syntax.json"></a>

```
{
  "[Path](#cfn-quicksight-template-entity-path)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-entity-syntax.yaml"></a>

```
  [Path](#cfn-quicksight-template-entity-path): String
```

## Properties<a name="aws-properties-quicksight-template-entity-properties"></a>

`Path`  <a name="cfn-quicksight-template-entity-path"></a>
The hierarchical path of the entity within the analysis, template, or dashboard definition tree\.  
*Required*: No  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)