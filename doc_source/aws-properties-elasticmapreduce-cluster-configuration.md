# AWS::EMR::Cluster Configuration<a name="aws-properties-elasticmapreduce-cluster-configuration"></a>

**Note**  
Used only with Amazon EMR release 4\.0 and later\.

`Configuration` is a subproperty of `InstanceFleetConfig` or `InstanceGroupConfig`\. `Configuration` specifies optional configurations for customizing open\-source big data applications and environment parameters\. A configuration consists of a classification, properties, and optional nested configurations\. A classification refers to an application\-specific configuration file\. Properties are the settings you want to change in that file\. For more information, see [Configuring Applications](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-configure-apps.html) in the *Amazon EMR Release Guide*\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-configuration-syntax.json"></a>

```
{
  "[Classification](#cfn-elasticmapreduce-cluster-configuration-classification)" : String,
  "[ConfigurationProperties](#cfn-elasticmapreduce-cluster-configuration-configurationproperties)" : {Key : Value, ...},
  "[Configurations](#cfn-elasticmapreduce-cluster-configuration-configurations)" : [ Configuration, ... ]
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-configuration-syntax.yaml"></a>

```
  [Classification](#cfn-elasticmapreduce-cluster-configuration-classification): String
  [ConfigurationProperties](#cfn-elasticmapreduce-cluster-configuration-configurationproperties): 
    Key : Value
  [Configurations](#cfn-elasticmapreduce-cluster-configuration-configurations): 
    - Configuration
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-configuration-properties"></a>

`Classification`  <a name="cfn-elasticmapreduce-cluster-configuration-classification"></a>
The classification within a configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfigurationProperties`  <a name="cfn-elasticmapreduce-cluster-configuration-configurationproperties"></a>
A list of additional configurations to apply within a configuration object\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Configurations`  <a name="cfn-elasticmapreduce-cluster-configuration-configurations"></a>
A list of additional configurations to apply within a configuration object\.  
*Required*: No  
*Type*: List of [Configuration](#aws-properties-elasticmapreduce-cluster-configuration)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)