# Amazon EMR Cluster BootstrapActionConfig<a name="aws-properties-emr-cluster-bootstrapactionconfig"></a>

`BootstrapActionConfig` is a property of the [AWS::EMR::Cluster](aws-resource-emr-cluster.md) resource that specifies bootstrap actions that Amazon EMR \(Amazon EMR\) runs before it installs applications on the cluster nodes\.

## Syntax<a name="w3ab2c21c14d876b5"></a>

### JSON<a name="aws-properties-emr-cluster-bootstrapactionconfig-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-bootstrapactionconfig-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction)" : ScriptBootstrapAction
}
```

### YAML<a name="aws-properties-emr-cluster-bootstrapactionconfig-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-bootstrapactionconfig-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-emr-cluster-bootstrapactionconfig-scriptbootstrapaction): ScriptBootstrapAction
```

## Properties<a name="w3ab2c21c14d876b7"></a>

`Name`  
The name of the bootstrap action to add to your cluster\.  
*Required: *Yes  
*Type*: String

`ScriptBootstrapAction`  
The script that the bootstrap action runs\.  
*Required: *Yes  
*Type*: [Amazon EMR Cluster ScriptBootstrapActionConfig](aws-properties-emr-cluster-bootstrapactionconfig-scriptbootstrapactionconfig.md)