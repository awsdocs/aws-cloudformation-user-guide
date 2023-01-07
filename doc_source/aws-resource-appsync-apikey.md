# AWS::AppSync::ApiKey<a name="aws-resource-appsync-apikey"></a>

The `AWS::AppSync::ApiKey` resource creates a unique key that you can distribute to clients who are executing GraphQL operations with AWS AppSync that require an API key\.

## Syntax<a name="aws-resource-appsync-apikey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-apikey-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::ApiKey",
  "Properties" : {
      "[ApiId](#cfn-appsync-apikey-apiid)" : String,
      "[ApiKeyId](#cfn-appsync-apikey-apikeyid)" : String,
      "[Description](#cfn-appsync-apikey-description)" : String,
      "[Expires](#cfn-appsync-apikey-expires)" : Double
    }
}
```

### YAML<a name="aws-resource-appsync-apikey-syntax.yaml"></a>

```
Type: AWS::AppSync::ApiKey
Properties: 
  [ApiId](#cfn-appsync-apikey-apiid): String
  [ApiKeyId](#cfn-appsync-apikey-apikeyid): String
  [Description](#cfn-appsync-apikey-description): String
  [Expires](#cfn-appsync-apikey-expires): Double
```

## Properties<a name="aws-resource-appsync-apikey-properties"></a>

`ApiId`  <a name="cfn-appsync-apikey-apiid"></a>
Unique AWS AppSync GraphQL API ID for this API key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ApiKeyId`  <a name="cfn-appsync-apikey-apikeyid"></a>
The API key ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-appsync-apikey-description"></a>
Unique description of your API key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expires`  <a name="cfn-appsync-apikey-expires"></a>
The time after which the API key expires\. The date is represented as seconds since the epoch, rounded down to the nearest hour\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appsync-apikey-return-values"></a>

### Ref<a name="aws-resource-appsync-apikey-return-values-ref"></a>

When you pass the logical ID of an `AWS::AppSync::ApiKey` resource to the intrinsic `Ref` function, the function returns the ARN of the API key, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/apikey/apikeya1bzhi`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref)\.

### Fn::GetAtt<a name="aws-resource-appsync-apikey-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt)\. 

#### <a name="aws-resource-appsync-apikey-return-values-fn--getatt-fn--getatt"></a>

`ApiKey`  <a name="ApiKey-fn::getatt"></a>
The API key\.

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the API key, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/apikey/apikeya1bzhi`\.

## Examples<a name="aws-resource-appsync-apikey--examples"></a>



### API Key Creation Example<a name="aws-resource-appsync-apikey--examples--API_Key_Creation_Example"></a>

The following example creates an API key and associates it with an existing GraphQL API by passing the GraphQL API ID as a parameter\. 

#### YAML<a name="aws-resource-appsync-apikey--examples--API_Key_Creation_Example--yaml"></a>

```
Parameters:
  graphQlApiId:
    Type: String
  apiKeyDescription:
    Type: String
  apiKeyExpires:
    Type: Number
Resources:
  ApiKey:
    Type: AWS::AppSync::ApiKey
    Properties:
      ApiId:
	Ref: graphQlApiId
      Description:
        Ref: apiKeyDescription
      Expires:
        Ref: apiKeyExpires
```

#### JSON<a name="aws-resource-appsync-apikey--examples--API_Key_Creation_Example--json"></a>

```
{
  "Parameters": {
    "graphQlApiId": {
      "Type": "String"
    },
    "apiKeyDescription": {
      "Type": "String"
    },
    "apiKeyExpires": {
      "Type": "Number"
    }
  },
  "Resources": {
    "ApiKey": {
      "Type": "AWS::AppSync::ApiKey",
      "Properties": {
        "ApiId": {
           "Ref": "graphQlApiId"
        },
        "Description": {
          "Ref": "apiKeyDescription"
        },
        "Expires": {
          "Ref": "apiKeyExpires"
        }
      }
    }
  }
}
```

## See also<a name="aws-resource-appsync-apikey--seealso"></a>
+  [CreateApiKey](https://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateApiKey.html) operation in the *AWS AppSync API Reference*\.

