# AWS::XRay::SamplingRule<a name="aws-resource-xray-samplingrule"></a>

Use the `AWS::XRay::SamplingRule` resource to specify a sampling rule, which controls sampling behavior for instrumented applications\. A new sampling rule is created by specifying a `SamplingRule`\. To change the configuration of an existing sampling rule, specify a `SamplingRuleUpdate`\. 

Services retrieve rules with [GetSamplingRules](https://docs.aws.amazon.com/xray/latest/api/API_GetSamplingRules.html), and evaluate each rule in ascending order of *priority* for each request\. If a rule matches, the service records a trace, borrowing it from the reservoir size\. After 10 seconds, the service reports back to X\-Ray with [GetSamplingTargets](https://docs.aws.amazon.com/xray/latest/api/API_GetSamplingTargets.html) to get updated versions of each in\-use rule\. The updated rule contains a trace quota that the service can use instead of borrowing from the reservoir\. 

## Syntax<a name="aws-resource-xray-samplingrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-xray-samplingrule-syntax.json"></a>

```
{
  "Type" : "AWS::XRay::SamplingRule",
  "Properties" : {
      "[RuleName](#cfn-xray-samplingrule-rulename)" : String,
      "[SamplingRule](#cfn-xray-samplingrule-samplingrule)" : SamplingRule,
      "[SamplingRuleRecord](#cfn-xray-samplingrule-samplingrulerecord)" : SamplingRuleRecord,
      "[SamplingRuleUpdate](#cfn-xray-samplingrule-samplingruleupdate)" : SamplingRuleUpdate,
      "[Tags](#cfn-xray-samplingrule-tags)" : [ TagsItems, ... ]
    }
}
```

### YAML<a name="aws-resource-xray-samplingrule-syntax.yaml"></a>

```
Type: AWS::XRay::SamplingRule
Properties: 
  [RuleName](#cfn-xray-samplingrule-rulename): String
  [SamplingRule](#cfn-xray-samplingrule-samplingrule): 
    SamplingRule
  [SamplingRuleRecord](#cfn-xray-samplingrule-samplingrulerecord): 
    SamplingRuleRecord
  [SamplingRuleUpdate](#cfn-xray-samplingrule-samplingruleupdate): 
    SamplingRuleUpdate
  [Tags](#cfn-xray-samplingrule-tags): 
    - TagsItems
```

## Properties<a name="aws-resource-xray-samplingrule-properties"></a>

`RuleName`  <a name="cfn-xray-samplingrule-rulename"></a>
The name of the sampling rule\. Specify a rule by either name or ARN, but not both\. Used only when deleting a sampling rule\. When creating or updating a sampling rule, use the `RuleName` or `RuleARN` properties within `SamplingRule` or `SamplingRuleUpdate`\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamplingRule`  <a name="cfn-xray-samplingrule-samplingrule"></a>
The sampling rule to be created\.  
Must be provided if creating a new sampling rule\. Not valid when updating an existing sampling rule\.  
*Required*: Conditional  
*Type*: [SamplingRule](aws-properties-xray-samplingrule-samplingrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamplingRuleRecord`  <a name="cfn-xray-samplingrule-samplingrulerecord"></a>
Property description not available\.  
*Required*: No  
*Type*: [SamplingRuleRecord](aws-properties-xray-samplingrule-samplingrulerecord.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SamplingRuleUpdate`  <a name="cfn-xray-samplingrule-samplingruleupdate"></a>
A document specifying changes to a sampling rule's configuration\.  
Must be provided if updating an existing sampling rule\. Not valid when creating a new sampling rule\.  
The `Version` of a sampling rule cannot be updated, and is not part of `SamplingRuleUpdate`\.
*Required*: Conditional  
*Type*: [SamplingRuleUpdate](aws-properties-xray-samplingrule-samplingruleupdate.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-xray-samplingrule-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [TagsItems](aws-properties-xray-samplingrule-tagsitems.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-xray-samplingrule-return-values"></a>

### Fn::GetAtt<a name="aws-resource-xray-samplingrule-return-values-fn--getatt"></a>

#### <a name="aws-resource-xray-samplingrule-return-values-fn--getatt-fn--getatt"></a>

`RuleARN`  <a name="RuleARN-fn::getatt"></a>
The sampling rule ARN that was created or updated\.

## Examples<a name="aws-resource-xray-samplingrule--examples"></a>



### Create sampling rule<a name="aws-resource-xray-samplingrule--examples--Create_sampling_rule"></a>

This example creates a new sampling rule called MySamplingRule\.

#### JSON<a name="aws-resource-xray-samplingrule--examples--Create_sampling_rule--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09T00:00:00.000Z",
   "Resources": {
        "SamplingRule": {
         "Type": "AWS::XRay::SamplingRule",
         "Properties": {
            "SamplingRule": {
               "RuleName": "MySamplingRule",
               "ResourceARN": "*",
               "Priority": 2,
               "FixedRate": 0.05,
               "ReservoirSize": 50,
               "ServiceName": "MyServiceName",
               "ServiceType": "MyServiceType",
               "Host": "MyHost",
               "HTTPMethod": "GET",
               "URLPath": "*",
               "Version": 1
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-xray-samplingrule--examples--Create_sampling_rule--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
   SamplingRule:
      Type: AWS::XRay::SamplingRule
      Properties:
         SamplingRule:
            RuleName: MySamplingRule
            ResourceARN: "*"
            Priority: 2
            FixedRate: 0.05
            ReservoirSize: 50
            ServiceName: "MyServiceName"
            ServiceType: "MyServiceType"
            Host: "MyHost"
            HTTPMethod: "GET"
            URLPath: "*"
            Version: 1
```

### Update sampling rule<a name="aws-resource-xray-samplingrule--examples--Update_sampling_rule"></a>

This example updates an existing sampling rule called MySamplingRule\.

#### JSON<a name="aws-resource-xray-samplingrule--examples--Update_sampling_rule--json"></a>

```
{
   "AWSTemplateFormatVersion": "2010-09-09T00:00:00.000Z",
   "Resources": {
        "SamplingRule": {
         "Type": "AWS::XRay::SamplingRule",
         "Properties": {
            "SamplingRuleUpdate": {
               "RuleName": "MySamplingRule",
               "ResourceARN": "*",
               "Priority": 1,
               "FixedRate": 0.07,
               "ReservoirSize": 20,
               "ServiceName": "MyServiceName",
               "ServiceType": "MyServiceType",
               "Host": "MyHost",
               "HTTPMethod": "GET",
               "URLPath": "*"
            }
         }
      }
   }
}
```

#### YAML<a name="aws-resource-xray-samplingrule--examples--Update_sampling_rule--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
   SamplingRule:
      Type: AWS::XRay::SamplingRule
      Properties:
         SamplingRuleUpdate:
            RuleName: MySamplingRule
            ResourceARN: "*"
            Priority: 1
            FixedRate: 0.07
            ReservoirSize: 20
            ServiceName: "MyServiceName"
            ServiceType: "MyServiceType"
            Host: "MyHost"
            HTTPMethod: "GET"
            URLPath: "*"
```

## See also<a name="aws-resource-xray-samplingrule--seealso"></a>
+ [Configuring sampling rules in the X\-Ray console](https://docs.aws.amazon.com/xray/latest/devguide/xray-console-sampling.html)
+ [Using sampling rules with the X\-Ray API](https://docs.aws.amazon.com/xray/latest/devguide/xray-api-sampling.html)
+ [CreateSamplingRule](https://docs.aws.amazon.com/xray/latest/api/API_CreateSamplingRule.html) action in the X\-Ray API Reference

