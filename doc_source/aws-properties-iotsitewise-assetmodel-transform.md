# AWS::IoTSiteWise::AssetModel Transform<a name="aws-properties-iotsitewise-assetmodel-transform"></a>

Contains an asset transform property\. A transform is a one\-to\-one mapping of a property's data points from one form to another\. For example, you can use a transform to convert a Celsius data stream to Fahrenheit by applying the transformation expression to each data point of the Celsius stream\. Transforms can only input properties that are `INTEGER`, `DOUBLE`, or `BOOLEAN` type\. Booleans convert to `0 `\(`FALSE`\) and `1` \(`TRUE`\)\.\.

For more information, see [Defining data properties](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/asset-properties.html#transforms) in the *AWS IoT SiteWise User Guide*\.

## Syntax<a name="aws-properties-iotsitewise-assetmodel-transform-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-assetmodel-transform-syntax.json"></a>

```
{
  "[Expression](#cfn-iotsitewise-assetmodel-transform-expression)" : String,
  "[Variables](#cfn-iotsitewise-assetmodel-transform-variables)" : [ ExpressionVariable, ... ]
}
```

### YAML<a name="aws-properties-iotsitewise-assetmodel-transform-syntax.yaml"></a>

```
  [Expression](#cfn-iotsitewise-assetmodel-transform-expression): String
  [Variables](#cfn-iotsitewise-assetmodel-transform-variables): 
    - ExpressionVariable
```

## Properties<a name="aws-properties-iotsitewise-assetmodel-transform-properties"></a>

`Expression`  <a name="cfn-iotsitewise-assetmodel-transform-expression"></a>
The mathematical expression that defines the transformation function\. You can specify up to 10 variables per expression\. You can specify up to 10 functions per expression\.   
For more information, see [Quotas](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/quotas.html) in the *AWS IoT SiteWise User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Variables`  <a name="cfn-iotsitewise-assetmodel-transform-variables"></a>
The list of variables used in the expression\.  
*Required*: Yes  
*Type*: List of [ExpressionVariable](aws-properties-iotsitewise-assetmodel-expressionvariable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)