# AWS::ElasticBeanstalk::Application<a name="aws-properties-beanstalk"></a>

Creates an Elastic Beanstalk application\.


+ [Syntax](#aws-resource-elasticbeanstalk-application-syntax)
+ [Properties](#w3ab2c21c10d570b9)
+ [Return Values](#w3ab2c21c10d570c11)
+ [Example](#w3ab2c21c10d570c13)
+ [See Also](#w3ab2c21c10d570c15)

## Syntax<a name="aws-resource-elasticbeanstalk-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticbeanstalk-application-syntax.json"></a>

```
{
   "Type" : "AWS::ElasticBeanstalk::Application",
   "Properties" : {
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-name)" : String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-description)" : String,
      "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-resourcelifecycleconfig)" : ApplicationResourceLifecycleConfig

   }
}
```

### YAML<a name="aws-resource-elasticbeanstalk-application-syntax.yaml"></a>

```
Type: "AWS::ElasticBeanstalk::Application"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-application-resourcelifecycleconfig):
     ApplicationResourceLifecycleConfig
```

## Properties<a name="w3ab2c21c10d570b9"></a>

`ApplicationName`  
A name for the Elastic Beanstalk application\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the application name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Description`  
An optional description of this application\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`ResourceLifecycleConfig`  
Defines lifecycle settings for resources that belong to the application, and the service role that Elastic Beanstalk assumes in order to apply lifecycle settings\.  
*Required*: No  
 *Type*: [Elastic Beanstalk Application ApplicationResourceLifecycleConfig](aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig.md)  
 *Update requires*: No interruption 

## Return Values<a name="w3ab2c21c10d570c11"></a>

### Ref<a name="w3ab2c21c10d570c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d570c13"></a>

### JSON<a name="aws-resource-elasticbeanstalk-application-example.json"></a>

```
{
   "Type" : "AWS::ElasticBeanstalk::Application",
   "Properties" : {
      "ApplicationName" : "SampleAWSElasticBeanstalkApplication",
      "Description" : "AWS Elastic Beanstalk PHP Sample Application"
   }
}
```

### YAML<a name="aws-resource-elasticbeanstalk-application-example.yaml"></a>

```
Type: "AWS::ElasticBeanstalk::Application"
Properties: 
  ApplicationName: "SampleAWSElasticBeanstalkApplication"
  Description: "AWS Elastic Beanstalk PHP Sample Application"
```

## See Also<a name="w3ab2c21c10d570c15"></a>

+ For a complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](quickref-elasticbeanstalk.md)\.