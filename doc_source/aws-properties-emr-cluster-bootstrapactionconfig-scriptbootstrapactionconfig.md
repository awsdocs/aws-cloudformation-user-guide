# Amazon EMR Cluster ScriptBootstrapActionConfig<a name="aws-properties-emr-cluster-bootstrapactionconfig-scriptbootstrapactionconfig"></a>

`ScriptBootstrapActionConfig` is a property of the [Amazon EMR Cluster BootstrapActionConfig](aws-properties-emr-cluster-bootstrapactionconfig.md) property that specifies the arguments and location of the bootstrap script that Amazon EMR \(Amazon EMR\) runs before it installs applications on the cluster nodes\.

## Syntax<a name="w3ab2c21c14e1131b5"></a>

### JSON<a name="aws-properties-emr-cluster-bootstrapactionconfig-scriptbootstrapactionconfig-syntax.json"></a>

```
{
  "[Args](#cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction-args)" : [ String, ... ],
  "[Path](#cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction-path)" : String
}
```

### YAML<a name="aws-properties-emr-cluster-bootstrapactionconfig-scriptbootstrapactionconfig-syntax.yaml"></a>

```
[Args](#cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction-args):
  - String
[Path](#cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction-path): String
```

## Properties<a name="w3ab2c21c14e1131b7"></a>

`Args`  <a name="cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction-args"></a>
A list of command line arguments to pass to the bootstrap action script\.  
*Required*: No  
*Type*: List of String values

`Path`  <a name="cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction-path"></a>
The location of the script that Amazon EMR runs during a bootstrap action\. Specify a location in an S3 bucket or your local file system\.  
*Required*: Yes  
*Type*: String