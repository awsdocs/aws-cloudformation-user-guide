# Amazon EMR Cluster Configurations<a name="aws-properties-emr-cluster-configuration"></a>

`Configurations` is a property of the [AWS::EMR::Cluster](aws-resource-emr-cluster.md) resource that specifies the software configuration of an Amazon EMR \(Amazon EMR\) cluster\. For example configurations, see [Configuring Applications](http://docs.aws.amazon.com//ElasticMapReduce/latest/ReleaseGuide/emr-configure-apps.html) in the *Amazon EMR Release Guide*\.

## Syntax<a name="w3ab2c21c14d886b5"></a>

### JSON<a name="aws-properties-emr-cluster-configuration-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-configuration-classification)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-configuration-configurationproperties)" : { String:String, ... },
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-configuration-configurations)" : [ Configuration, ... ]
}
```

### YAML<a name="aws-properties-emr-cluster-configuration-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-configuration-classification): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-configuration-configurationproperties):
  String: String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-configuration-configurations):
  - Configuration
```

## Properties<a name="w3ab2c21c14d886b7"></a>

`Classification`  
The name of an application\-specific configuration file\. For more information see, [Configuring Applications](http://docs.aws.amazon.com//ElasticMapReduce/latest/ReleaseGuide/emr-configure-apps.html) in the *Amazon EMR Release Guide*\.  
*Required: *No  
*Type*: String

`ConfigurationProperties`  
The settings that you want to change in the application\-specific configuration file\. For more information see, [Configuring Applications](http://docs.aws.amazon.com//ElasticMapReduce/latest/ReleaseGuide/emr-configure-apps.html) in the *Amazon EMR Release Guide*\.  
*Required: *No  
*Type*: String\-to\-string map

`Configurations`  
A list of configurations to apply to this configuration\. You can nest configurations so that a single configuration can have its own configurations\. In other words, you can configure a configuration\. For more information see, [Configuring Applications](http://docs.aws.amazon.com//ElasticMapReduce/latest/ReleaseGuide/emr-configure-apps.html) in the *Amazon EMR Release Guide*\.  
*Required: *No  
*Type*: List of [Amazon EMR Cluster Configurations](#aws-properties-emr-cluster-configuration)