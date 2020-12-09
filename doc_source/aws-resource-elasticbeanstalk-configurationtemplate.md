# AWS::ElasticBeanstalk::ConfigurationTemplate<a name="aws-resource-elasticbeanstalk-configurationtemplate"></a>

The AWS::ElasticBeanstalk::ConfigurationTemplate resource is an AWS Elastic Beanstalk resource type that specifies an Elastic Beanstalk configuration template, associated with a specific Elastic Beanstalk application\. You define application configuration settings in a configuration template\. You can then use the configuration template to deploy different versions of the application with the same configuration settings\.

**Note**  
The Elastic Beanstalk console and documentation often refer to configuration templates as *saved configurations*\. When you set configuration options in a saved configuration \(configuration template\), Elastic Beanstalk applies them with a particular precedence as part of applying options from multiple sources\. For more information, see [ Configuration Options](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.

## Syntax<a name="aws-resource-elasticbeanstalk-configurationtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticbeanstalk-configurationtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticBeanstalk::ConfigurationTemplate",
  "Properties" : {
      "[ApplicationName](#cfn-elasticbeanstalk-configurationtemplate-applicationname)" : String,
      "[Description](#cfn-elasticbeanstalk-configurationtemplate-description)" : String,
      "[EnvironmentId](#cfn-elasticbeanstalk-configurationtemplate-environmentid)" : String,
      "[OptionSettings](#cfn-elasticbeanstalk-configurationtemplate-optionsettings)" : [ ConfigurationOptionSetting, ... ],
      "[PlatformArn](#cfn-elasticbeanstalk-configurationtemplate-platformarn)" : String,
      "[SolutionStackName](#cfn-elasticbeanstalk-configurationtemplate-solutionstackname)" : String,
      "[SourceConfiguration](#cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration)" : SourceConfiguration
    }
}
```

### YAML<a name="aws-resource-elasticbeanstalk-configurationtemplate-syntax.yaml"></a>

```
Type: AWS::ElasticBeanstalk::ConfigurationTemplate
Properties: 
  [ApplicationName](#cfn-elasticbeanstalk-configurationtemplate-applicationname): String
  [Description](#cfn-elasticbeanstalk-configurationtemplate-description): String
  [EnvironmentId](#cfn-elasticbeanstalk-configurationtemplate-environmentid): String
  [OptionSettings](#cfn-elasticbeanstalk-configurationtemplate-optionsettings): 
    - ConfigurationOptionSetting
  [PlatformArn](#cfn-elasticbeanstalk-configurationtemplate-platformarn): String
  [SolutionStackName](#cfn-elasticbeanstalk-configurationtemplate-solutionstackname): String
  [SourceConfiguration](#cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration): 
    SourceConfiguration
```

## Properties<a name="aws-resource-elasticbeanstalk-configurationtemplate-properties"></a>

`ApplicationName`  <a name="cfn-elasticbeanstalk-configurationtemplate-applicationname"></a>
The name of the Elastic Beanstalk application to associate with this configuration template\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-elasticbeanstalk-configurationtemplate-description"></a>
An optional description for this configuration\.  
*Required*: No  
*Type*: String  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnvironmentId`  <a name="cfn-elasticbeanstalk-configurationtemplate-environmentid"></a>
The ID of an environment whose settings you want to use to create the configuration template\. You must specify `EnvironmentId` if you don't specify `PlatformArn`, `SolutionStackName`, or `SourceConfiguration`\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OptionSettings`  <a name="cfn-elasticbeanstalk-configurationtemplate-optionsettings"></a>
Option values for the Elastic Beanstalk configuration, such as the instance type\. If specified, these values override the values obtained from the solution stack or the source configuration template\. For a complete list of Elastic Beanstalk configuration options, see [Option Values](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
*Required*: No  
*Type*: List of [ConfigurationOptionSetting](aws-properties-elasticbeanstalk-configurationtemplate-configurationoptionsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PlatformArn`  <a name="cfn-elasticbeanstalk-configurationtemplate-platformarn"></a>
The Amazon Resource Name \(ARN\) of the custom platform\. For more information, see [ Custom Platforms](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/custom-platforms.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
If you specify `PlatformArn`, then don't specify `SolutionStackName`\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SolutionStackName`  <a name="cfn-elasticbeanstalk-configurationtemplate-solutionstackname"></a>
The name of an Elastic Beanstalk solution stack \(platform version\) that this configuration uses\. For example, `64bit Amazon Linux 2013.09 running Tomcat 7 Java 7`\. A solution stack specifies the operating system, runtime, and application server for a configuration template\. It also determines the set of configuration options as well as the possible and default values\. For more information, see [Supported Platforms](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.platforms.html) in the *AWS Elastic Beanstalk Developer Guide*\.  
You must specify `SolutionStackName` if you don't specify `PlatformArn`, `EnvironmentId`, or `SourceConfiguration`\.  
Use the [ `ListAvailableSolutionStacks` ](https://docs.aws.amazon.com/elasticbeanstalk/latest/api/API_ListAvailableSolutionStacks.html) API to obtain a list of available solution stacks\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceConfiguration`  <a name="cfn-elasticbeanstalk-configurationtemplate-sourceconfiguration"></a>
An Elastic Beanstalk configuration template to base this one on\. If specified, Elastic Beanstalk uses the configuration values from the specified configuration template to create a new configuration\.  
Values specified in `OptionSettings` override any values obtained from the `SourceConfiguration`\.  
You must specify `SourceConfiguration` if you don't specify `PlatformArn`, `EnvironmentId`, or `SolutionStackName`\.  
Constraint: If both solution stack name and source configuration are specified, the solution stack of the source configuration template must match the specified solution stack name\.  
*Required*: Conditional  
*Type*: [SourceConfiguration](aws-properties-elasticbeanstalk-configurationtemplate-sourceconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-elasticbeanstalk-configurationtemplate-return-values"></a>

### Ref<a name="aws-resource-elasticbeanstalk-configurationtemplate-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-elasticbeanstalk-configurationtemplate--examples"></a>

### <a name="aws-resource-elasticbeanstalk-configurationtemplate--examples--"></a>

#### JSON<a name="aws-resource-elasticbeanstalk-configurationtemplate--examples----json"></a>

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

#### YAML<a name="aws-resource-elasticbeanstalk-configurationtemplate--examples----yaml"></a>

```
myConfigTemplate: 
  Type: AWS::ElasticBeanstalk::ConfigurationTemplate
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

## See also<a name="aws-resource-elasticbeanstalk-configurationtemplate--seealso"></a>
+  [AWS::ElasticBeanstalk::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk.html) 
+  [Configuration Options](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options.html) in the *AWS Elastic Beanstalk Developer Guide* 
+ For a complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-elasticbeanstalk.html)\.