# AWS::AppSync::DataSource AwsIamConfig<a name="aws-properties-appsync-datasource-awsiamconfig"></a>

Use the `AwsIamConfig` property type to specify AwsIamConfig for a AWS AppSync authorizaton\.

 `AwsIamConfig` is a property of the [AWS AppSync DataSource AuthorizationConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-appsync-datasource-httpconfig-authorizationconfig.html) resource\. 

## Syntax<a name="aws-properties-appsync-datasource-awsiamconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appsync-datasource-awsiamconfig-syntax.json"></a>

```
{
  "[SigningRegion](#cfn-appsync-datasource-awsiamconfig-signingregion)" : String,
  "[SigningServiceName](#cfn-appsync-datasource-awsiamconfig-signingservicename)" : String
}
```

### YAML<a name="aws-properties-appsync-datasource-awsiamconfig-syntax.yaml"></a>

```
  [SigningRegion](#cfn-appsync-datasource-awsiamconfig-signingregion): String
  [SigningServiceName](#cfn-appsync-datasource-awsiamconfig-signingservicename): String
```

## Properties<a name="aws-properties-appsync-datasource-awsiamconfig-properties"></a>

`SigningRegion`  <a name="cfn-appsync-datasource-awsiamconfig-signingregion"></a>
The signing region for AWS IAM authorization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SigningServiceName`  <a name="cfn-appsync-datasource-awsiamconfig-signingservicename"></a>
The signing service name for AWS IAM authorization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)