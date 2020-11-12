# AWS::AmazonMQ::Broker LogList<a name="aws-properties-amazonmq-broker-loglist"></a>

The list of information about logs to be enabled for the specified broker\.

## Syntax<a name="aws-properties-amazonmq-broker-loglist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-broker-loglist-syntax.json"></a>

```
{
  "[Audit](#cfn-amazonmq-broker-loglist-audit)" : Boolean,
  "[General](#cfn-amazonmq-broker-loglist-general)" : Boolean
}
```

### YAML<a name="aws-properties-amazonmq-broker-loglist-syntax.yaml"></a>

```
  [Audit](#cfn-amazonmq-broker-loglist-audit): Boolean
  [General](#cfn-amazonmq-broker-loglist-general): Boolean
```

## Properties<a name="aws-properties-amazonmq-broker-loglist-properties"></a>

`Audit`  <a name="cfn-amazonmq-broker-loglist-audit"></a>
Enables audit logging\. Every user management action made using JMX or the ActiveMQ Web Console is logged\. Does not apply to RabbitMQ brokers\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`General`  <a name="cfn-amazonmq-broker-loglist-general"></a>
Enables general logging\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)