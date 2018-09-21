# Amazon MQ Broker LogsConfiguration<a name="aws-properties-amazonmq-broker-logsconfiguration"></a>

<a name="aws-properties-amazonmq-broker-logsconfiguration-description"></a>The `LogsConfiguration` property type enables general or audit logging for an Amazon MQ broker\.

<a name="aws-properties-amazonmq-broker-logsconfiguration-inheritance"></a> `LogsConfiguration` is a property of the `[AWS::AmazonMQ::Broker](aws-resource-amazonmq-broker.md)` resource\.

## Syntax<a name="aws-properties-amazonmq-broker-logsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-broker-logsconfiguration-syntax.json"></a>

```
{
  "[Audit](#cfn-amazonmq-broker-logsconfiguration-id)" : Boolean,
  "[General](#cfn-amazonmq-broker-logsconfiguration-revision)" : Boolean  
}
```

### YAML<a name="aws-properties-amazonmq-broker-logsconfiguration-syntax.yaml"></a>

```
[Audit](#cfn-amazonmq-broker-logsconfiguration-id): Boolean
[General](#cfn-amazonmq-broker-logsconfiguration-revision): Boolean
```

## Properties<a name="aws-properties-amazonmq-broker-logsconfiguration-properties"></a>

`Audit`  <a name="cfn-amazonmq-broker-logsconfiguration-id"></a>
Enables audit logging\. Every user management action made using JMS or the [ActiveMQ Web Console](http://activemq.apache.org/web-console.html) is logged\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`General`  <a name="cfn-amazonmq-broker-logsconfiguration-revision"></a>
Enables general logging\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)