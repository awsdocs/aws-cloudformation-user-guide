# AWS::AppConfig::Application<a name="aws-resource-appconfig-application"></a>

The `AWS::AppConfig::Application` resource creates an application, which is a logical unit of code that provides capabilities for your customers\. For example, an application can be a microservice that runs on Amazon EC2 instances, a mobile application installed by your users, a serverless application using Amazon API Gateway and AWS Lambda, or any system you run on behalf of others\.

AppConfig requires that you create resources and deploy a configuration in the following order:

1. Create an application

1. Create an environment

1. Create a configuration profile

1. Create a deployment strategy

1. Deploy the configuration

For more information, see [AWS AppConfig](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig.html) in the *AWS Systems Manager User Guide*\.

## Syntax<a name="aws-resource-appconfig-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appconfig-application-syntax.json"></a>

```
{
  "Type" : "AWS::AppConfig::Application",
  "Properties" : {
      "[Description](#cfn-appconfig-application-description)" : String,
      "[Name](#cfn-appconfig-application-name)" : String,
      "[Tags](#cfn-appconfig-application-tags)" : [ Tags, ... ]
    }
}
```

### YAML<a name="aws-resource-appconfig-application-syntax.yaml"></a>

```
Type: AWS::AppConfig::Application
Properties: 
  [Description](#cfn-appconfig-application-description): String
  [Name](#cfn-appconfig-application-name): String
  [Tags](#cfn-appconfig-application-tags): 
    - Tags
```

## Properties<a name="aws-resource-appconfig-application-properties"></a>

`Description`  <a name="cfn-appconfig-application-description"></a>
A description of the application\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appconfig-application-name"></a>
A name for the application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appconfig-application-tags"></a>
Metadata to assign to the application\. Tags help organize and categorize your AWS AppConfig resources\. Each tag consists of a key and an optional value, both of which you define\.  
*Required*: No  
*Type*: [List](aws-properties-appconfig-application-tags.md) of [Tags](aws-properties-appconfig-application-tags.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appconfig-application-return-values"></a>

### Ref<a name="aws-resource-appconfig-application-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the application ID\.

## Examples<a name="aws-resource-appconfig-application--examples"></a>



### AWS AppConfig Application Example<a name="aws-resource-appconfig-application--examples--AWS_AppConfig_Application_Example"></a>

The following example creates a simple AWS AppConfig application named MyTestApplication\. An application in AWS AppConfig is a logical unit of code that provides capabilities for your customers\. For example, an application can be a microservice that runs on Amazon EC2 instances, a mobile application installed by your users, a serverless application using Amazon API Gateway and AWS Lambda, or any system you run on behalf of others\. 

#### JSON<a name="aws-resource-appconfig-application--examples--AWS_AppConfig_Application_Example--json"></a>

```
BasicApplication": {
    "Type": "AWS::AppConfig::Application",
    "Properties": {
      "Name": "MyTestApplication",
      "Description": "A sample test application.",
      "Tags": [
        {
          "Key": "Env",
          "Value": "test"
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-appconfig-application--examples--AWS_AppConfig_Application_Example--yaml"></a>

```
BasicApplication:
    Type: AWS::AppConfig::Application
    Properties:
      Name: "MyTestApplication"
      Description: "A sample test application."
      Tags:
        - Key: Env
          Value: test
```

## See also<a name="aws-resource-appconfig-application--seealso"></a>
+  [AWS AppConfig](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig.html) 
+  [Creating an Application](https://docs.aws.amazon.com/systems-manager/latest/userguide/appconfig-creating-application.html)