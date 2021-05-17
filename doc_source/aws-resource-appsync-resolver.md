# AWS::AppSync::Resolver<a name="aws-resource-appsync-resolver"></a>

The `AWS::AppSync::Resolver` resource defines the logical GraphQL resolver that you attach to fields in a schema\. Request and response templates for resolvers are written in Apache Velocity Template Language \(VTL\) format\. For more information about resolvers, see [Resolver Mapping Template Reference](https://docs.aws.amazon.com/appsync/latest/devguide/resolver-mapping-template-reference.html)\.

**Note**  
When you submit an update, AWS CloudFormation updates resources based on differences between what you submit and the stack's current template\. To cause this resource to be updated you must change a property value for this resource in the CloudFormation template\. Changing the S3 file content without changing a property value will not result in an update operation\.  
See [Update Behaviors of Stack Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html) in the *AWS CloudFormation User Guide*\.

## Syntax<a name="aws-resource-appsync-resolver-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appsync-resolver-syntax.json"></a>

```
{
  "Type" : "AWS::AppSync::Resolver",
  "Properties" : {
      "[ApiId](#cfn-appsync-resolver-apiid)" : String,
      "[CachingConfig](#cfn-appsync-resolver-cachingconfig)" : CachingConfig,
      "[DataSourceName](#cfn-appsync-resolver-datasourcename)" : String,
      "[FieldName](#cfn-appsync-resolver-fieldname)" : String,
      "[Kind](#cfn-appsync-resolver-kind)" : String,
      "[PipelineConfig](#cfn-appsync-resolver-pipelineconfig)" : PipelineConfig,
      "[RequestMappingTemplate](#cfn-appsync-resolver-requestmappingtemplate)" : String,
      "[RequestMappingTemplateS3Location](#cfn-appsync-resolver-requestmappingtemplates3location)" : String,
      "[ResponseMappingTemplate](#cfn-appsync-resolver-responsemappingtemplate)" : String,
      "[ResponseMappingTemplateS3Location](#cfn-appsync-resolver-responsemappingtemplates3location)" : String,
      "[SyncConfig](#cfn-appsync-resolver-syncconfig)" : SyncConfig,
      "[TypeName](#cfn-appsync-resolver-typename)" : String
    }
}
```

### YAML<a name="aws-resource-appsync-resolver-syntax.yaml"></a>

```
Type: AWS::AppSync::Resolver
Properties: 
  [ApiId](#cfn-appsync-resolver-apiid): String
  [CachingConfig](#cfn-appsync-resolver-cachingconfig): 
    CachingConfig
  [DataSourceName](#cfn-appsync-resolver-datasourcename): String
  [FieldName](#cfn-appsync-resolver-fieldname): String
  [Kind](#cfn-appsync-resolver-kind): String
  [PipelineConfig](#cfn-appsync-resolver-pipelineconfig): 
    PipelineConfig
  [RequestMappingTemplate](#cfn-appsync-resolver-requestmappingtemplate): String
  [RequestMappingTemplateS3Location](#cfn-appsync-resolver-requestmappingtemplates3location): String
  [ResponseMappingTemplate](#cfn-appsync-resolver-responsemappingtemplate): String
  [ResponseMappingTemplateS3Location](#cfn-appsync-resolver-responsemappingtemplates3location): String
  [SyncConfig](#cfn-appsync-resolver-syncconfig): 
    SyncConfig
  [TypeName](#cfn-appsync-resolver-typename): String
```

## Properties<a name="aws-resource-appsync-resolver-properties"></a>

`ApiId`  <a name="cfn-appsync-resolver-apiid"></a>
The AWS AppSync GraphQL API to which you want to attach this resolver\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CachingConfig`  <a name="cfn-appsync-resolver-cachingconfig"></a>
The caching configuration for the resolver\.  
*Required*: No  
*Type*: [CachingConfig](aws-properties-appsync-resolver-cachingconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DataSourceName`  <a name="cfn-appsync-resolver-datasourcename"></a>
The resolver data source name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldName`  <a name="cfn-appsync-resolver-fieldname"></a>
The GraphQL field on a type that invokes the resolver\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Kind`  <a name="cfn-appsync-resolver-kind"></a>
The resolver type\.  
+  **UNIT**: A UNIT resolver type\. A UNIT resolver is the default resolver type\. A UNIT resolver enables you to execute a GraphQL query against a single data source\.
+  **PIPELINE**: A PIPELINE resolver type\. A PIPELINE resolver enables you to execute a series of `Function` in a serial manner\. You can use a pipeline resolver to execute a GraphQL query against multiple data sources\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PipelineConfig`  <a name="cfn-appsync-resolver-pipelineconfig"></a>
Functions linked with the pipeline resolver\.  
*Required*: No  
*Type*: [PipelineConfig](aws-properties-appsync-resolver-pipelineconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestMappingTemplate`  <a name="cfn-appsync-resolver-requestmappingtemplate"></a>
The request mapping template\.  
Request mapping templates are optional when using a Lambda data source\. For all other data sources, a request mapping template is required\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequestMappingTemplateS3Location`  <a name="cfn-appsync-resolver-requestmappingtemplates3location"></a>
The location of a request mapping template in an Amazon S3 bucket\. Use this if you want to provision with a template file in Amazon S3 rather than embedding it in your CloudFormation template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseMappingTemplate`  <a name="cfn-appsync-resolver-responsemappingtemplate"></a>
The response mapping template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResponseMappingTemplateS3Location`  <a name="cfn-appsync-resolver-responsemappingtemplates3location"></a>
The location of a response mapping template in an Amazon S3 bucket\. Use this if you want to provision with a template file in Amazon S3 rather than embedding it in your CloudFormation template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SyncConfig`  <a name="cfn-appsync-resolver-syncconfig"></a>
The `SyncConfig` for a resolver attached to a versioned datasource\.  
*Required*: No  
*Type*: [SyncConfig](aws-properties-appsync-resolver-syncconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TypeName`  <a name="cfn-appsync-resolver-typename"></a>
The GraphQL type that invokes this resolver\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appsync-resolver-return-values"></a>

### Ref<a name="aws-resource-appsync-resolver-return-values-ref"></a>

When you pass the logical ID of an `AWS::AppSync::Resolver` resource to the intrinsic `Ref` function, the function returns the ARN of the Resolver, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/types/typename/resolvers/resolvername`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref)\.

### Fn::GetAtt<a name="aws-resource-appsync-resolver-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt)\. 

#### <a name="aws-resource-appsync-resolver-return-values-fn--getatt-fn--getatt"></a>

`FieldName`  <a name="FieldName-fn::getatt"></a>
The GraphQL field on a type that invokes the resolver\. 

`ResolverArn`  <a name="ResolverArn-fn::getatt"></a>
ARN of the resolver, such as `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/types/typename/resolvers/resolvername`\.

`TypeName`  <a name="TypeName-fn::getatt"></a>
The GraphQL type that invokes this resolver\.

## Examples<a name="aws-resource-appsync-resolver--examples"></a>



### Resolver Creation Example<a name="aws-resource-appsync-resolver--examples--Resolver_Creation_Example"></a>

The following example creates a resolver and associates it with an existing GraphQL API and a data source by passing the GraphQL API ID and data source name as a parameter\. 

#### YAML<a name="aws-resource-appsync-resolver--examples--Resolver_Creation_Example--yaml"></a>

```
Parameters:
  graphQlApiId:
    Type: String
  dataSourceName:
    Type: String
  fieldName:
    Type: String
  typeName:
    Type: String
  requestMappingTemplateS3LocationInput:
    Type: String
  responseMappingTemplateS3LocationInput:
    Type: String
Resources:
  Resolver:
    Type: AWS::AppSync::Resolver
    Properties:
      ApiId:
	Ref: graphQlApiId
      TypeName:
        Ref: typeName
      FieldName:
        Ref: fieldName
      DataSourceName:
        Ref: dataSourceName
      RequestMappingTemplateS3Location:
        Ref: requestMappingTemplateS3LocationInput
      ResponseMappingTemplateS3Location:
        Ref: responseMappingTemplateS3LocationInput
```

#### JSON<a name="aws-resource-appsync-resolver--examples--Resolver_Creation_Example--json"></a>

```
{
  "Parameters": {
    "graphQlApiId": {
      "Type": "String"
    },
    "dataSourceName": {
      "Type": "String"
    },
    "fieldName": {
      "Type": "String"
    },
    "typeName": {
      "Type": "String"
    },
    "requestMappingTemplateS3LocationInput": {
      "Type": "String"
    },
    "responseMappingTemplateS3LocationInput": {
      "Type": "String"
    }
  },
  "Resources": {
    "Resolver": {
      "Type": "AWS::AppSync::Resolver",
      "Properties": {
        "ApiId": {
          "Ref": "graphQlApiId"
        },
        "TypeName": {
          "Ref": "typeName"
        },
        "FieldName": {
          "Ref": "fieldName"
        },
        "DataSourceName": {
          "Ref": "dataSourceName"
        },
        "RequestMappingTemplateS3Location": {
          "Ref": "requestMappingTemplateS3LocationInput"
        },
        "ResponseMappingTemplateS3Location": {
          "Ref": "responseMappingTemplateS3LocationInput"
        }
      }
    }
  }
}
```

## See also<a name="aws-resource-appsync-resolver--seealso"></a>
+  [CreateResolver](https://docs.aws.amazon.com/appsync/latest/APIReference/API_CreateResolver.html) operation in the *AWS AppSync API Reference*\.

