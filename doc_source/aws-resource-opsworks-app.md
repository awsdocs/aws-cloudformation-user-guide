# AWS::OpsWorks::App<a name="aws-resource-opsworks-app"></a>

Defines an AWS OpsWorks app for an AWS OpsWorks stack\. The app specifies the code that you want to run on an application server\.


+ [Syntax](#aws-resource-opsworks-app-syntax)
+ [Properties](#w3ab2c21c10d839b9)
+ [Return Values](#w3ab2c21c10d839c11)
+ [Template Snippet](#w3ab2c21c10d839c13)
+ [More Info](#w3ab2c21c10d839c15)

## Syntax<a name="aws-resource-opsworks-app-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworks-app-syntax.json"></a>

```
{
  "Type": "AWS::OpsWorks::App",
  "Properties": {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-appsource)" : Source,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-attributes)" : { String:String, ... },
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-datasources)" : [ DataSource, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-domains)" :  [ String, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-enablessl)" : Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-environment)" : [ Environment, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-shortname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-sslconfig)" : { SslConfiguration },
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-stackid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-type)" : String
  }
}
```

### YAML<a name="aws-resource-opsworks-app-syntax.yaml"></a>

```
Type: "AWS::OpsWorks::App"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-appsource):
    Source
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-attributes):
    String: String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-datasources): 
    - DataSource
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-domains):
    - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-enablessl): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-environment):
    - Environment
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-shortname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-sslconfig):
    SslConfiguration
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-stackid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-opsworks-app-type): String
```

## Properties<a name="w3ab2c21c10d839b9"></a>

`AppSource`  
The information required to retrieve an app from a repository\.  
*Required: *No  
*Type*: [AWS OpsWorks Source Type](aws-properties-opsworks-stack-source.md)  
*Update requires*: No interruption

`Attributes`  
One or more user\-defined key\-value pairs to be added to the app attributes bag\.  
*Required: *No  
*Type*: A list of key\-value pairs  
*Update requires*: No interruption

`Description`  
A description of the app\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`DataSources`  
A list of databases to associate with the AWS OpsWorks app\.  
*Required: *No  
*Type*: List of [AWS OpsWorks App DataSource](aws-properties-opsworks-app-datasource.md)  
*Update requires*: No interruption

`Domains`  
The app virtual host settings, with multiple domains separated by commas\. For example, `'www.example.com`, `example.com'`\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

`EnableSsl`  
Whether to enable SSL for this app\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`Environment`  
The environment variables to associate with the AWS OpsWorks app\.  
*Required: *No  
*Type*: List of [AWS OpsWorks App Environment](aws-properties-opsworks-app-environment.md)  
*Update requires*: No interruption

`Name`  
The name of the AWS OpsWorks app\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

`Shortname`  
The app short name, which is used internally by AWS OpsWorks and by Chef recipes\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`SslConfiguration`  
The SSL configuration  
*Required: *No  
*Type*: [AWS OpsWorks SslConfiguration Type](aws-properties-opsworks-app-sslconfiguration.md)  
*Update requires*: No interruption

`StackId`  
The ID of the AWS OpsWorks stack to associate this app with\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Type`  
The app type\. Each supported type is associated with a particular layer\. For more information, see [CreateApp](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateApp.html) in the *AWS OpsWorks Stacks API Reference*\.  
*Required: *Yes  
*Type*: String  
*Update requires*: No interruption

## Return Values<a name="w3ab2c21c10d839c11"></a>

### Ref<a name="w3ab2c21c10d839c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "myApp" }
```

For the AWS OpsWorks stack `myApp`, `Ref` returns the ID of the AWS OpsWorks app\.

For more information about using the `Ref` function, see Ref\.

## Template Snippet<a name="w3ab2c21c10d839c13"></a>

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

## More Info<a name="w3ab2c21c10d839c15"></a>

+ [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md)

+ [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md)

+ [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)