# AWS::ApiGateway::ApiKey<a name="aws-resource-apigateway-apikey"></a>

The `AWS::ApiGateway::ApiKey` resource creates a unique key that you can distribute to clients who are executing API Gateway `Method` resources that require an API key\. To specify which API key clients must use, map the API key with the `RestApi` and `Stage` resources that include the methods that require a key\. 

## Syntax<a name="aws-resource-apigateway-apikey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-apikey-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::ApiKey",
  "Properties" : {
      "[CustomerId](#cfn-apigateway-apikey-customerid)" : String,
      "[Description](#cfn-apigateway-apikey-description)" : String,
      "[Enabled](#cfn-apigateway-apikey-enabled)" : Boolean,
      "[GenerateDistinctId](#cfn-apigateway-apikey-generatedistinctid)" : Boolean,
      "[Name](#cfn-apigateway-apikey-name)" : String,
      "[StageKeys](#cfn-apigateway-apikey-stagekeys)" : [ StageKey, ... ],
      "[Tags](#cfn-apigateway-apikey-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Value](#cfn-apigateway-apikey-value)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-apikey-syntax.yaml"></a>

```
Type: AWS::ApiGateway::ApiKey
Properties: 
  [CustomerId](#cfn-apigateway-apikey-customerid): String
  [Description](#cfn-apigateway-apikey-description): String
  [Enabled](#cfn-apigateway-apikey-enabled): Boolean
  [GenerateDistinctId](#cfn-apigateway-apikey-generatedistinctid): Boolean
  [Name](#cfn-apigateway-apikey-name): String
  [StageKeys](#cfn-apigateway-apikey-stagekeys): 
    - StageKey
  [Tags](#cfn-apigateway-apikey-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Value](#cfn-apigateway-apikey-value): String
```

## Properties<a name="aws-resource-apigateway-apikey-properties"></a>

`CustomerId`  <a name="cfn-apigateway-apikey-customerid"></a>
An AWS Marketplace customer identifier to use when integrating with the AWS SaaS Marketplace\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigateway-apikey-description"></a>
A description of the purpose of the API key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-apigateway-apikey-enabled"></a>
Indicates whether the API key can be used by clients\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GenerateDistinctId`  <a name="cfn-apigateway-apikey-generatedistinctid"></a>
Specifies whether the key identifier is distinct from the created API key value\. This parameter is deprecated and should not be used\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-apigateway-apikey-name"></a>
A name for the API key\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the API key name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\. 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StageKeys`  <a name="cfn-apigateway-apikey-stagekeys"></a>
A list of stages to associate with this API key\.  
*Required*: No  
*Type*: List of [StageKey](aws-properties-apigateway-apikey-stagekey.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-apigateway-apikey-tags"></a>
An array of arbitrary tags \(key\-value pairs\) to associate with the API key\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-apigateway-apikey-value"></a>
The value of the API key\. Must be at least 20 characters long\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-apigateway-apikey-return-values"></a>

### Ref<a name="aws-resource-apigateway-apikey-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the API key ID, such as `m2m1k7sybf`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-apikey--examples"></a>



### API Key<a name="aws-resource-apigateway-apikey--examples--API_Key"></a>

The following example creates an API key and associates it with the `Test` stage of the `TestAPIDeployment` deployment\. To ensure that AWS CloudFormation creates the stage and deployment \(which are declared elsewhere in the same template\) before the API key, the example adds an explicit dependency on the deployment and stage\. Without this dependency, AWS CloudFormation might create the API key first, which would cause the association to fail because the deployment and stage wouldn't exist\.

#### JSON<a name="aws-resource-apigateway-apikey--examples--API_Key--json"></a>

```
{
    "ApiKey": {
        "Type": "AWS::ApiGateway::ApiKey",
        "DependsOn": [
            "TestAPIDeployment",
            "Test"
        ],
        "Properties": {
            "Name": "TestApiKey",
            "Description": "CloudFormation API Key V1",
            "Enabled": "true",
            "StageKeys": [
                {
                    "RestApiId": {
                        "Ref": "RestApi"
                    },
                    "StageName": "Test"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-apikey--examples--API_Key--yaml"></a>

```
ApiKey:
  Type: 'AWS::ApiGateway::ApiKey'
  DependsOn:
    - TestAPIDeployment
    - Test
  Properties:
    Name: TestApiKey
    Description: CloudFormation API Key V1
    Enabled: 'true'
    StageKeys:
      - RestApiId: !Ref RestApi
        StageName: Test
```

### Customer ID<a name="aws-resource-apigateway-apikey--examples--Customer_ID"></a>

The following example creates an API key, and enables you to specify a customer ID and whether to create a distinct ID\.

#### JSON<a name="aws-resource-apigateway-apikey--examples--Customer_ID--json"></a>

```
{
  "Parameters": {
    "apiKeyName": {
      "Type": "String"
    },
    "customerId": {
      "Type": "String"
    },
    "generateDistinctId": {
      "Type": "String"
    }
  },
  "Resources": {
    "ApiKey": {
      "Type": "AWS::ApiGateway::ApiKey",
      "Properties": {
        "CustomerId": {
          "Ref": "customerId"
        },
        "GenerateDistinctId": {
          "Ref": "generateDistinctId"
        },
        "Name": {
          "Ref": "apiKeyName"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-apigateway-apikey--examples--Customer_ID--yaml"></a>

```
Parameters:
  apiKeyName:
    Type: String
  customerId:
    Type: String
  generateDistinctId:
    Type: String
Resources:
  ApiKey:
    Type: AWS::ApiGateway::ApiKey
    Properties:
      CustomerId: !Ref customerId
      GenerateDistinctId: !Ref generateDistinctId
      Name: !Ref apiKeyName
```

## See also<a name="aws-resource-apigateway-apikey--seealso"></a>
+ [apikey:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/apikey-create/) in the *Amazon API Gateway REST API Reference*

