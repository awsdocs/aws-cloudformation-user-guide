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
      "[AuthParameters](#cfn-events-connection-authparameters)" : AuthParameters,
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
  [AuthParameters](#cfn-events-connection-authparameters): 
    AuthParameters
  [Description](#cfn-events-connection-description): String
  [Name](#cfn-events-connection-name): String
```

## Properties<a name="aws-resource-events-connection-properties"></a>

`AuthorizationType`  <a name="cfn-events-connection-authorizationtype"></a>
The type of authorization to use for the connection\.  
OAUTH tokens are refreshed when a 401 or 407 response is returned\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `API_KEY | BASIC | OAUTH_CLIENT_CREDENTIALS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthParameters`  <a name="cfn-events-connection-authparameters"></a>
A `CreateConnectionAuthRequestParameters` object that contains the authorization parameters to use to authorize with the endpoint\.   
*Required*: Yes  
*Type*: [AuthParameters](aws-properties-events-connection-authparameters.md)  
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

## Examples<a name="aws-resource-events-connection--examples"></a>



### Create a connection with ApiKey authorization parameters<a name="aws-resource-events-connection--examples--Create_a_connection_with_ApiKey_authorization_parameters"></a>

The following example creates a connection named pagerduty\-connection using ApiKey authorization and stores a secret from Secrets Manager\.

#### JSON<a name="aws-resource-events-connection--examples--Create_a_connection_with_ApiKey_authorization_parameters--json"></a>

```
{
  "PagerDutyConection": 
    "Type" : "AWS::Events::Connection",
    "Properties" : {
        "Name" : "pagerduty-connection",
        "AuthorizationType" : "API_KEY",
        "AuthParameters" : {
            "ApiKeyAuthParameters" : {
                "ApiKeyName" : "Authorization",
                "ApiKeyValue" : "{{resolve:secretsmanager:arn:aws:secretsmanager:us-west-2:123456789012:secret:pagerdutyApiToken-S9SoDa}}"},
            "AdditionalParameters" : {
                "BodyParameters" : {
                    "routing_key" : "my-pagerduty-integration-key", 
                }, 
            }, 
        },
    }
}
```

#### YAML<a name="aws-resource-events-connection--examples--Create_a_connection_with_ApiKey_authorization_parameters--yaml"></a>

```
PagerDutyConection:
  Type: AWS::Events::Connection
  Properties:
    Name: 'pagerduty-connection'
    AuthorizationType: API_KEY
    AuthParameters:
      ApiKeyAuthParameters:
        ApiKeyName: Authorization
        ApiKeyValue: '{{resolve:secretsmanager:arn:aws:secretsmanager:us-west-2:123456789012:secret:pagerdutyApiToken-S9SoDa}}'
      AdditionalParameters:
        BodyParameters:
        routing_key: 'my-pagerduty-integration-key'
```

### Create a connection with OAuth authorization parameters<a name="aws-resource-events-connection--examples--Create_a_connection_with_OAuth_authorization_parameters"></a>

The following example creates a connection named auth0\-connection using OAuth authorization and stores a secret from Secrets Manager\.

#### JSON<a name="aws-resource-events-connection--examples--Create_a_connection_with_OAuth_authorization_parameters--json"></a>

```
{
  "Auth0Connection":
    "Type" : "AWS::Events::Connection",
    "Properties": {
        "Name" : "auth0-connection",
        "AuthorizationType" : "OAUTH_CLIENT_CREDENTIALS",
        "AuthParameters" : {
            "OAuthParameters": {
                "ClientParameters" : {
                    "ClientId": "{{resolve:secretsmanager:arn:aws:secretsmanager:us-west-2:123456789012:secret:auth0ClientId}}",
                    "ClientSecret": "{{resolve:secretsmanager:arn:aws:secretsmanager:us-west-2:123456789012:secret:auth0ClientSecret}}",
                },
                "AuthorizationEndpoint" : "https://yourUserName.us.auth0.com/oauth/token",
                "HttpMethod" : "POST",
                "AdditionalParameters" : {
                    "BodyParameters: {
                        "audience" : "my-auth0-identifier",
                    },
                },    
            },
        },
    }
}
```

#### YAML<a name="aws-resource-events-connection--examples--Create_a_connection_with_OAuth_authorization_parameters--yaml"></a>

```
Auth0Connection:
  Type: AWS::Events::Connection
  Properties:
    Name: 'auth0-connection'
    AuthorizationType: OAUTH_CLIENT_CREDENTIALS
    AuthParameters:
      OAuthParameters:
        ClientParameters:
          ClientId: '{{resolve:secretsmanager:arn:aws:secretsmanager:us-west-2:123456789012:secret:auth0ClientId}}'
          ClientSecret: '{{resolve:secretsmanager:arn:aws:secretsmanager:us-west-2:123456789012:secret:auth0ClientSecret}}'
        AuthorizationEndpoint: 'https://yourUserName.us.auth0.com/oauth/token'
        HttpMethod: POST
        AdditionalParameters:
          BodyParameters:
            audience: 'my-auth0-identifier'
        #Note: This AdditionalParameters field is a child of OAuthParameters entry, meaning it's only sent with the token exchange
```