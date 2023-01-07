# AWS::ElasticBeanstalk::ApplicationVersion<a name="aws-properties-beanstalk-version"></a>

The AWS::ElasticBeanstalk::ApplicationVersion resource is an AWS Elastic Beanstalk resource type that specifies an application version, an iteration of deployable code, for an Elastic Beanstalk application\.

**Note**  
After you create an application version with a specified Amazon S3 bucket and key location, you can't change that Amazon S3 location\. If you change the Amazon S3 location, an attempt to launch an environment from the application version will fail\.

## Syntax<a name="aws-properties-beanstalk-version-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-beanstalk-version-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticBeanstalk::ApplicationVersion",
  "Properties" : {
      "[ApplicationName](#cfn-elasticbeanstalk-applicationversion-applicationname)" : String,
      "[Description](#cfn-elasticbeanstalk-applicationversion-description)" : String,
      "[SourceBundle](#cfn-elasticbeanstalk-applicationversion-sourcebundle)" : SourceBundle
    }
}
```

### YAML<a name="aws-properties-beanstalk-version-syntax.yaml"></a>

```
Type: AWS::ElasticBeanstalk::ApplicationVersion
Properties: 
  [ApplicationName](#cfn-elasticbeanstalk-applicationversion-applicationname): String
  [Description](#cfn-elasticbeanstalk-applicationversion-description): String
  [SourceBundle](#cfn-elasticbeanstalk-applicationversion-sourcebundle): 
    SourceBundle
```

## Properties<a name="aws-properties-beanstalk-version-properties"></a>

`ApplicationName`  <a name="cfn-elasticbeanstalk-applicationversion-applicationname"></a>
The name of the Elastic Beanstalk application that is associated with this application version\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-elasticbeanstalk-applicationversion-description"></a>
A description of this application version\.  
*Required*: No  
*Type*: String  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceBundle`  <a name="cfn-elasticbeanstalk-applicationversion-sourcebundle"></a>
The Amazon S3 bucket and key that identify the location of the source bundle for this version\.  
The Amazon S3 bucket must be in the same region as the environment\.
*Required*: Yes  
*Type*: [SourceBundle](aws-properties-beanstalk-sourcebundle.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-properties-beanstalk-version-return-values"></a>

### Ref<a name="aws-properties-beanstalk-version-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-properties-beanstalk-version--examples"></a>

### <a name="aws-properties-beanstalk-version--examples--"></a>

#### JSON<a name="aws-properties-beanstalk-version--examples----json"></a>

```
"myAppVersion": { 
  "Type" : "AWS::ElasticBeanstalk::ApplicationVersion",
  "Properties" : {
    "ApplicationName" : {"Ref" : "myApp"},
    "Description" : "my sample version",
    "SourceBundle" : {
      "S3Bucket" : { "Fn::Join" :
        ["-", [ "elasticbeanstalk-samples", { "Ref" : "AWS::Region" } ] ] },
      "S3Key" : "php-newsample-app.zip"
    } 
  }
}
```

#### YAML<a name="aws-properties-beanstalk-version--examples----yaml"></a>

```
myAppVersion: 
  Type: AWS::ElasticBeanstalk::ApplicationVersion
  Properties: 
    ApplicationName: 
      Ref: "myApp"
    Description: "my sample version"
    SourceBundle: 
      S3Bucket: 
        Fn::Join: 
          - "-"
          - 
            - "elasticbeanstalk-samples"
            - Ref: "AWS::Region"
      S3Key: "php-newsample-app.zip"
```

## See also<a name="aws-properties-beanstalk-version--seealso"></a>
+ For a complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-elasticbeanstalk.html)\.