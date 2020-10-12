# AWS::ElasticBeanstalk::Application<a name="aws-properties-beanstalk"></a>

The AWS::ElasticBeanstalk::Application resource is an AWS Elastic Beanstalk resource type that specifies an Elastic Beanstalk application\.

## Syntax<a name="aws-properties-beanstalk-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-beanstalk-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticBeanstalk::Application",
  "Properties" : {
      "[ApplicationName](#cfn-elasticbeanstalk-application-name)" : String,
      "[Description](#cfn-elasticbeanstalk-application-description)" : String,
      "[ResourceLifecycleConfig](#cfn-elasticbeanstalk-application-resourcelifecycleconfig)" : ApplicationResourceLifecycleConfig
    }
}
```

### YAML<a name="aws-properties-beanstalk-syntax.yaml"></a>

```
Type: AWS::ElasticBeanstalk::Application
Properties: 
  [ApplicationName](#cfn-elasticbeanstalk-application-name): String
  [Description](#cfn-elasticbeanstalk-application-description): String
  [ResourceLifecycleConfig](#cfn-elasticbeanstalk-application-resourcelifecycleconfig): 
    ApplicationResourceLifecycleConfig
```

## Properties<a name="aws-properties-beanstalk-properties"></a>

`ApplicationName`  <a name="cfn-elasticbeanstalk-application-name"></a>
A name for the Elastic Beanstalk application\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the application name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-elasticbeanstalk-application-description"></a>
Your description of the application\.  
*Required*: No  
*Type*: String  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceLifecycleConfig`  <a name="cfn-elasticbeanstalk-application-resourcelifecycleconfig"></a>
Specifies an application resource lifecycle configuration to prevent your application from accumulating too many versions\.  
*Required*: No  
*Type*: [ApplicationResourceLifecycleConfig](aws-properties-elasticbeanstalk-application-applicationresourcelifecycleconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-beanstalk-return-values"></a>

### Ref<a name="aws-properties-beanstalk-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-beanstalk--examples"></a>

### <a name="aws-properties-beanstalk--examples--"></a>

#### JSON<a name="aws-properties-beanstalk--examples----json"></a>

```
{
   "Type" : "AWS::ElasticBeanstalk::Application",
   "Properties" : {
      "ApplicationName" : "SampleAWSElasticBeanstalkApplication",
      "Description" : "AWS Elastic Beanstalk PHP Sample Application"
   }
}
```

#### YAML<a name="aws-properties-beanstalk--examples----yaml"></a>

```
Type: AWS::ElasticBeanstalk::Application
Properties: 
  ApplicationName: "SampleAWSElasticBeanstalkApplication"
  Description: "AWS Elastic Beanstalk PHP Sample Application"
```

## See also<a name="aws-properties-beanstalk--seealso"></a>
+ For a complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-elasticbeanstalk.html)\.