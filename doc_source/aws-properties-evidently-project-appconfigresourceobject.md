# AWS::Evidently::Project AppConfigResourceObject<a name="aws-properties-evidently-project-appconfigresourceobject"></a>

This is a structure that defines the configuration of how your application integrates with AWS AppConfig to run client\-side evaluation\.

## Syntax<a name="aws-properties-evidently-project-appconfigresourceobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-evidently-project-appconfigresourceobject-syntax.json"></a>

```
{
  "[ApplicationId](#cfn-evidently-project-appconfigresourceobject-applicationid)" : String,
  "[EnvironmentId](#cfn-evidently-project-appconfigresourceobject-environmentid)" : String
}
```

### YAML<a name="aws-properties-evidently-project-appconfigresourceobject-syntax.yaml"></a>

```
  [ApplicationId](#cfn-evidently-project-appconfigresourceobject-applicationid): String
  [EnvironmentId](#cfn-evidently-project-appconfigresourceobject-environmentid): String
```

## Properties<a name="aws-properties-evidently-project-appconfigresourceobject-properties"></a>

`ApplicationId`  <a name="cfn-evidently-project-appconfigresourceobject-applicationid"></a>
The ID of the AWS AppConfig application to use for client\-side evaluation\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentId`  <a name="cfn-evidently-project-appconfigresourceobject-environmentid"></a>
The ID of the AWS AppConfig environment to use for client\-side evaluation\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)