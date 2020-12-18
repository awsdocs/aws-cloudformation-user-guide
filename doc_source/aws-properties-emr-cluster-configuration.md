# AWS::EMR::InstanceGroupConfig Configuration<a name="aws-properties-emr-cluster-configuration"></a>

`Configurations` is a property of the `AWS::EMR::Cluster` resource that specifies the configuration of applications on an Amazon EMR cluster\.

Configurations are optional\. You can use them to have EMR customize applications and software bundled with Amazon EMR when a cluster is created\. A configuration consists of a classification, properties, and optional nested configurations\. A classification refers to an application\-specific configuration file\. Properties are the settings you want to change in that file\. For more information, see [Configuring Applications](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-configure-apps.html)\.

**Note**  
Applies only to Amazon EMR releases 4\.0 and later\.

## Syntax<a name="aws-properties-emr-cluster-configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emr-cluster-configuration-syntax.json"></a>

```
{
  "[Classification](#cfn-emr-cluster-configuration-classification)" : String,
  "[ConfigurationProperties](#cfn-emr-cluster-configuration-configurationproperties)" : {Key : Value, ...},
  "[Configurations](#cfn-emr-cluster-configuration-configurations)" : [ Configuration, ... ]
}
```

### YAML<a name="aws-properties-emr-cluster-configuration-syntax.yaml"></a>

```
  [Classification](#cfn-emr-cluster-configuration-classification): String
  [ConfigurationProperties](#cfn-emr-cluster-configuration-configurationproperties): 
    Key : Value
  [Configurations](#cfn-emr-cluster-configuration-configurations): 
    - Configuration
```

## Properties<a name="aws-properties-emr-cluster-configuration-properties"></a>

`Classification`  <a name="cfn-emr-cluster-configuration-classification"></a>
The classification within a configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationProperties`  <a name="cfn-emr-cluster-configuration-configurationproperties"></a>
Within a configuration classification, a set of properties that represent the settings that you want to change in the configuration file\. Duplicates not allowed\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Configurations`  <a name="cfn-emr-cluster-configuration-configurations"></a>
A list of additional configurations to apply within a configuration object\.  
*Required*: No  
*Type*: List of [Configuration](#aws-properties-emr-cluster-configuration)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)