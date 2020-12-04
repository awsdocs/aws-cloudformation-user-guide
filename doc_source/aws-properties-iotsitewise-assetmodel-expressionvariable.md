# AWS::IoTSiteWise::AssetModel ExpressionVariable<a name="aws-properties-iotsitewise-assetmodel-expressionvariable"></a>

Contains expression variable information\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-expressionvariable-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-expressionvariable-syntax.json"></a>

```
{
  "[Name](#cfn-iotsitewise-assetmodel-expressionvariable-name)" : String,
  "[Value](#cfn-iotsitewise-assetmodel-expressionvariable-value)" : VariableValue
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-expressionvariable-syntax.yaml"></a>

```
  [Name](#cfn-iotsitewise-assetmodel-expressionvariable-name): String
  [Value](#cfn-iotsitewise-assetmodel-expressionvariable-value): 
    VariableValue
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-expressionvariable-properties"></a>

`Name`  <a name="cfn-iotsitewise-assetmodel-expressionvariable-name"></a>
The friendly name of the variable to be used in the expression\.  
The maximum length is 64 characters with the pattern `^[a-z][a-z0-9_]*$`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-iotsitewise-assetmodel-expressionvariable-value"></a>
The variable that identifies an asset property from which to use values\.  
*Required*: Yes  
*Type*: [VariableValue](aws-properties-iotsitewise-assetmodel-variablevalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)