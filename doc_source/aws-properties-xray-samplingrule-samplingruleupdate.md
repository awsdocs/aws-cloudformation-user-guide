# AWS::XRay::SamplingRule SamplingRuleUpdate<a name="aws-properties-xray-samplingrule-samplingruleupdate"></a>

A document specifying changes to a sampling rule's configuration\.

## Syntax<a name="aws-properties-xray-samplingrule-samplingruleupdate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-xray-samplingrule-samplingruleupdate-syntax.json"></a>

```
{
  "[Attributes](#cfn-xray-samplingrule-samplingruleupdate-attributes)" : {Key : Value, ...},
  "[FixedRate](#cfn-xray-samplingrule-samplingruleupdate-fixedrate)" : Double,
  "[Host](#cfn-xray-samplingrule-samplingruleupdate-host)" : String,
  "[HTTPMethod](#cfn-xray-samplingrule-samplingruleupdate-httpmethod)" : String,
  "[Priority](#cfn-xray-samplingrule-samplingruleupdate-priority)" : Integer,
  "[ReservoirSize](#cfn-xray-samplingrule-samplingruleupdate-reservoirsize)" : Integer,
  "[ResourceARN](#cfn-xray-samplingrule-samplingruleupdate-resourcearn)" : String,
  "[RuleARN](#cfn-xray-samplingrule-samplingruleupdate-rulearn)" : String,
  "[RuleName](#cfn-xray-samplingrule-samplingruleupdate-rulename)" : String,
  "[ServiceName](#cfn-xray-samplingrule-samplingruleupdate-servicename)" : String,
  "[ServiceType](#cfn-xray-samplingrule-samplingruleupdate-servicetype)" : String,
  "[URLPath](#cfn-xray-samplingrule-samplingruleupdate-urlpath)" : String
}
```

### YAML<a name="aws-properties-xray-samplingrule-samplingruleupdate-syntax.yaml"></a>

```
  [Attributes](#cfn-xray-samplingrule-samplingruleupdate-attributes): 
    Key : Value
  [FixedRate](#cfn-xray-samplingrule-samplingruleupdate-fixedrate): Double
  [Host](#cfn-xray-samplingrule-samplingruleupdate-host): String
  [HTTPMethod](#cfn-xray-samplingrule-samplingruleupdate-httpmethod): String
  [Priority](#cfn-xray-samplingrule-samplingruleupdate-priority): Integer
  [ReservoirSize](#cfn-xray-samplingrule-samplingruleupdate-reservoirsize): Integer
  [ResourceARN](#cfn-xray-samplingrule-samplingruleupdate-resourcearn): String
  [RuleARN](#cfn-xray-samplingrule-samplingruleupdate-rulearn): String
  [RuleName](#cfn-xray-samplingrule-samplingruleupdate-rulename): String
  [ServiceName](#cfn-xray-samplingrule-samplingruleupdate-servicename): String
  [ServiceType](#cfn-xray-samplingrule-samplingruleupdate-servicetype): String
  [URLPath](#cfn-xray-samplingrule-samplingruleupdate-urlpath): String
```

## Properties<a name="aws-properties-xray-samplingrule-samplingruleupdate-properties"></a>

`Attributes`  <a name="cfn-xray-samplingrule-samplingruleupdate-attributes"></a>
Matches attributes derived from the request\.  
*Map Entries:* Maximum number of 5 items\.  
*Key Length Constraints:* Minimum length of 1\. Maximum length of 32\.  
*Value Length Constraints:* Minimum length of 1\. Maximum length of 32\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FixedRate`  <a name="cfn-xray-samplingrule-samplingruleupdate-fixedrate"></a>
The percentage of matching requests to instrument, after the reservoir is exhausted\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Host`  <a name="cfn-xray-samplingrule-samplingruleupdate-host"></a>
Matches the hostname from a request URL\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HTTPMethod`  <a name="cfn-xray-samplingrule-samplingruleupdate-httpmethod"></a>
Matches the HTTP method of a request\.  
*Required*: No  
*Type*: String  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Priority`  <a name="cfn-xray-samplingrule-samplingruleupdate-priority"></a>
The priority of the sampling rule\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReservoirSize`  <a name="cfn-xray-samplingrule-samplingruleupdate-reservoirsize"></a>
A fixed number of matching requests to instrument per second, prior to applying the fixed rate\. The reservoir is not used directly by services, but applies to all services using the rule collectively\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceARN`  <a name="cfn-xray-samplingrule-samplingruleupdate-resourcearn"></a>
Matches the ARN of the AWS resource on which the service runs\.  
*Required*: No  
*Type*: String  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleARN`  <a name="cfn-xray-samplingrule-samplingruleupdate-rulearn"></a>
The ARN of the sampling rule\. You must specify either RuleARN or RuleName, but not both\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleName`  <a name="cfn-xray-samplingrule-samplingruleupdate-rulename"></a>
The name of the sampling rule\. You must specify either RuleARN or RuleName, but not both\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-xray-samplingrule-samplingruleupdate-servicename"></a>
Matches the `name` that the service uses to identify itself in segments\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceType`  <a name="cfn-xray-samplingrule-samplingruleupdate-servicetype"></a>
Matches the `origin` that the service uses to identify its type in segments\.  
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`URLPath`  <a name="cfn-xray-samplingrule-samplingruleupdate-urlpath"></a>
Matches the path from a request URL\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)