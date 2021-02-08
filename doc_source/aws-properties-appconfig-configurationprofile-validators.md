# AWS::AppConfig::ConfigurationProfile Validators<a name="aws-properties-appconfig-configurationprofile-validators"></a>

A validator provides a syntactic or semantic check to ensure the configuration you want to deploy functions as intended\. To validate your application configuration data, you provide a schema or a Lambda function that runs against the configuration\. The configuration deployment or update can only proceed when the configuration data is valid\.

## Syntax<a name="aws-properties-appconfig-configurationprofile-validators-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appconfig-configurationprofile-validators-syntax.json"></a>

```
{
  "[Content](#cfn-appconfig-configurationprofile-validators-content)" : String,
  "[Type](#cfn-appconfig-configurationprofile-validators-type)" : String
}
```

### YAML<a name="aws-properties-appconfig-configurationprofile-validators-syntax.yaml"></a>

```
  [Content](#cfn-appconfig-configurationprofile-validators-content): String
  [Type](#cfn-appconfig-configurationprofile-validators-type): String
```

## Properties<a name="aws-properties-appconfig-configurationprofile-validators-properties"></a>

`Content`  <a name="cfn-appconfig-configurationprofile-validators-content"></a>
Either the JSON Schema content or the Amazon Resource Name \(ARN\) of an AWS Lambda function\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `32768`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-appconfig-configurationprofile-validators-type"></a>
AWS AppConfig supports validators of type `JSON_SCHEMA` and `LAMBDA`   
*Required*: No  
*Type*: String  
*Allowed values*: `JSON_SCHEMA | LAMBDA`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)