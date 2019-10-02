# AWS::AppSync::DataSource HttpConfig<a name="aws-properties-appsync-datasource-httpconfig"></a>

Use the `HttpConfig` property type to specify `HttpConfig` for an AWS AppSync data source\.

 `HttpConfig` is a property of the [AWS::AppSync::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-datasource.html) resource\. 

## Syntax<a name="aws-properties-appsync-datasource-httpconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-httpconfig-syntax.json"></a>

```
{
  "[AuthorizationConfig](#cfn-appsync-datasource-httpconfig-authorizationconfig)" : [AuthorizationConfig](aws-properties-appsync-datasource-authorizationconfig.md),
  "[Endpoint](#cfn-appsync-datasource-httpconfig-endpoint)" : String
}
```

### YAML<a name="aws-properties-appsync-datasource-httpconfig-syntax.yaml"></a>

```
  [AuthorizationConfig](#cfn-appsync-datasource-httpconfig-authorizationconfig): 
    [AuthorizationConfig](aws-properties-appsync-datasource-authorizationconfig.md)
  [Endpoint](#cfn-appsync-datasource-httpconfig-endpoint): String
```

## Properties<a name="aws-properties-appsync-datasource-httpconfig-properties"></a>

`AuthorizationConfig`  <a name="cfn-appsync-datasource-httpconfig-authorizationconfig"></a>
The authorization configuration\.  
*Required*: No  
*Type*: [AuthorizationConfig](aws-properties-appsync-datasource-authorizationconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Endpoint`  <a name="cfn-appsync-datasource-httpconfig-endpoint"></a>
The endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `us-east-1`
- `us-east-2`
- `us-west-2`
