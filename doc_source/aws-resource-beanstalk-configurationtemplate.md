# AWS::ElasticBeanstalk::ConfigurationTemplate<a name="aws-resource-beanstalk-configurationtemplate"></a>

Creates a configuration template for an Elastic Beanstalk application\. You can use configuration templates to deploy different versions of an application by using the configuration settings that you define in the configuration template\.


+ [Syntax](#aws-resource-elasticbeanstalk-configurationtemplate-syntax)
+ [Properties](#w3ab2c21c10d578b9)
+ [Return Values](#w3ab2c21c10d578c11)
+ [Example](#w3ab2c21c10d578c13)
+ [See Also](#w3ab2c21c10d578c15)

## Syntax<a name="aws-resource-elasticbeanstalk-configurationtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticbeanstalk-configurationtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticBeanstalk::ConfigurationTemplate",
  "Properties" : {  
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-applicationname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-environmentid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-optionsettings)" : [ ConfigurationOptionSetting, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-platformarn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-solutionstackname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration)" : SourceConfiguration
  } 
}
```

### YAML<a name="aws-resource-elasticbeanstalk-configurationtemplate-syntax.yaml"></a>

```
Type: "AWS::ElasticBeanstalk::ConfigurationTemplate"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-applicationname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-environmentid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-optionsettings):
    - ConfigurationOptionSetting
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-platformarn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-solutionstackname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration):
    SourceConfiguration
```

## Properties<a name="w3ab2c21c10d578b9"></a>

For more information, see [ CreateConfigurationTemplate](http://docs.aws.amazon.com/elasticbeanstalk/latest/api/API_CreateConfigurationTemplate.html) in the *AWS Elastic Beanstalk API Reference*\.

`ApplicationName`  
Name of the Elastic Beanstalk application that is associated with this configuration template\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Description`  
An optional description for this configuration\.  
*Type*: String  
*Required: *No  
*Update requires*: Some interruptions

`EnvironmentId`  
An environment whose settings you want to use to create the configuration template\. You must specify this property if you don't specify the `SolutionStackName` or `SourceConfiguration` properties\.  
*Type*: String  
*Required: *Conditional  
*Update requires*: Replacement

`OptionSettings`  
The options for the Elastic Beanstalk configuration, such as the instance type\. For a complete list of Elastic Beanstalk configuration options, see [ Option Values](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html), in the *AWS Elastic Beanstalk Developer Guide*\.  
*Type*: List of [Elastic Beanstalk ConfigurationTemplate ConfigurationOptionSetting](aws-properties-elasticbeanstalk-configurationtemplate-configurationoptionsetting.md)   
*Required: *No  
*Update requires*: Some interruptions

`PlatformArn`  
The Amazon Resource Name \(ARN\) of the custom platform\. For more information, see [ Custom Platforms](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/custom-platforms.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
If you specify `PlatformArn`, then don't specify `SolutionStackName`\.
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`SolutionStackName`  
The name of an Elastic Beanstalk solution stack that this configuration will use\. A solution stack specifies the operating system, architecture, and application server for a configuration template, such as `64bit Amazon Linux 2013.09 running Tomcat 7 Java 7`\. For more information, see [Supported Platforms](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.platforms.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
You must specify this property if you don't specify the `PlatformArn`, `EnvironmentId`, or `SourceConfiguration` properties\.  
*Type*: String  
*Required: *Conditional  
*Update requires*: Replacement

`SourceConfiguration`  
A configuration template that is associated with another Elastic Beanstalk application\. If you specify the `SolutionStackName` property and the `SourceConfiguration` property, the solution stack in the source configuration template must match the value that you specified for the `SolutionStackName` property\.  
You must specify this property if you don't specify the `EnvironmentId` or `SolutionStackName` properties\.  
*Type*: [Elastic Beanstalk ConfigurationTemplate SourceConfiguration](aws-properties-beanstalk-configurationtemplate-sourceconfiguration.md)  
*Required: *Conditional  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d578c11"></a>

### Ref<a name="w3ab2c21c10d578c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d578c13"></a>

This example of an ElasticBeanstalk `ConfigurationTemplate` is found in the AWS CloudFormation sample template [ElasticBeanstalkSample\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/ElasticBeanstalkSample.template), which also provides an example of its use within an `AWS::ElasticBeanstalk::Application`\.

### JSON<a name="aws-resource-elasticbeanstalk-configurationtemplate-example.json"></a>

```
"myConfigTemplate" : { 
  "Type" : "AWS::ElasticBeanstalk::ConfigurationTemplate",
  "Properties" : {
    "ApplicationName" :{"Ref" : "myApp"},
    "Description" : "my sample configuration template",
    "EnvironmentId" : "",
    "SourceConfiguration" : {
      "ApplicationName" : {"Ref" : "mySecondApp"},
      "TemplateName" : {"Ref" : "mySourceTemplate"}
    }, 
    "SolutionStackName" : "64bit Amazon Linux running PHP 5.3",
    "OptionSettings" : [ {
      "Namespace" : "aws:autoscaling:launchconfiguration",
      "OptionName" : "EC2KeyName",
      "Value" : { "Ref" : "KeyName" }
    } ]
  }
}
```

### YAML<a name="aws-resource-elasticbeanstalk-configurationtemplate-example.yaml"></a>

```
myConfigTemplate: 
  Type: "AWS::ElasticBeanstalk::ConfigurationTemplate"
  Properties: 
    ApplicationName: 
      Ref: "myApp"
    Description: "my sample configuration template"
    EnvironmentId: ""
    SourceConfiguration: 
      ApplicationName: 
        Ref: "mySecondApp"
      TemplateName: 
        Ref: "mySourceTemplate"
    SolutionStackName: "64bit Amazon Linux running PHP 5.3"
    OptionSettings: 
      - 
        Namespace: "aws:autoscaling:launchconfiguration"
        OptionName: "EC2KeyName"
        Value: 
          Ref: "KeyName"
```

## See Also<a name="w3ab2c21c10d578c15"></a>

+ 

+ [Option Values](http://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*

+ For a complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](quickref-elasticbeanstalk.md)\.