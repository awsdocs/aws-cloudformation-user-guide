# AWS::QuickSight::Template SmallMultiplesAxisProperties<a name="aws-properties-quicksight-template-smallmultiplesaxisproperties"></a>

Configures the properties of a chart's axes that are used by small multiples panels\.

## Syntax<a name="aws-properties-quicksight-template-smallmultiplesaxisproperties-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-smallmultiplesaxisproperties-syntax.json"></a>

```
{
  "[Placement](#cfn-quicksight-template-smallmultiplesaxisproperties-placement)" : String,
  "[Scale](#cfn-quicksight-template-smallmultiplesaxisproperties-scale)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-smallmultiplesaxisproperties-syntax.yaml"></a>

```
  [Placement](#cfn-quicksight-template-smallmultiplesaxisproperties-placement): String
  [Scale](#cfn-quicksight-template-smallmultiplesaxisproperties-scale): String
```

## Properties<a name="aws-properties-quicksight-template-smallmultiplesaxisproperties-properties"></a>

`Placement`  <a name="cfn-quicksight-template-smallmultiplesaxisproperties-placement"></a>
Defines the placement of the axis\. By default, axes are rendered `OUTSIDE` of the panels\. Axes with `INDEPENDENT` scale are rendered `INSIDE` the panels\.  
*Required*: No  
*Type*: String  
*Allowed values*: `INSIDE | OUTSIDE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scale`  <a name="cfn-quicksight-template-smallmultiplesaxisproperties-scale"></a>
Determines whether scale of the axes are shared or independent\. The default value is `SHARED`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `INDEPENDENT | SHARED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)