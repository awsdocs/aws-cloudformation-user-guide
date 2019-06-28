# AWS::ApiGateway::BasePathMapping<a name="aws-resource-apigateway-basepathmapping"></a>

The `AWS::ApiGateway::BasePathMapping` resource creates a base path that clients who call your API must use in the invocation URL\.

## Syntax<a name="aws-resource-apigateway-basepathmapping-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apigateway-basepathmapping-syntax.json"></a>

```
{
  "Type" : "AWS::ApiGateway::BasePathMapping",
  "Properties" : {
      "[BasePath](#cfn-apigateway-basepathmapping-basepath)" : String,
      "[DomainName](#cfn-apigateway-basepathmapping-domainname)" : String,
      "[RestApiId](#cfn-apigateway-basepathmapping-restapiid)" : String,
      "[Stage](#cfn-apigateway-basepathmapping-stage)" : String
    }
}
```

### YAML<a name="aws-resource-apigateway-basepathmapping-syntax.yaml"></a>

```
Type: AWS::ApiGateway::BasePathMapping
Properties:
  [BasePath](#cfn-apigateway-basepathmapping-basepath): String
  [DomainName](#cfn-apigateway-basepathmapping-domainname): String
  [RestApiId](#cfn-apigateway-basepathmapping-restapiid): String
  [Stage](#cfn-apigateway-basepathmapping-stage): String
```

## Properties<a name="aws-resource-apigateway-basepathmapping-properties"></a>

`BasePath`  <a name="cfn-apigateway-basepathmapping-basepath"></a>
The base path name that callers of the API must provide in the URL after the domain name\. If you specify this property, it can't be an empty string\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DomainName`  <a name="cfn-apigateway-basepathmapping-domainname"></a>
The `DomainName` of an [AWS::ApiGateway::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-domainname.html) resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RestApiId`  <a name="cfn-apigateway-basepathmapping-restapiid"></a>
The name of the API\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Stage`  <a name="cfn-apigateway-basepathmapping-stage"></a>
The name of the API's stage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)


## Examples<a name="aws-resource-apigateway-basepathmapping--examples"></a>

### Base Path Mapping<a name="aws-resource-apigateway-basepathmapping--examples--Create_authorizer"></a>

The following examples create a base path for the domain "mydomain.com". It expects an input parameter for an [ACM Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-certificatemanager-certificate.html) for "mydomain.com" and a Stage name to use for the API deployment.\.

#### JSON<a name="aws-resource-apigateway-authorizer--examples--BasePathMapping--json"></a>

```
{
  "MyAPI": {
    "Type": "AWS::ApiGateway::RestApi",
    "Properties": {
      "Name": "myCoolAPI"
    }
  },
  "MockMethod": {
    "Type": "AWS::ApiGateway::Method",
    "Properties": {
      "HttpMethod": "GET",
      "ResourceId": {
        "Fn::GetAtt": [
            "MyAPI",
          "RootResourceId"
        ]
      },
      "RestApiId": {
        "Ref": "MyAPI"
      },
      "AuthorizationType": "NONE",
      "Integration": {
        "IntegrationResponses": [
          {
            "ResponseTemplates": {
              "application/json": "{\"hello\":\"world\"}"
            },
            "StatusCode": 200
          }
        ],
        "RequestTemplates": {
          "application/json": "{\"statusCode\": 200}"
        },
        "Type": "MOCK"
      }
    }
  },
  "APIDeployment": {
    "Type": "AWS::ApiGateway::Deployment",
    "DependsOn": [
      "MockMethod"
    ],
    "Properties": {
      "Description": {
        "Fn::Sub": "${Stage} for MyAPI"
      },
      "RestApiId": {
        "Ref": "MyAPI"
      },
      "StageName": {
        "Ref": "Stage"
      }
    }
  },
  "APIDomainName": {
    "Type": "AWS::ApiGateway::DomainName",
    "Properties": {
      "CertificateArn": {
        "Ref": "certificateArn"
      },
      "DomainName": "mydomain.com"
    }
  },
  "APIBasePathMapping": {
    "Type": "AWS::ApiGateway::BasePathMapping",
    "Properties": {
      "DomainName": {
        "Ref": "APIDomainName"
      },
      "RestApiId": {
        "Ref": "MyAPI"
      },
      "Stage": {
        "Ref": "Stage"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-apigateway-basepathmapping--examples--BasePathMapping--yaml"></a>

```
MyAPI:
  Type: AWS::ApiGateway::RestApi
  Properties:
    Name: myCoolAPI
MockMethod:
  Type: AWS::ApiGateway::Method
  Properties:
    HttpMethod: GET
    ResourceId: !GetAtt MyAPI.RootResourceId
    RestApiId: !Ref MyAPI
    AuthorizationType: NONE
    Integration:
      IntegrationResponses:
        - ResponseTemplates:
            application/json: "{\"hello\":\"world\"}"
          StatusCode: 200
      RequestTemplates:
        application/json: "{\"statusCode\": 200}"
      Type: MOCK
APIDeployment:
  Type: AWS::ApiGateway::Deployment
  DependsOn:
    - MockMethod
  Properties:
    Description: !Sub "${Stage} for MyAPI"
    RestApiId: !Ref MyAPI
    StageName: !Ref Stage
APIDomainName:
  Type: AWS::ApiGateway::DomainName
  Properties:
    CertificateArn: !Ref certificateArn
    DomainName: "mydomain.com"
APIBasePathMapping:
  Type: AWS::ApiGateway::BasePathMapping
  Properties:
    DomainName: !Ref APIDomainName
    RestApiId: !Ref MyAPI
    Stage: !Ref Stage
```

## See Also<a name="aws-resource-apigateway-basepathmapping--seealso"></a>
+ [basepathmapping:create](https://docs.aws.amazon.com/apigateway/api-reference/link-relation/basepathmapping-create/) in the *Amazon API Gateway REST API Reference*
