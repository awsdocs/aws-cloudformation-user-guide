# AWS::ElasticBeanstalk::ApplicationVersion<a name="aws-properties-beanstalk-version"></a>

Creates an application version, an iteration of deployable code, for an Elastic Beanstalk application\.


+ [Syntax](#aws-resource-elasticbeanstalk-applicationversion-syntax)
+ [Members](#w3ab2c21c10d574b9)
+ [Return Values](#w3ab2c21c10d574c11)
+ [Example](#w3ab2c21c10d574c13)
+ [See Also](#w3ab2c21c10d574c15)

## Syntax<a name="aws-resource-elasticbeanstalk-applicationversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticbeanstalk-applicationversion-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticBeanstalk::ApplicationVersion",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-applicationversion-applicationname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-applicationversion-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-applicationversion-sourcebundle)" : { SourceBundle }
  }
}
```

### YAML<a name="aws-resource-elasticbeanstalk-applicationversion-syntax.yaml"></a>

```
Type: AWS::ElasticBeanstalk::ApplicationVersion
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-applicationversion-applicationname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-applicationversion-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-elasticbeanstalk-applicationversion-sourcebundle):
    SourceBundle
```

## Members<a name="w3ab2c21c10d574b9"></a>

`ApplicationName`  
Name of the Elastic Beanstalk application that is associated with this application version\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Description`  
A description of this application version\.  
*Required: *No  
*Type*: String  
*Update requires*: Some interruptions

`SourceBundle`  
The location of the source bundle for this version\.  
*Required: *Yes  
*Type*: Source Bundle  
*Update requires*: Replacement

## Return Values<a name="w3ab2c21c10d574c11"></a>

### Ref<a name="w3ab2c21c10d574c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="w3ab2c21c10d574c13"></a>

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

## See Also<a name="w3ab2c21c10d574c15"></a>

+ For a complete Elastic Beanstalk sample template, see [Elastic Beanstalk Template Snippets](quickref-elasticbeanstalk.md)\.