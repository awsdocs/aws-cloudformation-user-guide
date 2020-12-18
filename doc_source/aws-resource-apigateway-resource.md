# AWS::ApiGateway::Resource<a name="aws-resource-apigateway-resource"></a>

The `AWS::ApiGateway::Resource` resource creates a resource in an API\.

## Syntax<a name="aws-resource-apigateway-resource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-resource-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::Resource",
  "Properties" : {
      "[ParentId](#cfn-apigateway-resource-parentid)" : String,
      "[PathPart](#cfn-apigateway-resource-pathpart)" : String,
      "[RestApiId](#cfn-apigateway-resource-restapiid)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-resource-syntax.yaml"></a>

```
Type: AWS::ApiGateway::Resource
Properties: 
  [ParentId](#cfn-apigateway-resource-parentid): String
  [PathPart](#cfn-apigateway-resource-pathpart): String
  [RestApiId](#cfn-apigateway-resource-restapiid): String
```

## Properties<a name="aws-resource-apigateway-resource-properties"></a>

`ParentId`  <a name="cfn-apigateway-resource-parentid"></a>
If you want to create a child resource, the ID of the parent resource\. For resources without a parent, specify the `RestApi` root resource ID, such as `{ "Fn::GetAtt": ["MyRestApi", "RootResourceId"] }`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PathPart`  <a name="cfn-apigateway-resource-pathpart"></a>
A path name for the resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestApiId`  <a name="cfn-apigateway-resource-restapiid"></a>
The ID of the [RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html) resource in which you want to create this resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-apigateway-resource-return-values"></a>

### Ref<a name="aws-resource-apigateway-resource-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ID, such as `abc123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigateway-resource--examples"></a>



### Create resource<a name="aws-resource-apigateway-resource--examples--Create_resource"></a>

The following example creates a `stack` resource for the `MyApi` API\.

#### JSON<a name="aws-resource-apigateway-resource--examples--Create_resource--json"></a>

```
{
    "Stack": {
        "Type": "AWS::ApiGateway::Resource",
        "Properties": {
            "RestApiId": {
                "Ref": "MyApi"
            },
            "ParentId": {
                "Fn::GetAtt": [
                    "MyApi",
                    "RootResourceId"
                ]
            },
            "PathPart": "stack"
        }
    }
}
```

#### YAML<a name="aws-resource-apigateway-resource--examples--Create_resource--yaml"></a>

```
Stack:
  Type: 'AWS::ApiGateway::Resource'
  Properties:
    RestApiId: !Ref MyApi
    ParentId: !GetAtt 
      - MyApi
      - RootResourceId
    PathPart: stack
```

## See also<a name="aws-resource-apigateway-resource--seealso"></a>
+ [resource:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/resource-create/) in the *Amazon API Gateway REST API Reference*

