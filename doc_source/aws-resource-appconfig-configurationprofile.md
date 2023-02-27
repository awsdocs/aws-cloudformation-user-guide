# AWS::AppConfig::ConfigurationProfile<a name="aws-resource-appconfig-configurationprofile"></a>

The `AWS::AppConfig::ConfigurationProfile` resource creates a configuration profile that enables AWS AppConfig to access the configuration source\. Valid configuration sources include AWS Systems Manager \(SSM\) documents, SSM Parameter Store parameters, and Amazon S3\. A configuration profile includes the following information\.
+ The Uri location of the configuration data\.
+ The AWS Identity and Access Management \(IAM\) role that provides access to the configuration data\.
+ A validator for the configuration data\. Available validators include either a JSON Schema or the Amazon Resource Name \(ARN\) of an AWS Lambda function\.

AWS AppConfig requires that you create resources and deploy a configuration in the following order:

1. Create an application

1. Create an environment

1. Create a configuration profile

1. Create a deployment strategy

1. Deploy the configuration

For more information, see [AWS AppConfig](https://docs.aws.amazon.com/appconfig/latest/userguide/what-is-appconfig.html) in the *AWS AppConfig User Guide*\.

## Syntax<a name="aws-resource-appconfig-configurationprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appconfig-configurationprofile-syntax.json"></a>

```
{
  "Type" : "AWS::AppConfig::ConfigurationProfile",
  "Properties" : {
      "[ApplicationId](#cfn-appconfig-configurationprofile-applicationid)" : String,
      "[Description](#cfn-appconfig-configurationprofile-description)" : String,
      "[LocationUri](#cfn-appconfig-configurationprofile-locationuri)" : String,
      "[Name](#cfn-appconfig-configurationprofile-name)" : String,
      "[RetrievalRoleArn](#cfn-appconfig-configurationprofile-retrievalrolearn)" : String,
      "[Tags](#cfn-appconfig-configurationprofile-tags)" : [ Tags, ... ],
      "[Type](#cfn-appconfig-configurationprofile-type)" : String,
      "[Validators](#cfn-appconfig-configurationprofile-validators)" : [ Validators, ... ]
    }
}
```

### YAML<a name="aws-resource-appconfig-configurationprofile-syntax.yaml"></a>

```
Type: AWS::AppConfig::ConfigurationProfile
Properties: 
  [ApplicationId](#cfn-appconfig-configurationprofile-applicationid): String
  [Description](#cfn-appconfig-configurationprofile-description): String
  [LocationUri](#cfn-appconfig-configurationprofile-locationuri): String
  [Name](#cfn-appconfig-configurationprofile-name): String
  [RetrievalRoleArn](#cfn-appconfig-configurationprofile-retrievalrolearn): String
  [Tags](#cfn-appconfig-configurationprofile-tags): 
    - Tags
  [Type](#cfn-appconfig-configurationprofile-type): String
  [Validators](#cfn-appconfig-configurationprofile-validators): 
    - Validators
```

## Properties<a name="aws-resource-appconfig-configurationprofile-properties"></a>

`ApplicationId`  <a name="cfn-appconfig-configurationprofile-applicationid"></a>
The application ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-z0-9]{4,7}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-appconfig-configurationprofile-description"></a>
A description of the configuration profile\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LocationUri`  <a name="cfn-appconfig-configurationprofile-locationuri"></a>
A URI to locate the configuration\. You can specify the following:  
+ For the AWS AppConfig hosted configuration store and for feature flags, specify `hosted`\.
+ For an AWS Systems Manager Parameter Store parameter, specify either the parameter name in the format `ssm-parameter://<parameter name>` or the ARN\.
+ For an AWS Secrets Manager secret, specify the URI in the following format: `secrets-manager`://<secret name>\.
+ For an Amazon S3 object, specify the URI in the following format: `s3://<bucket>/<objectKey> `\. Here is an example: `s3://my-bucket/my-app/us-east-1/my-config.json` 
+ For an SSM document, specify either the document name in the format `ssm-document://<document name>` or the Amazon Resource Name \(ARN\)\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-appconfig-configurationprofile-name"></a>
A name for the configuration profile\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetrievalRoleArn`  <a name="cfn-appconfig-configurationprofile-retrievalrolearn"></a>
The ARN of an IAM role with permission to access the configuration at the specified `LocationUri`\.  
A retrieval role ARN is not required for configurations stored in the AWS AppConfig hosted configuration store\. It is required for all other sources that store your configuration\. 
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `^((arn):(aws|aws-cn|aws-iso|aws-iso-[a-z]{1}|aws-us-gov):(iam)::\d{12}:role[/].*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appconfig-configurationprofile-tags"></a>
Metadata to assign to the configuration profile\. Tags help organize and categorize your AWS AppConfig resources\. Each tag consists of a key and an optional value, both of which you define\.  
*Required*: No  
*Type*: [List](aws-properties-appconfig-configurationprofile-tags.md) of [Tags](aws-properties-appconfig-configurationprofile-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-appconfig-configurationprofile-type"></a>
The type of configurations contained in the profile\. AWS AppConfig supports `feature flags` and `freeform` configurations\. We recommend you create feature flag configurations to enable or disable new features and freeform configurations to distribute configurations to an application\. When calling this API, enter one of the following values for `Type`:  
 `AWS.AppConfig.FeatureFlags`   
 `AWS.Freeform`   
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z\.]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Validators`  <a name="cfn-appconfig-configurationprofile-validators"></a>
A list of methods for validating the configuration\.  
*Required*: No  
*Type*: [List](aws-properties-appconfig-configurationprofile-validators.md) of [Validators](aws-properties-appconfig-configurationprofile-validators.md)  
*Maximum*: `2`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appconfig-configurationprofile-return-values"></a>

### Ref<a name="aws-resource-appconfig-configurationprofile-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the configuration profile ID\.

## Examples<a name="aws-resource-appconfig-configurationprofile--examples"></a>



### AWS AppConfig configuration profile example \- AWS CodePipeline<a name="aws-resource-appconfig-configurationprofile--examples--_configuration_profile_example_-_"></a>

The following examples creates an AWS AppConfig configuration profile named MyTestConfigurationProfile\. A configuration profile includes source information for accessing your configuration data\. A configuration profile can also include optional validators to ensure your configuration data is syntactically and semantically correct\. The following configuration profile example uses the specified `LocationUri` to retrieve configuration data from AWS CodePipeline\.

#### JSON<a name="aws-resource-appconfig-configurationprofile--examples--_configuration_profile_example_-_--json"></a>

```
{
  "Resources": {
    "CodePipelineConfigurationProfile": {
      "Type": "AWS::AppConfig::ConfigurationProfile",
      "DependsOn": "MyTestApplication",
      "Properties": {
        "ApplicationId": "MyTestApplication",
        "Name": "MyTestConfigurationProfile",
        "Description": "My test configuration profile",
        "LocationUri": "codepipeline://YourPipelineName",
        "Validators": [
          {
            "Type": "LAMBDA",
            "Content": "MyLambdaValidator"
          }
        ],
        "Tags": [
          {
            "Key": "Env",
            "Value": "test"
          }
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-appconfig-configurationprofile--examples--_configuration_profile_example_-_--yaml"></a>

```
Resources:
  CodePipelineConfigurationProfile:
    Type: AWS::AppConfig::ConfigurationProfile
    Properties:
      ApplicationId: !Ref MyTestApplication
      Name: "MyTestConfigurationProfile"
      Description: "My test configuration profile"
      LocationUri: "codepipeline://YourPipelineName"
      Validators:
        - Type: LAMBDA
          Content: !ImportValue MyLambdaValidator
      Tags:
        - Key: Env
          Value: test
```

### AWS AppConfig configuration profile example \- Parameter Store<a name="aws-resource-appconfig-configurationprofile--examples--_configuration_profile_example_-_Parameter_Store"></a>

The following examples creates an AWS AppConfig configuration profile named MyTestConfigurationProfile\. A configuration profile includes source information for accessing your configuration data\. A configuration profile can also include optional validators to ensure your configuration data is syntactically and semantically correct\. The following configuration profile example uses the specified `RetrievalRoleArn` and `LocationUri` to retrieve configuration data from an SSM parameter\.

#### JSON<a name="aws-resource-appconfig-configurationprofile--examples--_configuration_profile_example_-_Parameter_Store--json"></a>

```
{
  "Type": "AWS::AppConfig::ConfigurationProfile",
  "DependsOn": "MyTestApplication",
  "Properties": {
    "ApplicationId": {
      "Ref": "MyTestApplication"
    },
    "Name": "MyTestConfigurationProfile",
    "Description": "My test configuration profile",
    "RetrievalRoleArn": {
      "Fn::ImportValue": "ConfigurationRetrievalAndMonitoringRole"
    },
    "LocationUri": {
      "Fn::Sub": [
        "ssm-parameter://${ParameterName}",
        {
          "ParameterName": {
            "Fn::ImportValue": "SSMParameter"
          }
        }
      ]
    },
    "Validators": [
      {
        "Type": "LAMBDA",
        "Content": {
          "Fn::ImportValue": "MyLambdaValidator"
        }
      }
    ],
    "Tags": [
      {
        "Key": "Env",
        "Value": "Test"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-appconfig-configurationprofile--examples--_configuration_profile_example_-_Parameter_Store--yaml"></a>

```
Resources:
  BasicConfigurationProfile:
    Type: AWS::AppConfig::ConfigurationProfile
    Properties:
      ApplicationId: !Ref MyTestApplication
      Name: "MyTestConfigurationProfile"
      Description: "My test configuration profile"
      RetrievalRoleArn: !ImportValue ConfigurationRetrievalAndMonitoringRole
      LocationUri:
        Fn::Sub:
          - "ssm-parameter://${ParameterName}"
          - ParameterName: !ImportValue SSMParameter
      Validators:
        - Type: LAMBDA
          Content: !ImportValue MyLambdaValidator
      Tags:
        - Key: Env
          Value: test
```

## See also<a name="aws-resource-appconfig-configurationprofile--seealso"></a>
+  [AWS AppConfig](https://docs.aws.amazon.com/appconfig/latest/userguide/what-is-appconfig.html) 
+  [Creating a configuration and a configuration profile ](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig-creating-configuration-and-profile.html)