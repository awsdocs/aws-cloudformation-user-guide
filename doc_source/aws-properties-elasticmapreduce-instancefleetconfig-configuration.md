# AWS::EMR::InstanceFleetConfig Configuration<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration"></a>

**Note**  
Used only with Amazon EMR release 4\.0 and later\.

`Configuration` specifies optional configurations for customizing open\-source big data applications and environment parameters\. A configuration consists of a classification, properties, and optional nested configurations\. A classification refers to an application\-specific configuration file\. Properties are the settings you want to change in that file\. For more information, see [Configuring Applications](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-configure-apps.html) in the *Amazon EMR Release Guide*\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration-syntax.json"></a>

```
{
  "[Classification](#cfn-elasticmapreduce-instancefleetconfig-configuration-classification)" : String,
  "[ConfigurationProperties](#cfn-elasticmapreduce-instancefleetconfig-configuration-configurationproperties)" : {Key : Value, ...},
  "[Configurations](#cfn-elasticmapreduce-instancefleetconfig-configuration-configurations)" : [ Configuration, ... ]
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration-syntax.yaml"></a>

```
  [Classification](#cfn-elasticmapreduce-instancefleetconfig-configuration-classification): String
  [ConfigurationProperties](#cfn-elasticmapreduce-instancefleetconfig-configuration-configurationproperties): 
    Key : Value
  [Configurations](#cfn-elasticmapreduce-instancefleetconfig-configuration-configurations): 
    - Configuration
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration-properties"></a>

`Classification`  <a name="cfn-elasticmapreduce-instancefleetconfig-configuration-classification"></a>
The classification within a configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationProperties`  <a name="cfn-elasticmapreduce-instancefleetconfig-configuration-configurationproperties"></a>
Within a configuration classification, a set of properties that represent the settings that you want to change in the configuration file\. Duplicates not allowed\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Configurations`  <a name="cfn-elasticmapreduce-instancefleetconfig-configuration-configurations"></a>
A list of additional configurations to apply within a configuration object\.  
*Required*: No  
*Type*: List of [Configuration](#aws-properties-elasticmapreduce-instancefleetconfig-configuration)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)