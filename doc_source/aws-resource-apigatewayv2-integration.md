# AWS::ApiGatewayV2::Integration<a name="aws-resource-apigatewayv2-integration"></a>

The `AWS::ApiGatewayV2::Integration` resource creates an integration for an API\.

## Syntax<a name="aws-resource-apigatewayv2-integration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigatewayv2-integration-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGatewayV2::Integration",
  "Properties" : {
      "[ApiId](#cfn-apigatewayv2-integration-apiid)" : String,
      "[ConnectionId](#cfn-apigatewayv2-integration-connectionid)" : String,
      "[ConnectionType](#cfn-apigatewayv2-integration-connectiontype)" : String,
      "[ContentHandlingStrategy](#cfn-apigatewayv2-integration-contenthandlingstrategy)" : String,
      "[CredentialsArn](#cfn-apigatewayv2-integration-credentialsarn)" : String,
      "[Description](#cfn-apigatewayv2-integration-description)" : String,
      "[IntegrationMethod](#cfn-apigatewayv2-integration-integrationmethod)" : String,
      "[IntegrationSubtype](#cfn-apigatewayv2-integration-integrationsubtype)" : String,
      "[IntegrationType](#cfn-apigatewayv2-integration-integrationtype)" : String,
      "[IntegrationUri](#cfn-apigatewayv2-integration-integrationuri)" : String,
      "[PassthroughBehavior](#cfn-apigatewayv2-integration-passthroughbehavior)" : String,
      "[PayloadFormatVersion](#cfn-apigatewayv2-integration-payloadformatversion)" : String,
      "[RequestParameters](#cfn-apigatewayv2-integration-requestparameters)" : Json,
      "[RequestTemplates](#cfn-apigatewayv2-integration-requesttemplates)" : Json,
      "[TemplateSelectionExpression](#cfn-apigatewayv2-integration-templateselectionexpression)" : String,
      "[TimeoutInMillis](#cfn-apigatewayv2-integration-timeoutinmillis)" : Integer,
      "[TlsConfig](#cfn-apigatewayv2-integration-tlsconfig)" : TlsConfig
    }
}
```

### YAML<a name="aws-resource-apigatewayv2-integration-syntax.yaml"></a>

```
Type: AWS::ApiGatewayV2::Integration
Properties: 
  [ApiId](#cfn-apigatewayv2-integration-apiid): String
  [ConnectionId](#cfn-apigatewayv2-integration-connectionid): String
  [ConnectionType](#cfn-apigatewayv2-integration-connectiontype): String
  [ContentHandlingStrategy](#cfn-apigatewayv2-integration-contenthandlingstrategy): String
  [CredentialsArn](#cfn-apigatewayv2-integration-credentialsarn): String
  [Description](#cfn-apigatewayv2-integration-description): String
  [IntegrationMethod](#cfn-apigatewayv2-integration-integrationmethod): String
  [IntegrationSubtype](#cfn-apigatewayv2-integration-integrationsubtype): String
  [IntegrationType](#cfn-apigatewayv2-integration-integrationtype): String
  [IntegrationUri](#cfn-apigatewayv2-integration-integrationuri): String
  [PassthroughBehavior](#cfn-apigatewayv2-integration-passthroughbehavior): String
  [PayloadFormatVersion](#cfn-apigatewayv2-integration-payloadformatversion): String
  [RequestParameters](#cfn-apigatewayv2-integration-requestparameters): Json
  [RequestTemplates](#cfn-apigatewayv2-integration-requesttemplates): Json
  [TemplateSelectionExpression](#cfn-apigatewayv2-integration-templateselectionexpression): String
  [TimeoutInMillis](#cfn-apigatewayv2-integration-timeoutinmillis): Integer
  [TlsConfig](#cfn-apigatewayv2-integration-tlsconfig): 
    TlsConfig
```

## Properties<a name="aws-resource-apigatewayv2-integration-properties"></a>

`ApiId`  <a name="cfn-apigatewayv2-integration-apiid"></a>
The API identifier\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConnectionId`  <a name="cfn-apigatewayv2-integration-connectionid"></a>
The ID of the VPC link for a private integration\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionType`  <a name="cfn-apigatewayv2-integration-connectiontype"></a>
The type of the network connection to the integration endpoint\. Specify `INTERNET` for connections through the public routable internet or `VPC_LINK` for private connections between API Gateway and resources in a VPC\. The default value is `INTERNET`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentHandlingStrategy`  <a name="cfn-apigatewayv2-integration-contenthandlingstrategy"></a>
Supported only for WebSocket APIs\. Specifies how to handle response payload content type conversions\. Supported values are `CONVERT_TO_BINARY` and `CONVERT_TO_TEXT`, with the following behaviors:  
 `CONVERT_TO_BINARY`: Converts a response payload from a Base64\-encoded string to the corresponding binary blob\.  
 `CONVERT_TO_TEXT`: Converts a response payload from a binary blob to a Base64\-encoded string\.  
If this property is not defined, the response payload will be passed through from the integration response to the route response or method response without modification\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CredentialsArn`  <a name="cfn-apigatewayv2-integration-credentialsarn"></a>
Specifies the credentials required for the integration, if any\. For AWS integrations, three options are available\. To specify an IAM Role for API Gateway to assume, use the role's Amazon Resource Name \(ARN\)\. To require that the caller's identity be passed through from the request, specify the string `arn:aws:iam::*:user/*`\. To use resource\-based permissions on supported AWS services, don't specify this parameter\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-apigatewayv2-integration-description"></a>
The description of the integration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegrationMethod`  <a name="cfn-apigatewayv2-integration-integrationmethod"></a>
Specifies the integration's HTTP method type\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegrationSubtype`  <a name="cfn-apigatewayv2-integration-integrationsubtype"></a>
Supported only for HTTP API `AWS_PROXY` integrations\. Specifies the AWS service action to invoke\. To learn more, see [Integration subtype reference](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-integrations-aws-services-reference.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegrationType`  <a name="cfn-apigatewayv2-integration-integrationtype"></a>
The integration type of an integration\. One of the following:  
 `AWS`: for integrating the route or method request with an AWS service action, including the Lambda function\-invoking action\. With the Lambda function\-invoking action, this is referred to as the Lambda custom integration\. With any other AWS service action, this is known as AWS integration\. Supported only for WebSocket APIs\.  
 `AWS_PROXY`: for integrating the route or method request with a Lambda function or other AWS service action\. This integration is also referred to as a Lambda proxy integration\.  
 `HTTP`: for integrating the route or method request with an HTTP endpoint\. This integration is also referred to as the HTTP custom integration\. Supported only for WebSocket APIs\.  
 `HTTP_PROXY`: for integrating the route or method request with an HTTP endpoint, with the client request passed through as\-is\. This is also referred to as HTTP proxy integration\. For HTTP API private integrations, use an `HTTP_PROXY` integration\.  
 `MOCK`: for integrating the route or method request with API Gateway as a "loopback" endpoint without invoking any backend\. Supported only for WebSocket APIs\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegrationUri`  <a name="cfn-apigatewayv2-integration-integrationuri"></a>
For a Lambda integration, specify the URI of a Lambda function\.  
For an HTTP integration, specify a fully\-qualified URL\.  
For an HTTP API private integration, specify the ARN of an Application Load Balancer listener, Network Load Balancer listener, or AWS Cloud Map service\. If you specify the ARN of an AWS Cloud Map service, API Gateway uses `DiscoverInstances` to identify resources\. You can use query parameters to target specific resources\. To learn more, see [DiscoverInstances](https://docs.aws.amazon.com/cloud-map/latest/api/API_DiscoverInstances.html)\. For private integrations, all resources must be owned by the same AWS account\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PassthroughBehavior`  <a name="cfn-apigatewayv2-integration-passthroughbehavior"></a>
Specifies the pass\-through behavior for incoming requests based on the `Content-Type` header in the request, and the available mapping templates specified as the `requestTemplates` property on the `Integration` resource\. There are three valid values: `WHEN_NO_MATCH`, `WHEN_NO_TEMPLATES`, and `NEVER`\. Supported only for WebSocket APIs\.  
 `WHEN_NO_MATCH` passes the request body for unmapped content types through to the integration backend without transformation\.  
 `NEVER` rejects unmapped content types with an `HTTP 415 Unsupported Media Type` response\.  
 `WHEN_NO_TEMPLATES` allows pass\-through when the integration has no content types mapped to templates\. However, if there is at least one content type defined, unmapped content types will be rejected with the same `HTTP 415 Unsupported Media Type` response\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PayloadFormatVersion`  <a name="cfn-apigatewayv2-integration-payloadformatversion"></a>
Specifies the format of the payload sent to an integration\. Required for HTTP APIs\. For HTTP APIs, supported values for Lambda proxy integrations are `1.0` and `2.0`\. For all other integrations, `1.0` is the only supported value\. To learn more, see [Working with AWS Lambda proxy integrations for HTTP APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-integrations-lambda.html)\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestParameters`  <a name="cfn-apigatewayv2-integration-requestparameters"></a>
For WebSocket APIs, a key\-value map specifying request parameters that are passed from the method request to the backend\. The key is an integration request parameter name and the associated value is a method request parameter value or static value that must be enclosed within single quotes and pre\-encoded as required by the backend\. The method request parameter value must match the pattern of `method.request.{location}.{name} `, where ` {location} ` is `querystring`, `path`, or `header`; and `{name}` must be a valid and unique method request parameter name\.  
For HTTP APIs, request parameters are a key\-value map specifying parameters that are passed to `AWS_PROXY` integrations with a specified `integrationSubtype`\. You can provide static values, or map request data, stage variables, or context variables that are evaluated at runtime\. To learn more, see [Working with AWS service integrations for HTTP APIs](https://docs.aws.amazon.com/apigateway/latest/developerguide/http-api-develop-integrations-aws-services.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestTemplates`  <a name="cfn-apigatewayv2-integration-requesttemplates"></a>
Represents a map of Velocity templates that are applied on the request payload based on the value of the Content\-Type header sent by the client\. The content type value is the key in this map, and the template \(as a String\) is the value\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateSelectionExpression`  <a name="cfn-apigatewayv2-integration-templateselectionexpression"></a>
The template selection expression for the integration\. Supported only for WebSocket APIs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutInMillis`  <a name="cfn-apigatewayv2-integration-timeoutinmillis"></a>
Custom timeout between 50 and 29,000 milliseconds for WebSocket APIs and between 50 and 30,000 milliseconds for HTTP APIs\. The default timeout is 29 seconds for WebSocket APIs and 30 seconds for HTTP APIs\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TlsConfig`  <a name="cfn-apigatewayv2-integration-tlsconfig"></a>
The TLS configuration for a private integration\. If you specify a TLS configuration, private integration traffic uses the HTTPS protocol\. Supported only for HTTP APIs\.  
*Required*: No  
*Type*: [TlsConfig](aws-properties-apigatewayv2-integration-tlsconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-apigatewayv2-integration-return-values"></a>

### Ref<a name="aws-resource-apigatewayv2-integration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Integration resource ID, such as `abcd123`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-apigatewayv2-integration--examples"></a>



### Integration creation example<a name="aws-resource-apigatewayv2-integration--examples--Integration_creation_example"></a>

The following example creates an `integration` resource named `MyIntegration` for the `MyApi` API, whose credentials are specified by `MyCredentialsArn`\.

#### JSON<a name="aws-resource-apigatewayv2-integration--examples--Integration_creation_example--json"></a>

```
{
    "MyIntegration": {
        "Type": "AWS::ApiGatewayV2::Integration",
        "Properties": {
            "ApiId": {
                "Ref": "MyApi"
            },
            "Description": "Lambda Integration",
            "IntegrationType": "AWS",
            "IntegrationUri": {
                "Fn::Join": [
                    "",
                    [
                        "arn:",
                        {
                            "Ref": "AWS::Partition"
                        },
                        ":apigateway:",
                        {
                            "Ref": "AWS::Region"
                        },
                        ":lambda:path/2015-03-31/functions/",
                        {
                            "Ref": "MyLambdaFunction"
                        },
                        "/invocations"
                    ]
                ]
            },
            "CredentialsArn": "MyCredentialsArn",
            "IntegrationMethod": "GET",
            "ConnectionType": "INTERNET"
        }
    }
}
```

#### YAML<a name="aws-resource-apigatewayv2-integration--examples--Integration_creation_example--yaml"></a>

```
MyIntegration:
  Type: 'AWS::ApiGatewayV2::Integration'
  Properties:
    ApiId: !Ref MyApi
    Description: Lambda Integration
    IntegrationType: AWS
    IntegrationUri: !Join 
      - ''
      - - 'arn:'
        - !Ref 'AWS::Partition'
        - ':apigateway:'
        - !Ref 'AWS::Region'
        - ':lambda:path/2015-03-31/functions/'
        - !Ref MyLambdaFunction
        - /invocations
    CredentialsArn: MyCredentialsArn
    IntegrationMethod: GET
    ConnectionType: INTERNET
```

## See also<a name="aws-resource-apigatewayv2-integration--seealso"></a>
+ [CreateIntegration](https://docs.aws.amazon.com/apigatewayv2/latest/api-reference/apis-apiid-integrations.html#CreateIntegration) in the *Amazon API Gateway Version 2 API Reference*

