# Amazon EMR Cluster BootstrapActionConfig<a name="aws-properties-emr-cluster-bootstrapactionconfig"></a>

`BootstrapActionConfig` is a property of the [AWS::EMR::Cluster](aws-resource-emr-cluster.md) resource that specifies bootstrap actions that Amazon EMR \(Amazon EMR\) runs before it installs applications on the cluster nodes\.

## Syntax<a name="w3ab2c21c14e1067b5"></a>

### JSON<a name="aws-properties-emr-cluster-bootstrapactionconfig-syntax.json"></a>

```
{
  "[Name](#cfn-emr-cluster-bootstrapactionconfig-name)" : String,
  "[ScriptBootstrapAction](#cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction)" : ScriptBootstrapAction
}
```

### YAML<a name="aws-properties-emr-cluster-bootstrapactionconfig-syntax.yaml"></a>

```
[Name](#cfn-emr-cluster-bootstrapactionconfig-name): String
[ScriptBootstrapAction](#cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction): ScriptBootstrapAction
```

## Properties<a name="w3ab2c21c14e1067b7"></a>

`Name`  <a name="cfn-emr-cluster-bootstrapactionconfig-name"></a>
The name of the bootstrap action to add to your cluster\.  
*Required*: Yes  
*Type*: String

`ScriptBootstrapAction`  <a name="cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction"></a>
The script that the bootstrap action runs\.  
*Required*: Yes  
*Type*: [Amazon EMR Cluster ScriptBootstrapActionConfig](aws-properties-emr-cluster-bootstrapactionconfig-scriptbootstrapactionconfig.md)