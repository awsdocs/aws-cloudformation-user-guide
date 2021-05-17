# AWS::Events::ApiDestination<a name="aws-resource-events-apidestination"></a>

Creates an API destination, which is an HTTP invocation endpoint configured as a target for events\. 

## Syntax<a name="aws-resource-events-apidestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-events-apidestination-syntax.json"></a>

```
{
  "Type" : "AWS::Events::ApiDestination",
  "Properties" : {
      "[ConnectionArn](#cfn-events-apidestination-connectionarn)" : String,
      "[Description](#cfn-events-apidestination-description)" : String,
      "[HttpMethod](#cfn-events-apidestination-httpmethod)" : String,
      "[InvocationEndpoint](#cfn-events-apidestination-invocationendpoint)" : String,
      "[InvocationRateLimitPerSecond](#cfn-events-apidestination-invocationratelimitpersecond)" : Integer,
      "[Name](#cfn-events-apidestination-name)" : String
    }
}
```

### YAML<a name="aws-resource-events-apidestination-syntax.yaml"></a>

```
Type: AWS::Events::ApiDestination
Properties: 
  [ConnectionArn](#cfn-events-apidestination-connectionarn): String
  [Description](#cfn-events-apidestination-description): String
  [HttpMethod](#cfn-events-apidestination-httpmethod): String
  [InvocationEndpoint](#cfn-events-apidestination-invocationendpoint): String
  [InvocationRateLimitPerSecond](#cfn-events-apidestination-invocationratelimitpersecond): Integer
  [Name](#cfn-events-apidestination-name): String
```

## Properties<a name="aws-resource-events-apidestination-properties"></a>

`ConnectionArn`  <a name="cfn-events-apidestination-connectionarn"></a>
The ARN of the connection to use for the API destination\. The destination endpoint must support the authorization type specified for the connection\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-events-apidestination-description"></a>
A description for the API destination to create\. Maximum length of 512 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HttpMethod`  <a name="cfn-events-apidestination-httpmethod"></a>
The method to use for the request to the HTTP invocation endpoint\. One of `POST` \| `GET` \| `HEAD` \| `OPTIONS` \| `PUT` \| `PATCH` \| `DELETE`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InvocationEndpoint`  <a name="cfn-events-apidestination-invocationendpoint"></a>
The URL to the HTTP invocation endpoint for the API destination\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InvocationRateLimitPerSecond`  <a name="cfn-events-apidestination-invocationratelimitpersecond"></a>
The maximum number of requests per second to send to the HTTP invocation endpoint\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-events-apidestination-name"></a>
The name for the API destination to create\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-events-apidestination-return-values"></a>

### Ref<a name="aws-resource-events-apidestination-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the API destination that was created by the request\.

### Fn::GetAtt<a name="aws-resource-events-apidestination-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-events-apidestination-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the API destination that was created by the request\.