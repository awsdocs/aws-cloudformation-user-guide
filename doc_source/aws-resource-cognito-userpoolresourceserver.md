# AWS::Cognito::UserPoolResourceServer<a name="aws-resource-cognito-userpoolresourceserver"></a>

The `AWS::Cognito::UserPoolResourceServer` resource creates a new OAuth2\.0 resource server and defines custom scopes in it\.

## Syntax<a name="aws-resource-cognito-userpoolresourceserver-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cognito-userpoolresourceserver-syntax.json"></a>

```
{
  "Type" : "AWS::Cognito::UserPoolResourceServer",
  "Properties" : {
      "[Identifier](#cfn-cognito-userpoolresourceserver-identifier)" : String,
      "[Name](#cfn-cognito-userpoolresourceserver-name)" : String,
      "[Scopes](#cfn-cognito-userpoolresourceserver-scopes)" : [ ResourceServerScopeType, ... ],
      "[UserPoolId](#cfn-cognito-userpoolresourceserver-userpoolid)" : String
    }
}
```

### YAML<a name="aws-resource-cognito-userpoolresourceserver-syntax.yaml"></a>

```
Type: AWS::Cognito::UserPoolResourceServer
Properties: 
  [Identifier](#cfn-cognito-userpoolresourceserver-identifier): String
  [Name](#cfn-cognito-userpoolresourceserver-name): String
  [Scopes](#cfn-cognito-userpoolresourceserver-scopes): 
    - ResourceServerScopeType
  [UserPoolId](#cfn-cognito-userpoolresourceserver-userpoolid): String
```

## Properties<a name="aws-resource-cognito-userpoolresourceserver-properties"></a>

`Identifier`  <a name="cfn-cognito-userpoolresourceserver-identifier"></a>
A unique resource server identifier for the resource server\. This could be an HTTPS endpoint where the resource server is located\. For example: `https://my-weather-api.example.com`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\x21\x23-\x5B\x5D-\x7E]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-cognito-userpoolresourceserver-name"></a>
A friendly name for the resource server\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[\w\s+=,.@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scopes`  <a name="cfn-cognito-userpoolresourceserver-scopes"></a>
The scopes\. Each scope is a map, where the keys are `name` and the values are `description` for the scope\.  
*Required*: No  
*Type*: List of [ResourceServerScopeType](aws-properties-cognito-userpoolresourceserver-resourceserverscopetype.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserPoolId`  <a name="cfn-cognito-userpoolresourceserver-userpoolid"></a>
The user pool ID for the user pool\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `55`  
*Pattern*: `[\w-]+_[0-9a-zA-Z]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-cognito-userpoolresourceserver-return-values"></a>

### Ref<a name="aws-resource-cognito-userpoolresourceserver-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns physicalResourceId, which is the resource server identifier “Identifier"\. For example:

 `{ "Ref": "yourResourceServerIdentifier" }` 

For the Amazon Cognito resource server `yourResourceServerIdentifier`, Ref returns the name of the resource server\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-cognito-userpoolresourceserver--examples"></a>



### Creating a new resource server for a user pool<a name="aws-resource-cognito-userpoolresourceserver--examples--Creating_a_new_resource_server_for_a_user_pool"></a>

The following example creates a resource server "Name" with the identifier "Identifier" in the referenced user pool\.

#### JSON<a name="aws-resource-cognito-userpoolresourceserver--examples--Creating_a_new_resource_server_for_a_user_pool--json"></a>

```
{
	"UserPoolResourceServer": {
		"Type": "AWS::Cognito::UserPoolResourceServer",
		"Properties": {
			"UserPoolId": {
				"Ref": "UserPool"
			},
			"Identifier": "Identifier",
			"Name": "Name",
			"Scopes": [{
				"ScopeName": "ScopeName1",
				"ScopeDescription": "description"
			}, {
				"ScopeName": "ScopeName2",
				"ScopeDescription": "description"
			}]
		}
	}
}
```

#### YAML<a name="aws-resource-cognito-userpoolresourceserver--examples--Creating_a_new_resource_server_for_a_user_pool--yaml"></a>

```
UserPoolResourceServer: 
  Type: AWS::Cognito::UserPoolResourceServer
  Properties: 
    UserPoolId: !Ref UserPool 
    Identifier: "Identifier" 
    Name: "Name" 
    Scopes: 
     - ScopeName: "ScopeName1" 
       ScopeDescription: "description" 
     - ScopeName: "ScopeName2"
       ScopeDescription: "description"
```