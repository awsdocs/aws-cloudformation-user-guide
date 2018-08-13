# AWS::ElasticBeanstalk::Application<a name="aws-properties-beanstalk"></a>

Creates an Elastic Beanstalk application\.

**Topics**
+ [Syntax](#aws-resource-elasticbeanstalk-application-syntax)
+ [Properties](#w3ab2c21c10d615b9)
+ [Return Values](#w3ab2c21c10d615c11)
+ [Example](#w3ab2c21c10d615c13)
+ [See Also](#w3ab2c21c10d615c15)

## Syntax<a name="aws-resource-elasticbeanstalk-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticbeanstalk-application-syntax.json"></a>

```
{
   "Type" : "AWS::ElasticBeanstalk::Application",
   "Properties" : {
      "[ApplicationName](#cfn-elasticbeanstalk-application-name)" : String,
      "[Description](#cfn-elasticbeanstalk-application-description)" : String,
      "[ResourceLifecycleConfig](#cfn-elasticbeanstalk-application-resourcelifecycleconfig)" : [*ApplicationResourceLifecycleConfig*](aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig.md)

   }
}
```

### YAML<a name="aws-resource-elasticbeanstalk-application-syntax.yaml"></a>

```
Type: "AWS::ElasticBeanstalk::Application"
Properties:
  [ApplicationName](#cfn-elasticbeanstalk-application-name): String
  [Description](#cfn-elasticbeanstalk-application-description): String
  [ResourceLifecycleConfig](#cfn-elasticbeanstalk-application-resourcelifecycleconfig):
     [*ApplicationResourceLifecycleConfig*](aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig.md)
```

## Properties<a name="w3ab2c21c10d615b9"></a>

`ApplicationName`  <a name="cfn-elasticbeanstalk-application-name"></a>
A name for the Elastic Beanstalk application\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the application name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Description`  <a name="cfn-elasticbeanstalk-application-description"></a>
An optional description of this application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ResourceLifecycleConfig`  <a name="cfn-elasticbeanstalk-application-resourcelifecycleconfig"></a>
Defines lifecycle settings for resources that belong to the application, and the service role that Elastic Beanstalk assumes in order to apply lifecycle settings\.  
*Required*: No  
 *Type*: [Elastic Beanstalk Application ApplicationResourceLifecycleConfig](aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="w3ab2c21c10d615c11"></a>

### Ref<a name="w3ab2c21c10d615c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d615c13"></a>

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

## See Also<a name="w3ab2c21c10d615c15"></a>
+ For a complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](quickref-elasticbeanstalk.md)\.