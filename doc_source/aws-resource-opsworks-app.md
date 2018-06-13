# AWS::OpsWorks::App<a name="aws-resource-opsworks-app"></a>

Defines an AWS OpsWorks app for an AWS OpsWorks stack\. The app specifies the code that you want to run on an application server\.

**Topics**
+ [Syntax](#aws-resource-opsworks-app-syntax)
+ [Properties](#w3ab2c21c10d911b9)
+ [Return Values](#w3ab2c21c10d911c11)
+ [Template Snippet](#w3ab2c21c10d911c13)
+ [More Info](#w3ab2c21c10d911c15)

## Syntax<a name="aws-resource-opsworks-app-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-app-syntax.json"></a>

```
{
  "Type": "AWS::OpsWorks::App",
  "Properties": {
    "[AppSource](#cfn-opsworks-app-appsource)" : Source,
    "[Attributes](#cfn-opsworks-app-attributes)" : { String:String, ... },
    "[DataSources](#cfn-opsworks-app-datasources)" : [ [DataSource](aws-properties-opsworks-app-datasource.md), ... ],
    "[Description](#cfn-opsworks-app-description)" : String,
    "[Domains](#cfn-opsworks-app-domains)" :  [ String, ... ],
    "[EnableSsl](#cfn-opsworks-app-enablessl)" : Boolean,
    "[Environment](#cfn-opsworks-app-environment)" : [ Environment, ... ],
    "[Name](#cfn-opsworks-app-name)" : String,
    "[Shortname](#cfn-opsworks-app-shortname)" : String,
    "[SslConfiguration](#cfn-opsworks-app-sslconfig)" : { SslConfiguration },
    "[StackId](#cfn-opsworks-app-stackid)" : String,
    "[Type](#cfn-opsworks-app-type)" : String
  }
}
```

### YAML<a name="aws-resource-opsworks-app-syntax.yaml"></a>

```
Type: "AWS::OpsWorks::App"
Properties: 
  [AppSource](#cfn-opsworks-app-appsource):
    Source
  [Attributes](#cfn-opsworks-app-attributes):
    String: String
  [Description](#cfn-opsworks-app-description): String
  [DataSources](#cfn-opsworks-app-datasources): 
    - [DataSource](aws-properties-opsworks-app-datasource.md)
  [Domains](#cfn-opsworks-app-domains):
    - String
  [EnableSsl](#cfn-opsworks-app-enablessl): Boolean
  [Environment](#cfn-opsworks-app-environment):
    - Environment
  [Name](#cfn-opsworks-app-name): String
  [Shortname](#cfn-opsworks-app-shortname): String
  [SslConfiguration](#cfn-opsworks-app-sslconfig):
    SslConfiguration
  [StackId](#cfn-opsworks-app-stackid): String
  [Type](#cfn-opsworks-app-type): String
```

## Properties<a name="w3ab2c21c10d911b9"></a>

`AppSource`  <a name="cfn-opsworks-app-appsource"></a>
The information required to retrieve an app from a repository\.  
*Required*: No  
*Type*: [AWS OpsWorks Source Type](aws-properties-opsworks-stack-source.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Attributes`  <a name="cfn-opsworks-app-attributes"></a>
One or more user\-defined key\-value pairs to be added to the app attributes bag\.  
*Required*: No  
*Type*: A list of key\-value pairs  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-opsworks-app-description"></a>
A description of the app\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DataSources`  <a name="cfn-opsworks-app-datasources"></a>
A list of databases to associate with the AWS OpsWorks app\.  
*Required*: No  
*Type*: List of [AWS OpsWorks App DataSource](aws-properties-opsworks-app-datasource.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Domains`  <a name="cfn-opsworks-app-domains"></a>
The app virtual host settings, with multiple domains separated by commas\. For example, `'www.example.com`, `example.com'`\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EnableSsl`  <a name="cfn-opsworks-app-enablessl"></a>
Whether to enable SSL for this app\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Environment`  <a name="cfn-opsworks-app-environment"></a>
The environment variables to associate with the AWS OpsWorks app\.  
*Required*: No  
*Type*: List of [AWS OpsWorks App Environment](aws-properties-opsworks-app-environment.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-opsworks-app-name"></a>
The name of the AWS OpsWorks app\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Shortname`  <a name="cfn-opsworks-app-shortname"></a>
The app short name, which is used internally by AWS OpsWorks and by Chef recipes\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SslConfiguration`  <a name="cfn-opsworks-app-sslconfig"></a>
The SSL configuration  
*Required*: No  
*Type*: [AWS OpsWorks SslConfiguration Type](aws-properties-opsworks-app-sslconfiguration.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`StackId`  <a name="cfn-opsworks-app-stackid"></a>
The ID of the AWS OpsWorks stack to associate this app with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Type`  <a name="cfn-opsworks-app-type"></a>
The app type\. Each supported type is associated with a particular layer\. For more information, see [CreateApp](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateApp.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d911c11"></a>

### Ref<a name="w3ab2c21c10d911c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myApp" }
```

For the AWS OpsWorks stack `myApp`, `Ref` returns the ID of the AWS OpsWorks app\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Template Snippet<a name="w3ab2c21c10d911c13"></a>

The following snippet creates an AWS OpsWorks app that uses a PHP application in a Git repository:

### JSON<a name="aws-resource-opsworks-app-example.json"></a>

```
"myApp" : {
  "Type" : "AWS::OpsWorks::App",
  "Properties" : {
    "StackId" : {"Ref":"myStack"},
    "Type" : "php",
    "Name" : "myPHPapp",
    "AppSource" : {
      "Type" : "git",
      "Url" : "git://github.com/amazonwebservices/opsworks-demo-php-simple-app.git",
      "Revision" : "version1"
    }
  }
}
```

### YAML<a name="aws-resource-opsworks-app-example.yaml"></a>

```
myApp: 
  Type: "AWS::OpsWorks::App"
  Properties: 
    StackId: 
      Ref: "myStack"
    Type: "php"
    Name: "myPHPapp"
    AppSource: 
      Type: "git"
      Url: "git://github.com/amazonwebservices/opsworks-demo-php-simple-app.git"
      Revision: "version1"
```

## More Info<a name="w3ab2c21c10d911c15"></a>
+ [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md)
+ [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md)
+ [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)