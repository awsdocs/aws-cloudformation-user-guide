# AWS::AppSync::ApiKey<a name="aws-resource-appsync-apikey"></a>

The `AWS::AppSync::ApiKey` resource creates a unique key that you can distribute to clients who are executing GraphQL operations with AWS AppSync that require an API key\. 

**Topics**
+ [Syntax](#aws-resource-appsync-apikey-syntax)
+ [Properties](#aws-resource-appsync-apikey-properties)
+ [Return Values](#aws-resource-appsync-apikey-returnvalues)
+ [Examples](#aws-resource-appsync-apikey-examples)
+ [See Also](#aws-resource-appsync-apikey-seealso)

## Syntax<a name="aws-resource-appsync-apikey-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-apikey-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::ApiKey",
  "Properties" : {
    "[Description](#cfn-appsync-apikey-description)" : String,
    "[Expires](#cfn-appsync-apikey-expires)" : Number,
    "[ApiId](#cfn-appsync-apikey-apiid)" : String
  }
}
```

### YAML<a name="aws-resource-appsync-apikey-syntax.yaml"></a>

```
Type: "AWS::AppSync::ApiKey"
Properties:
  [Description](#cfn-appsync-apikey-description): String
  [Expires](#cfn-appsync-apikey-expires): Number
  [ApiId](#cfn-appsync-apikey-apiid): String
```

## Properties<a name="aws-resource-appsync-apikey-properties"></a>

`Description`  <a name="cfn-appsync-apikey-description"></a>
Unique description of your API Key\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Expires`  <a name="cfn-appsync-apikey-expires"></a>
Expiration time of the API Key in seconds \(using Unix Epoch time\), with a minimum of 1 day and a maximum of 365 days\.  
 *Required*: Yes  
 *Type*: Number  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ApiId`  <a name="cfn-appsync-apikey-apiid"></a>
Unique AWS AppSync GraphQL API Identifier for this API Key\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-appsync-apikey-returnvalues"></a>

### Ref<a name="aws-resource-appsync-apikey-ref"></a>

When you pass the logical ID of an `AWS::AppSync::ApiKey` resource to the intrinsic `Ref` function, the function returns the ARN of the API Key, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/apikey/apikeya1bzhi`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-appsync-apikey-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`ApiKey`  
The API key\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the API key, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/apikey/apikeya1bzhi`\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-appsync-apikey-examples"></a>

### API Key creation example<a name="aws-resource-appsync-apikey-example1"></a>

The following example creates an API Key and associates it with an existing GraphQL API by passing the GraphQL API Id as a paramater\.

#### JSON<a name="aws-resource-appsync-apikey-example1.json"></a>

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

#### YAML<a name="aws-resource-appsync-apikey-example1.yaml"></a>

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
    Type: "AWS::AppSync::ApiKey"
    Properties:
      ApiId:
	Ref: graphQlApiId
      Description:
        Ref: apiKeyDescription
      Expires:
        Ref: apiKeyExpires
```

## See Also<a name="aws-resource-appsync-apikey-seealso"></a>
+ [ CreateApiKey](http://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateApiKey.html) operation in the *AWS AppSync API Reference*