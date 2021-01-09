# AWS::ApiGateway::UsagePlanKey<a name="aws-resource-apigateway-usageplankey"></a>

The `AWS::ApiGateway::UsagePlanKey` resource associates an API key with a usage plan\. This association determines which users the usage plan is applied to\.

## Syntax<a name="aws-resource-apigateway-usageplankey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-usageplankey-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::UsagePlanKey",
  "Properties" : {
      "[KeyId](#cfn-apigateway-usageplankey-keyid)" : String,
      "[KeyType](#cfn-apigateway-usageplankey-keytype)" : String,
      "[UsagePlanId](#cfn-apigateway-usageplankey-usageplanid)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-usageplankey-syntax.yaml"></a>

```
Type: AWS::ApiGateway::UsagePlanKey
Properties: 
  [KeyId](#cfn-apigateway-usageplankey-keyid): String
  [KeyType](#cfn-apigateway-usageplankey-keytype): String
  [UsagePlanId](#cfn-apigateway-usageplankey-usageplanid): String
```

## Properties<a name="aws-resource-apigateway-usageplankey-properties"></a>

`KeyId`  <a name="cfn-apigateway-usageplankey-keyid"></a>
The ID of the usage plan key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyType`  <a name="cfn-apigateway-usageplankey-keytype"></a>
The type of usage plan key\. Currently, the only valid key type is `API_KEY`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UsagePlanId`  <a name="cfn-apigateway-usageplankey-usageplanid"></a>
The ID of the usage plan\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-apigateway-usageplankey-return-values"></a>

### Ref<a name="aws-resource-apigateway-usageplankey-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the key and ID of the usage plan combined with a ":", such as `123abcdef:abc123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-usageplankey--examples"></a>



### Create usage plan key<a name="aws-resource-apigateway-usageplankey--examples--Create_usage_plan_key"></a>



#### JSON<a name="aws-resource-apigateway-usageplankey--examples--Create_usage_plan_key--json"></a>

```
{
    "usagePlanKey": {
        "Type": "AWS::ApiGateway::UsagePlanKey",
        "Properties": {
            "KeyId": {
                "Ref": "myApiKey"
            },
            "KeyType": "API_KEY",
            "UsagePlanId": {
                "Ref": "myUsagePlan"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-usageplankey--examples--Create_usage_plan_key--yaml"></a>

```
usagePlanKey:
  Type: 'AWS::ApiGateway::UsagePlanKey'
  Properties:
    KeyId: !Ref myApiKey
    KeyType: API_KEY
    UsagePlanId: !Ref myUsagePlan
```

## See also<a name="aws-resource-apigateway-usageplankey--seealso"></a>
+ [usageplankey:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/usageplankey-create/) in the *Amazon API Gateway REST API Reference*

