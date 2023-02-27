# AWS::ApiGateway::Method Integration<a name="aws-properties-apitgateway-method-integration"></a>

`Integration` is a property of the [AWS::ApiGateway::Method](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-method.html) resource that specifies information about the target backend that a method calls\.

## Syntax<a name="aws-properties-apitgateway-method-integration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apitgateway-method-integration-syntax.json"></a>

```
{
  "[CacheKeyParameters](#cfn-apigateway-method-integration-cachekeyparameters)" : [ String, ... ],
  "[CacheNamespace](#cfn-apigateway-method-integration-cachenamespace)" : String,
  "[ConnectionId](#cfn-apigateway-method-integration-connectionid)" : String,
  "[ConnectionType](#cfn-apigateway-method-integration-connectiontype)" : String,
  "[ContentHandling](#cfn-apigateway-method-integration-contenthandling)" : String,
  "[Credentials](#cfn-apigateway-method-integration-credentials)" : String,
  "[IntegrationHttpMethod](#cfn-apigateway-method-integration-integrationhttpmethod)" : String,
  "[IntegrationResponses](#cfn-apigateway-method-integration-integrationresponses)" : [ IntegrationResponse, ... ],
  "[PassthroughBehavior](#cfn-apigateway-method-integration-passthroughbehavior)" : String,
  "[RequestParameters](#cfn-apigateway-method-integration-requestparameters)" : {Key : Value, ...},
  "[RequestTemplates](#cfn-apigateway-method-integration-requesttemplates)" : {Key : Value, ...},
  "[TimeoutInMillis](#cfn-apigateway-method-integration-timeoutinmillis)" : Integer,
  "[Type](#cfn-apigateway-method-integration-type)" : String,
  "[Uri](#cfn-apigateway-method-integration-uri)" : String
}
```

### YAML<a name="aws-properties-apitgateway-method-integration-syntax.yaml"></a>

```
  [CacheKeyParameters](#cfn-apigateway-method-integration-cachekeyparameters): 
    - String
  [CacheNamespace](#cfn-apigateway-method-integration-cachenamespace): String
  [ConnectionId](#cfn-apigateway-method-integration-connectionid): String
  [ConnectionType](#cfn-apigateway-method-integration-connectiontype): String
  [ContentHandling](#cfn-apigateway-method-integration-contenthandling): String
  [Credentials](#cfn-apigateway-method-integration-credentials): String
  [IntegrationHttpMethod](#cfn-apigateway-method-integration-integrationhttpmethod): String
  [IntegrationResponses](#cfn-apigateway-method-integration-integrationresponses): 
    - IntegrationResponse
  [PassthroughBehavior](#cfn-apigateway-method-integration-passthroughbehavior): String
  [RequestParameters](#cfn-apigateway-method-integration-requestparameters): 
    Key : Value
  [RequestTemplates](#cfn-apigateway-method-integration-requesttemplates): 
    Key : Value
  [TimeoutInMillis](#cfn-apigateway-method-integration-timeoutinmillis): Integer
  [Type](#cfn-apigateway-method-integration-type): String
  [Uri](#cfn-apigateway-method-integration-uri): String
```

## Properties<a name="aws-properties-apitgateway-method-integration-properties"></a>

`CacheKeyParameters`  <a name="cfn-apigateway-method-integration-cachekeyparameters"></a>
A list of request parameters whose values API Gateway caches\. To be valid values for `cacheKeyParameters`, these parameters must also be specified for Method `requestParameters`\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CacheNamespace`  <a name="cfn-apigateway-method-integration-cachenamespace"></a>
Specifies a group of related cached parameters\. By default, API Gateway uses the resource ID as the `cacheNamespace`\. You can specify the same `cacheNamespace` across resources to return the same cached data for requests to different resources\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionId`  <a name="cfn-apigateway-method-integration-connectionid"></a>
The ID of the VpcLink used for the integration when `connectionType=VPC_LINK` and undefined, otherwise\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionType`  <a name="cfn-apigateway-method-integration-connectiontype"></a>
The type of the network connection to the integration endpoint\. The valid value is `INTERNET` for connections through the public routable internet or `VPC_LINK` for private connections between API Gateway and a network load balancer in a VPC\. The default value is `INTERNET`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `INTERNET | VPC_LINK`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentHandling`  <a name="cfn-apigateway-method-integration-contenthandling"></a>
Specifies how to handle request payload content type conversions\. Supported values are `CONVERT_TO_BINARY` and `CONVERT_TO_TEXT`, with the following behaviors:  
If this property is not defined, the request payload will be passed through from the method request to integration request without modification, provided that the `passthroughBehavior` is configured to support payload pass\-through\.  
*Required*: No  
*Type*: String  
*Allowed values*: `CONVERT_TO_BINARY | CONVERT_TO_TEXT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Credentials`  <a name="cfn-apigateway-method-integration-credentials"></a>
Specifies the credentials required for the integration, if any\. For AWS integrations, three options are available\. To specify an IAM Role for API Gateway to assume, use the role's Amazon Resource Name \(ARN\)\. To require that the caller's identity be passed through from the request, specify the string `arn:aws:iam::\*:user/\*`\. To use resource\-based permissions on supported AWS services, specify null\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegrationHttpMethod`  <a name="cfn-apigateway-method-integration-integrationhttpmethod"></a>
Specifies the integration's HTTP method type\. For the Type property, if you specify `MOCK`, this property is optional\. For Lambda integrations, you must set the integration method to `POST`\. For all other types, you must specify this property\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IntegrationResponses`  <a name="cfn-apigateway-method-integration-integrationresponses"></a>
Specifies the integration's responses\.  
*Required*: No  
*Type*: List of [IntegrationResponse](aws-properties-apitgateway-method-integration-integrationresponse.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PassthroughBehavior`  <a name="cfn-apigateway-method-integration-passthroughbehavior"></a>
Specifies how the method request body of an unmapped content type will be passed through the integration request to the back end without transformation\. A content type is unmapped if no mapping template is defined in the integration or the content type does not match any of the mapped content types, as specified in `requestTemplates`\. The valid value is one of the following: `WHEN_NO_MATCH`: passes the method request body through the integration request to the back end without transformation when the method request content type does not match any content type associated with the mapping templates defined in the integration request\. `WHEN_NO_TEMPLATES`: passes the method request body through the integration request to the back end without transformation when no mapping template is defined in the integration request\. If a template is defined when this option is selected, the method request of an unmapped content\-type will be rejected with an HTTP 415 Unsupported Media Type response\. `NEVER`: rejects the method request with an HTTP 415 Unsupported Media Type response when either the method request content type does not match any content type associated with the mapping templates defined in the integration request or no mapping template is defined in the integration request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestParameters`  <a name="cfn-apigateway-method-integration-requestparameters"></a>
A key\-value map specifying request parameters that are passed from the method request to the back end\. The key is an integration request parameter name and the associated value is a method request parameter value or static value that must be enclosed within single quotes and pre\-encoded as required by the back end\. The method request parameter value must match the pattern of `method.request.{location}.{name}`, where `location` is `querystring`, `path`, or `header` and `name` must be a valid and unique method request parameter name\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestTemplates`  <a name="cfn-apigateway-method-integration-requesttemplates"></a>
Represents a map of Velocity templates that are applied on the request payload based on the value of the Content\-Type header sent by the client\. The content type value is the key in this map, and the template \(as a String\) is the value\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeoutInMillis`  <a name="cfn-apigateway-method-integration-timeoutinmillis"></a>
Custom timeout between 50 and 29,000 milliseconds\. The default value is 29,000 milliseconds or 29 seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-apigateway-method-integration-type"></a>
Specifies an API method integration type\. The valid value is one of the following:  
For the HTTP and HTTP proxy integrations, each integration can specify a protocol \(`http/https`\), port and path\. Standard 80 and 443 ports are supported as well as custom ports above 1024\. An HTTP or HTTP proxy integration with a `connectionType` of `VPC_LINK` is referred to as a private integration and uses a VpcLink to connect API Gateway to a network load balancer of a VPC\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AWS | AWS_PROXY | HTTP | HTTP_PROXY | MOCK`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Uri`  <a name="cfn-apigateway-method-integration-uri"></a>
Specifies Uniform Resource Identifier \(URI\) of the integration endpoint\.  
For `HTTP` or `HTTP_PROXY` integrations, the URI must be a fully formed, encoded HTTP\(S\) URL according to the RFC\-3986 specification for standard integrations\. If `connectionType` is `VPC_LINK` specify the Network Load Balancer DNS name\. For `AWS` or `AWS_PROXY` integrations, the URI is of the form `arn:aws:apigateway:{region}:{subdomain.service|service}:path|action/{service_api}`\. Here, \{Region\} is the API Gateway region \(e\.g\., us\-east\-1\); \{service\} is the name of the integrated AWS service \(e\.g\., s3\); and \{subdomain\} is a designated subdomain supported by certain AWS service for fast host\-name lookup\. action can be used for an AWS service action\-based API, using an Action=\{name\}&\{p1\}=\{v1\}&p2=\{v2\}\.\.\. query string\. The ensuing \{service\_api\} refers to a supported action \{name\} plus any required input parameters\. Alternatively, path can be used for an AWS service path\-based API\. The ensuing service\_api refers to the path to an AWS service resource, including the region of the integrated AWS service, if applicable\. For example, for integration with the S3 API of GetObject, the uri can be either `arn:aws:apigateway:us-west-2:s3:action/GetObject&Bucket={bucket}&Key={key}` or `arn:aws:apigateway:us-west-2:s3:path/{bucket}/{key}`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-apitgateway-method-integration--seealso"></a>
+ [Method](https://docs.aws.amazon.com/apigateway/latest/api/API_Method.html) in the *Amazon API Gateway REST API Reference*

