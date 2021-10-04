# AWS::Location::RouteCalculator<a name="aws-resource-location-routecalculator"></a>

The `AWS::Location::RouteCalculator` resource specifies a route calculator resource in your AWS account\.

You can send requests to a route calculator resource to estimate travel time, distance, and get directions\. A route calculator sources traffic and road network data from your chosen data provider\.

## Syntax<a name="aws-resource-location-routecalculator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-location-routecalculator-syntax.json"></a>

```
{
  "Type" : "AWS::Location::RouteCalculator",
  "Properties" : {
      "[CalculatorName](#cfn-location-routecalculator-calculatorname)" : String,
      "[DataSource](#cfn-location-routecalculator-datasource)" : String,
      "[Description](#cfn-location-routecalculator-description)" : String,
      "[PricingPlan](#cfn-location-routecalculator-pricingplan)" : String
    }
}
```

### YAML<a name="aws-resource-location-routecalculator-syntax.yaml"></a>

```
Type: AWS::Location::RouteCalculator
Properties: 
  [CalculatorName](#cfn-location-routecalculator-calculatorname): String
  [DataSource](#cfn-location-routecalculator-datasource): String
  [Description](#cfn-location-routecalculator-description): String
  [PricingPlan](#cfn-location-routecalculator-pricingplan): String
```

## Properties<a name="aws-resource-location-routecalculator-properties"></a>

`CalculatorName`  <a name="cfn-location-routecalculator-calculatorname"></a>
The name of the route calculator resource\.  
Requirements:  
+ Can use alphanumeric characters \(A–Z, a–z, 0–9\) , hyphens \(\-\), periods \(\.\), and underscores \(\_\)\.
+ Must be a unique route calculator resource name\.
+ No spaces allowed\. For example, `ExampleRouteCalculator`\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[-._\w]+$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataSource`  <a name="cfn-location-routecalculator-datasource"></a>
Specifies the data provider of traffic and road network data\.  
This field is case\-sensitive\. Enter the valid values as shown\. For example, entering `HERE` returns an error\.
Valid values include:  
+ `Esri`
+ `Here`
For more information about data providers, see the [Amazon Location Service data providers page](https://docs.aws.amazon.com/location/latest/developerguide/what-is-data-provider.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-location-routecalculator-description"></a>
The optional description for the route calculator resource\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PricingPlan`  <a name="cfn-location-routecalculator-pricingplan"></a>
Specifies the pricing plan for your route calculator resource\.  
For additional details and restrictions on each pricing plan option, see the [Amazon Location Service pricing page](https://docs.aws.amazon.com/location/pricing/)\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MobileAssetManagement | MobileAssetTracking | RequestBasedUsage`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)