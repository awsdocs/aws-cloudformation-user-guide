# Amazon EMR InstanceFleetConfig Configuration<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration"></a>

Use the `Configuration` property to configure fleet instances for Amazon EMR and applications and software bundled with Amazon EMR\. For more information, see [Configuring Applications](http://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-configure-apps.html) in the *Amazon EMR Release Guide*\. `Configuration` is a subproperty of the [Amazon EMR InstanceFleetConfig InstanceTypeConfig](aws-properties-elasticmapreduce-instancefleetconfig-instancetypeconfig.md) property\.

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration-syntax.json"></a>

```
"[Classification](#cfn-elasticmapreduce-instancefleetconfig-configuration-classification)" : String,
"[ConfigurationProperties](#cfn-elasticmapreduce-instancefleetconfig-configuration-configurationproperties)" : { String:String, ... },
"[Configurations](#cfn-elasticmapreduce-instancefleetconfig-configuration-configurations)" : [ [*Configuration*](#aws-properties-elasticmapreduce-instancefleetconfig-configuration), ... ]
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration-syntax.yaml"></a>

```
[Classification](#cfn-elasticmapreduce-instancefleetconfig-configuration-classification): String
[ConfigurationProperties](#cfn-elasticmapreduce-instancefleetconfig-configuration-configurationproperties): 
  String: String
[Configurations](#cfn-elasticmapreduce-instancefleetconfig-configuration-configurations): 
  - [*Configuration*](#aws-properties-elasticmapreduce-instancefleetconfig-configuration)
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-configuration-properties"></a>

`Classification`  <a name="cfn-elasticmapreduce-instancefleetconfig-configuration-classification"></a>
The application\-specific configuration file\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ConfigurationProperties`  <a name="cfn-elasticmapreduce-instancefleetconfig-configuration-configurationproperties"></a>
Within a configuration classification, a set of properties that represent the settings that you want to change in the configuration file\. Duplicates not allowed\.  
*Required*: No  
*Type*: String to String map  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Configurations`  <a name="cfn-elasticmapreduce-instancefleetconfig-configuration-configurations"></a>
The list of additional configurations to apply within a configuration object\. Duplicates not allowed\.  
*Required*: No  
*Type*: List of [Amazon EMR InstanceFleetConfig Configuration](#aws-properties-elasticmapreduce-instancefleetconfig-configuration)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)