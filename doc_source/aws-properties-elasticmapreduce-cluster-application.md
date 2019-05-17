# AWS::EMR::Cluster Application<a name="aws-properties-elasticmapreduce-cluster-application"></a>

`Application` is a property of `AWS::EMR::Cluster`\. The `Application` property type defines the open\-source big data applications for EMR to install and configure when a cluster is created\.

With Amazon EMR release version 4\.0 and later, the only accepted parameter is the application `Name`\. To pass arguments to these applications, you use configuration classifications specified using JSON objects in a `Configuration` property\. For more information, see [Configuring Applications](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-configure-apps.html)\.

With earlier Amazon EMR releases, the application is any Amazon or third\-party software that you can add to the cluster\. You can specify the version of the application and arguments to pass to it\. Amazon EMR accepts and forwards the argument list to the corresponding installation script as a bootstrap action argument\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-application-syntax.json"></a>

```
{
  "[AdditionalInfo](#cfn-elasticmapreduce-cluster-application-additionalinfo)" : {Key : Value, ...},
  "[Args](#cfn-elasticmapreduce-cluster-application-args)" : [ String, ... ],
  "[Name](#cfn-elasticmapreduce-cluster-application-name)" : String,
  "[Version](#cfn-elasticmapreduce-cluster-application-version)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-application-syntax.yaml"></a>

```
  [AdditionalInfo](#cfn-elasticmapreduce-cluster-application-additionalinfo): 
    Key : Value
  [Args](#cfn-elasticmapreduce-cluster-application-args): 
    - String
  [Name](#cfn-elasticmapreduce-cluster-application-name): String
  [Version](#cfn-elasticmapreduce-cluster-application-version): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-application-properties"></a>

`AdditionalInfo`  <a name="cfn-elasticmapreduce-cluster-application-additionalinfo"></a>
This option is for advanced users only\. This is meta information about clusters and applications that are used for testing and troubleshooting\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Args`  <a name="cfn-elasticmapreduce-cluster-application-args"></a>
Arguments for Amazon EMR to pass to the application\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-elasticmapreduce-cluster-application-name"></a>
The name of the application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-elasticmapreduce-cluster-application-version"></a>
The version of the application\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)