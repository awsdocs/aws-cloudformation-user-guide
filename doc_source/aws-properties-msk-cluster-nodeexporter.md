# AWS::MSK::Cluster NodeExporter<a name="aws-properties-msk-cluster-nodeexporter"></a>

Indicates whether you want to enable or disable the Node Exporter\.

## Syntax<a name="aws-properties-msk-cluster-nodeexporter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-nodeexporter-syntax.json"></a>

```
{
  "[EnabledInBroker](#cfn-msk-cluster-nodeexporter-enabledinbroker)" : Boolean
}
```

### YAML<a name="aws-properties-msk-cluster-nodeexporter-syntax.yaml"></a>

```
  [EnabledInBroker](#cfn-msk-cluster-nodeexporter-enabledinbroker): Boolean
```

## Properties<a name="aws-properties-msk-cluster-nodeexporter-properties"></a>

`EnabledInBroker`  <a name="cfn-msk-cluster-nodeexporter-enabledinbroker"></a>
Indicates whether you want to enable or disable the Node Exporter\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)