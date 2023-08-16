# AWS::XRay::SamplingRule<a name="aws-resource-xray-samplingrule"></a>

Use the `AWS::XRay::SamplingRule` resource to specify a sampling rule, which controls sampling behavior for instrumented applications\. Include a `SamplingRule` entity to create or update a sampling rule\.

**Note**  
`SamplingRule.Version` can only be set when creating a sampling rule\. Updating the version will cause the update to fail\.

Services retrieve rules with [GetSamplingRules](https://docs.aws.amazon.com/xray/latest/api/API_GetSamplingRules.html), and evaluate each rule in ascending order of *priority* for each request\. If a rule matches, the service records a trace, borrowing it from the reservoir size\. After 10 seconds, the service reports back to X\-Ray with [GetSamplingTargets](https://docs.aws.amazon.com/xray/latest/api/API_GetSamplingTargets.html) to get updated versions of each in\-use rule\. The updated rule contains a trace quota that the service can use instead of borrowing from the reservoir\.

## Syntax<a name="aws-resource-xray-samplingrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-xray-samplingrule-syntax.json"></a>

```
{
  "Type" : "AWS::XRay::SamplingRule",
  "Properties" : {
      "[SamplingRule](#cfn-xray-samplingrule-samplingrule)" : SamplingRule,
      "[Tags](#cfn-xray-samplingrule-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-xray-samplingrule-syntax.yaml"></a>

```
Type: AWS::XRay::SamplingRule
Properties: 
  [SamplingRule](#cfn-xray-samplingrule-samplingrule): 
    SamplingRule
  [Tags](#cfn-xray-samplingrule-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-xray-samplingrule-properties"></a>

`SamplingRule`  <a name="cfn-xray-samplingrule-samplingrule"></a>
The sampling rule to be created or updated\.  
*Required*: No  
*Type*: [SamplingRule](aws-properties-xray-samplingrule-samplingrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-xray-samplingrule-tags"></a>
An array of key\-value pairs to apply to this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-xray-samplingrule-return-values"></a>

### Ref<a name="aws-resource-xray-samplingrule-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the Amazon Resource Name \(ARN\) of the sampling rule\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-xray-samplingrule-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

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
        "MySamplingRuleResource": {
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
   MySamplingRuleResource:
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
        "MySamplingRuleResource": {
         "Type": "AWS::XRay::SamplingRule",
         "Properties": {
            "SamplingRule": {
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
   MySamplingRuleResource:
      Type: AWS::XRay::SamplingRule
      Properties:
         SamplingRule:
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

