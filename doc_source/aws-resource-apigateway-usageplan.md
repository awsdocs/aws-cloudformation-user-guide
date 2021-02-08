# AWS::ApiGateway::UsagePlan<a name="aws-resource-apigateway-usageplan"></a>

The `AWS::ApiGateway::UsagePlan` resource creates a usage plan for deployed APIs\. A usage plan enforces throttling and quota limits on individual client API keys\. For more information, see [Creating and Using API Usage Plans in Amazon API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-api-usage-plans.html) in the *API Gateway Developer Guide*\.

## Syntax<a name="aws-resource-apigateway-usageplan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-usageplan-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::UsagePlan",
  "Properties" : {
      "[ApiStages](#cfn-apigateway-usageplan-apistages)" : [ ApiStage, ... ],
      "[Description](#cfn-apigateway-usageplan-description)" : String,
      "[Quota](#cfn-apigateway-usageplan-quota)" : QuotaSettings,
      "[Tags](#cfn-apigateway-usageplan-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Throttle](#cfn-apigateway-usageplan-throttle)" : ThrottleSettings,
      "[UsagePlanName](#cfn-apigateway-usageplan-usageplanname)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-usageplan-syntax.yaml"></a>

```
Type: AWS::ApiGateway::UsagePlan
Properties: 
  [ApiStages](#cfn-apigateway-usageplan-apistages): 
    - ApiStage
  [Description](#cfn-apigateway-usageplan-description): String
  [Quota](#cfn-apigateway-usageplan-quota): 
    QuotaSettings
  [Tags](#cfn-apigateway-usageplan-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Throttle](#cfn-apigateway-usageplan-throttle): 
    ThrottleSettings
  [UsagePlanName](#cfn-apigateway-usageplan-usageplanname): String
```

## Properties<a name="aws-resource-apigateway-usageplan-properties"></a>

`ApiStages`  <a name="cfn-apigateway-usageplan-apistages"></a>
The API stages to associate with this usage plan\.  
*Required*: No  
*Type*: List of [ApiStage](aws-properties-apigateway-usageplan-apistage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigateway-usageplan-description"></a>
A description of the usage plan\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Quota`  <a name="cfn-apigateway-usageplan-quota"></a>
Configures the number of requests that users can make within a given interval\.  
*Required*: No  
*Type*: [QuotaSettings](aws-properties-apigateway-usageplan-quotasettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-apigateway-usageplan-tags"></a>
An array of arbitrary tags \(key\-value pairs\) to associate with the usage plan\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Throttle`  <a name="cfn-apigateway-usageplan-throttle"></a>
Configures the overall request rate \(average requests per second\) and burst capacity\.  
*Required*: No  
*Type*: [ThrottleSettings](aws-properties-apigateway-usageplan-throttlesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UsagePlanName`  <a name="cfn-apigateway-usageplan-usageplanname"></a>
A name for the usage plan\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigateway-usageplan-return-values"></a>

### Ref<a name="aws-resource-apigateway-usageplan-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the usage plan ID, such as `abc123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-usageplan--examples"></a>



### Create usage plan<a name="aws-resource-apigateway-usageplan--examples--Create_usage_plan"></a>

The following examples create a usage plan for the Prod API stage, with a quota of 5000 requests per month and a rate limit of 100 requests per second\.

#### JSON<a name="aws-resource-apigateway-usageplan--examples--Create_usage_plan--json"></a>

```
{
    "usagePlan": {
        "Type": "AWS::ApiGateway::UsagePlan",
        "Properties": {
            "ApiStages": [
                {
                    "ApiId": {
                        "Ref": "MyRestApi"
                    },
                    "Stage": {
                        "Ref": "Prod"
                    }
                }
            ],
            "Description": "Customer ABC's usage plan",
            "Quota": {
                "Limit": 5000,
                "Period": "MONTH"
            },
            "Throttle": {
                "BurstLimit": 200,
                "RateLimit": 100
            },
            "UsagePlanName": "Plan_ABC"
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-usageplan--examples--Create_usage_plan--yaml"></a>

```
usagePlan:
  Type: 'AWS::ApiGateway::UsagePlan'
  Properties:
    ApiStages:
      - ApiId: !Ref MyRestApi
        Stage: !Ref Prod
    Description: Customer ABC's usage plan
    Quota:
      Limit: 5000
      Period: MONTH
    Throttle:
      BurstLimit: 200
      RateLimit: 100
    UsagePlanName: Plan_ABC
```

## See also<a name="aws-resource-apigateway-usageplan--seealso"></a>
+ [usageplan:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/usageplan-create/) in the *Amazon API Gateway REST API Reference*

