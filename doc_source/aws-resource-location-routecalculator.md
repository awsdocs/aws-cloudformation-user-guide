# AWS::Location::RouteCalculator<a name="aws-resource-location-routecalculator"></a>

Specifies a route calculator resource in your AWS account\.

You can send requests to a route calculator resource to estimate travel time, distance, and get directions\. A route calculator sources traffic and road network data from your chosen data provider\.

**Note**  
If your application is tracking or routing assets you use in your business, such as delivery vehicles or employees, you must not use Esri as your geolocation provider\. See section 82 of the [AWS service terms](http://aws.amazon.com/service-terms) for more details\.

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
+ Must be a unique Route calculator resource name\.
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
+ `Esri` – For additional information about [Esri](https://docs.aws.amazon.com/location/latest/developerguide/esri.html)'s coverage in your region of interest, see [Esri details on street networks and traffic coverage](https://doc.arcgis.com/en/arcgis-online/reference/network-coverage.htm)\.

  Route calculators that use Esri as a data source only calculate routes that are shorter than 400 km\.
+ `Grab` – Grab provides routing functionality for Southeast Asia\. For additional information about [GrabMaps](https://docs.aws.amazon.com/location/latest/developerguide/grab.html)' coverage, see [GrabMaps countries and areas covered](https://docs.aws.amazon.com/location/latest/developerguide/grab.html#grab-coverage-area)\.
+ `Here` – For additional information about [HERE Technologies](https://docs.aws.amazon.com/location/latest/developerguide/HERE.html)' coverage in your region of interest, see [HERE car routing coverage](https://developer.here.com/documentation/routing-api/dev_guide/topics/coverage/car-routing.html) and [HERE truck routing coverage](https://developer.here.com/documentation/routing-api/dev_guide/topics/coverage/truck-routing.html)\.
For additional information , see [Data providers](https://docs.aws.amazon.com/location/latest/developerguide/what-is-data-provider.html) on the *Amazon Location Service Developer Guide*\.  
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
No longer used\. If included, the only allowed value is `RequestBasedUsage`\.  
*Allowed Values*: `RequestBasedUsage`  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-location-routecalculator-return-values"></a>

### Ref<a name="aws-resource-location-routecalculator-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `RouteCalculator` name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-location-routecalculator-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-location-routecalculator-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) for the route calculator resource\. Use the ARN when you specify a resource across all AWS\.  
+ Format example: `arn:aws:geo:region:account-id:route-calculator/ExampleCalculator`

`CalculatorArn`  <a name="CalculatorArn-fn::getatt"></a>
Synonym for `Arn`\. The Amazon Resource Name \(ARN\) for the route calculator resource\. Use the ARN when you specify a resource across all AWS\.  
+ Format example: `arn:aws:geo:region:account-id:route-calculator/ExampleCalculator`

`CreateTime`  <a name="CreateTime-fn::getatt"></a>
The timestamp for when the route calculator resource was created in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format: `YYYY-MM-DDThh:mm:ss.sssZ`\.

`UpdateTime`  <a name="UpdateTime-fn::getatt"></a>
The timestamp for when the route calculator resource was last updated in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format: `YYYY-MM-DDThh:mm:ss.sssZ`\.