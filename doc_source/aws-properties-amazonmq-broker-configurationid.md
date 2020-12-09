# AWS::AmazonMQ::Broker ConfigurationId<a name="aws-properties-amazonmq-broker-configurationid"></a>

A list of information about the configuration\.

**Important**  
Does not apply to RabbitMQ brokers\.

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
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Revision`  <a name="cfn-amazonmq-broker-configurationid-revision"></a>
The revision number of the configuration\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)