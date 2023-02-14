# AWS::XRay::SamplingRule SamplingRule<a name="aws-properties-xray-samplingrule-samplingrule"></a>

A sampling rule that services use to decide whether to instrument a request\. Rule fields can match properties of the service, or properties of a request\. The service can ignore rules that don't match its properties\.

## Syntax<a name="aws-properties-xray-samplingrule-samplingrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-xray-samplingrule-samplingrule-syntax.json"></a>

```
{
  "[Attributes](#cfn-xray-samplingrule-samplingrule-attributes)" : {Key : Value, ...},
  "[FixedRate](#cfn-xray-samplingrule-samplingrule-fixedrate)" : Double,
  "[Host](#cfn-xray-samplingrule-samplingrule-host)" : String,
  "[HTTPMethod](#cfn-xray-samplingrule-samplingrule-httpmethod)" : String,
  "[Priority](#cfn-xray-samplingrule-samplingrule-priority)" : Integer,
  "[ReservoirSize](#cfn-xray-samplingrule-samplingrule-reservoirsize)" : Integer,
  "[ResourceARN](#cfn-xray-samplingrule-samplingrule-resourcearn)" : String,
  "[RuleARN](#cfn-xray-samplingrule-samplingrule-rulearn)" : String,
  "[RuleName](#cfn-xray-samplingrule-samplingrule-rulename)" : String,
  "[ServiceName](#cfn-xray-samplingrule-samplingrule-servicename)" : String,
  "[ServiceType](#cfn-xray-samplingrule-samplingrule-servicetype)" : String,
  "[URLPath](#cfn-xray-samplingrule-samplingrule-urlpath)" : String,
  "[Version](#cfn-xray-samplingrule-samplingrule-version)" : Integer
}
```

### YAML<a name="aws-properties-xray-samplingrule-samplingrule-syntax.yaml"></a>

```
  [Attributes](#cfn-xray-samplingrule-samplingrule-attributes): 
    Key : Value
  [FixedRate](#cfn-xray-samplingrule-samplingrule-fixedrate): Double
  [Host](#cfn-xray-samplingrule-samplingrule-host): String
  [HTTPMethod](#cfn-xray-samplingrule-samplingrule-httpmethod): String
  [Priority](#cfn-xray-samplingrule-samplingrule-priority): Integer
  [ReservoirSize](#cfn-xray-samplingrule-samplingrule-reservoirsize): Integer
  [ResourceARN](#cfn-xray-samplingrule-samplingrule-resourcearn): String
  [RuleARN](#cfn-xray-samplingrule-samplingrule-rulearn): String
  [RuleName](#cfn-xray-samplingrule-samplingrule-rulename): String
  [ServiceName](#cfn-xray-samplingrule-samplingrule-servicename): String
  [ServiceType](#cfn-xray-samplingrule-samplingrule-servicetype): String
  [URLPath](#cfn-xray-samplingrule-samplingrule-urlpath): String
  [Version](#cfn-xray-samplingrule-samplingrule-version): Integer
```

## Properties<a name="aws-properties-xray-samplingrule-samplingrule-properties"></a>

`Attributes`  <a name="cfn-xray-samplingrule-samplingrule-attributes"></a>
Matches attributes derived from the request\.  
*Map Entries:* Maximum number of 5 items\.  
*Key Length Constraints:* Minimum length of 1\. Maximum length of 32\.  
*Value Length Constraints:* Minimum length of 1\. Maximum length of 32\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FixedRate`  <a name="cfn-xray-samplingrule-samplingrule-fixedrate"></a>
The percentage of matching requests to instrument, after the reservoir is exhausted\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-xray-samplingrule-samplingrule-host"></a>
Matches the hostname from a request URL\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HTTPMethod`  <a name="cfn-xray-samplingrule-samplingrule-httpmethod"></a>
Matches the HTTP method of a request\.  
*Required*: No  
*Type*: String  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-xray-samplingrule-samplingrule-priority"></a>
The priority of the sampling rule\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `9999`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReservoirSize`  <a name="cfn-xray-samplingrule-samplingrule-reservoirsize"></a>
A fixed number of matching requests to instrument per second, prior to applying the fixed rate\. The reservoir is not used directly by services, but applies to all services using the rule collectively\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceARN`  <a name="cfn-xray-samplingrule-samplingrule-resourcearn"></a>
Matches the ARN of the AWS resource on which the service runs\.  
*Required*: No  
*Type*: String  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleARN`  <a name="cfn-xray-samplingrule-samplingrule-rulearn"></a>
The ARN of the sampling rule\. You must specify either RuleARN or RuleName, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleName`  <a name="cfn-xray-samplingrule-samplingrule-rulename"></a>
The name of the sampling rule\. You must specify either RuleARN or RuleName, but not both\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-xray-samplingrule-samplingrule-servicename"></a>
Matches the `name` that the service uses to identify itself in segments\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceType`  <a name="cfn-xray-samplingrule-samplingrule-servicetype"></a>
Matches the `origin` that the service uses to identify its type in segments\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`URLPath`  <a name="cfn-xray-samplingrule-samplingrule-urlpath"></a>
Matches the path from a request URL\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-xray-samplingrule-samplingrule-version"></a>
The version of the sampling rule format \(`1`\)\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)