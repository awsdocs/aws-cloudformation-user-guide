# Amazon MQ Broker ConfigurationId<a name="aws-properties-amazonmq-broker-configurationid"></a>

<a name="aws-properties-amazonmq-broker-configurationid-description"></a>The `ConfigurationId` property type specifies the unique ID that Amazon MQ generates for the configuration\.

<a name="aws-properties-amazonmq-broker-configurationid-inheritance"></a> `ConfigurationId` is a property of the `[AWS::AmazonMQ::Broker](aws-resource-amazonmq-broker.md)` resource\.

## Syntax<a name="aws-properties-amazonmq-broker-configurationid-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-broker-configurationid-syntax.json"></a>

```
{
  "[Id](#cfn-amazonmq-broker-configurationid-id)" : String,
  "[Revision](#cfn-amazonmq-broker-configurationid-revision)" : Integer  
}
```

### YAML<a name="aws-properties-amazonmq-broker-configurationid-syntax.yaml"></a>

```
[Id](#cfn-amazonmq-broker-configurationid-id): String
[Revision](#cfn-amazonmq-broker-configurationid-revision): Integer
```

## Properties<a name="aws-properties-amazonmq-broker-configurationid-properties"></a>

`Id`  <a name="cfn-amazonmq-broker-configurationid-id"></a>
The unique ID that Amazon MQ generates for the configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`Revision`  <a name="cfn-amazonmq-broker-configurationid-revision"></a>
The revision number of the configuration\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)