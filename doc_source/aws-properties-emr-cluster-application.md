# Amazon EMR Cluster Application<a name="aws-properties-emr-cluster-application"></a>

`Application` is a property of the [AWS::EMR::Cluster](aws-resource-emr-cluster.md) resource that adds an Amazon EMR \(Amazon EMR\) application bundle or third\-party software to an Amazon EMR cluster\.

## Syntax<a name="w3ab2c21c14e1059b5"></a>

### JSON<a name="aws-properties-emr-cluster-application-syntax.json"></a>

```
{
  "[AdditionalInfo](#cfn-emr-cluster-application-additionalinfo)" : { String:String, ... },
  "[Args](#cfn-emr-cluster-application-args)" : [ String, ... ],
  "[Name](#cfn-emr-cluster-application-name)" : String,
  "[Version](#cfn-emr-cluster-application-version)" : String
}
```

### YAML<a name="aws-properties-emr-cluster-application-syntax.yaml"></a>

```
[AdditionalInfo](#cfn-emr-cluster-application-additionalinfo):
  String: String
[Args](#cfn-emr-cluster-application-args):
  - String
[Name](#cfn-emr-cluster-application-name): String
[Version](#cfn-emr-cluster-application-version): String
```

## Properties<a name="w3ab2c21c14e1059b7"></a>

`AdditionalInfo`  <a name="cfn-emr-cluster-application-additionalinfo"></a>
Metadata about third\-party applications that third\-party vendors use for testing purposes\.  
*Required*: No  
*Type*: String\-to\-string map

`Args`  <a name="cfn-emr-cluster-application-args"></a>
Arguments that Amazon EMR passes to the application\.  
*Required*: No  
*Type*: List of String values

`Name`  <a name="cfn-emr-cluster-application-name"></a>
The name of the application to add to your cluster, such as `Hadoop` or `Hive`\. For valid values, see the [Applications](http://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_RunJobFlow.html) parameter in the *Amazon EMR API Reference*\.  
*Required*: No  
*Type*: String

`Version`  <a name="cfn-emr-cluster-application-version"></a>
The version of the application\.  
*Required*: No  
*Type*: String