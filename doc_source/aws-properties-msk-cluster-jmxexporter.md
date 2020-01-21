# AWS::MSK::Cluster JmxExporter<a name="aws-properties-msk-cluster-jmxexporter"></a>

Indicates whether you want to enable or disable the JMX Exporter\.

## Syntax<a name="aws-properties-msk-cluster-jmxexporter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-jmxexporter-syntax.json"></a>

```
{
  "[EnabledInBroker](#cfn-msk-cluster-jmxexporter-enabledinbroker)" : Boolean
}
```

### YAML<a name="aws-properties-msk-cluster-jmxexporter-syntax.yaml"></a>

```
  [EnabledInBroker](#cfn-msk-cluster-jmxexporter-enabledinbroker): Boolean
```

## Properties<a name="aws-properties-msk-cluster-jmxexporter-properties"></a>

`EnabledInBroker`  <a name="cfn-msk-cluster-jmxexporter-enabledinbroker"></a>
Indicates whether you want to enable or disable the JMX Exporter\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)