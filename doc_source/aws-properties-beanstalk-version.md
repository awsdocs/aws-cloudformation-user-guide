# AWS::ElasticBeanstalk::ApplicationVersion<a name="aws-properties-beanstalk-version"></a>

Creates an application version, an iteration of deployable code, for an Elastic Beanstalk application\.

**Topics**
+ [Syntax](#aws-resource-elasticbeanstalk-applicationversion-syntax)
+ [Members](#w3ab2c21c10d619b9)
+ [Return Values](#w3ab2c21c10d619c11)
+ [Example](#w3ab2c21c10d619c13)
+ [See Also](#w3ab2c21c10d619c15)

## Syntax<a name="aws-resource-elasticbeanstalk-applicationversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticbeanstalk-applicationversion-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticBeanstalk::ApplicationVersion",
  "Properties" : {
    "[ApplicationName](#cfn-elasticbeanstalk-applicationversion-applicationname)" : String,
    "[Description](#cfn-elasticbeanstalk-applicationversion-description)" : String,
    "[SourceBundle](#cfn-elasticbeanstalk-applicationversion-sourcebundle)" : { SourceBundle }
  }
}
```

### YAML<a name="aws-resource-elasticbeanstalk-applicationversion-syntax.yaml"></a>

```
Type: AWS::ElasticBeanstalk::ApplicationVersion
Properties:
  [ApplicationName](#cfn-elasticbeanstalk-applicationversion-applicationname): String
  [Description](#cfn-elasticbeanstalk-applicationversion-description): String
  [SourceBundle](#cfn-elasticbeanstalk-applicationversion-sourcebundle):
    SourceBundle
```

## Members<a name="w3ab2c21c10d619b9"></a>

`ApplicationName`  <a name="cfn-elasticbeanstalk-applicationversion-applicationname"></a>
Name of the Elastic Beanstalk application that is associated with this application version\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Description`  <a name="cfn-elasticbeanstalk-applicationversion-description"></a>
A description of this application version\.  
*Required*: No  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`SourceBundle`  <a name="cfn-elasticbeanstalk-applicationversion-sourcebundle"></a>
The location of the source bundle for this version\.  
*Required*: Yes  
*Type*: [Source Bundle](aws-properties-beanstalk-sourcebundle.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10d619c11"></a>

### Ref<a name="w3ab2c21c10d619c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d619c13"></a>

### JSON<a name="aws-resource-elasticbeanstalk-applicationversion-example.json"></a>

```
"myAppVersion" :{ 
  "Type" : "AWS::ElasticBeanstalk::ApplicationVersion",
  "Properties" : {
    "ApplicationName" : {"Ref" : "myApp"},
    "Description" : "my sample version",
    "SourceBundle" : {
      "S3Bucket" : { "Fn::Join" :
        ["-", [ "elasticbeanstalk-samples", { "Ref" : "AWS::Region" } ] ] },
      "S3Key" : "php-sample.zip"
    } 
  }
}
```

### YAML<a name="aws-resource-elasticbeanstalk-applicationversion-example.yaml"></a>

```
myAppVersion: 
  Type: "AWS::ElasticBeanstalk::ApplicationVersion"
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
      S3Key: "php-sample.zip"
```

## See Also<a name="w3ab2c21c10d619c15"></a>
+ For a complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](quickref-elasticbeanstalk.md)\.