# AWS::Events::Connection<a name="aws-resource-events-connection"></a>

Creates a connection\. A connection defines the authorization type and credentials to use for authorization with an API destination HTTP endpoint\.

## Syntax<a name="aws-resource-events-connection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-events-connection-syntax.json"></a>

```
{
  "Type" : "AWS::Events::Connection",
  "Properties" : {
      "[AuthorizationType](#cfn-events-connection-authorizationtype)" : String,
      "[AuthParameters](#cfn-events-connection-authparameters)" : Json,
      "[Description](#cfn-events-connection-description)" : String,
      "[Name](#cfn-events-connection-name)" : String
    }
}
```

### YAML<a name="aws-resource-events-connection-syntax.yaml"></a>

```
Type: AWS::Events::Connection
Properties: 
  [AuthorizationType](#cfn-events-connection-authorizationtype): String
  [AuthParameters](#cfn-events-connection-authparameters): Json
  [Description](#cfn-events-connection-description): String
  [Name](#cfn-events-connection-name): String
```

## Properties<a name="aws-resource-events-connection-properties"></a>

`AuthorizationType`  <a name="cfn-events-connection-authorizationtype"></a>
The type of authorization to use for the connection\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `API_KEY | BASIC | OAUTH_CLIENT_CREDENTIALS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthParameters`  <a name="cfn-events-connection-authparameters"></a>
A `CreateConnectionAuthRequestParameters` object that contains the authorization parameters to use to authorize with the endpoint\.   
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-events-connection-description"></a>
A description for the connection to create\.  
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-events-connection-name"></a>
The name for the connection to create\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[\.\-_A-Za-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-events-connection-return-values"></a>

### Ref<a name="aws-resource-events-connection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the connection that was created by the request\.

### Fn::GetAtt<a name="aws-resource-events-connection-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-events-connection-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the connection that was created by the request\.

`SecretArn`  <a name="SecretArn-fn::getatt"></a>
The ARN for the secret created for the connection\.