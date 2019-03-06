# ConfigurationAssociation ConfigurationId<a name="aws-properties-amazonmq-configurationassociation-configurationid"></a>

<a name="aws-properties-amazonmq-configurationassociation-configurationid-description"></a>The `ConfigurationId` property type specifies a configuration Id and the revision of a configuration\.

<a name="aws-properties-amazonmq-configurationassociation-configurationid-inheritance"></a> `ConfigurationId` is a property of the [AWS::AmazonMQ::ConfigurationAssociation](aws-resource-amazonmq-configurationassociation.md) resource type\.

## Syntax<a name="aws-properties-amazonmq-configurationassociation-configurationid-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-configurationassociation-configurationid-syntax.json"></a>

```
{
  "[Id](#cfn-amazonmq-configurationassociation-configurationid-id)" : String,
  "[Revision](#cfn-amazonmq-configurationassociation-configurationid-revision)" : Integer
}
```

### YAML<a name="aws-properties-amazonmq-configurationassociation-configurationid-syntax.yaml"></a>

```
[Id](#cfn-amazonmq-configurationassociation-configurationid-id): String
[Revision](#cfn-amazonmq-configurationassociation-configurationid-revision): Integer
```

## Properties<a name="aws-properties-amazonmq-configurationassociation-configurationid-properties"></a>

`Id`  <a name="cfn-amazonmq-configurationassociation-configurationid-id"></a>
The Id of the configuration\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Revision`  <a name="cfn-amazonmq-configurationassociation-configurationid-revision"></a>
The revision number of the configuration\.  
 *Required*: Yes  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-amazonmq-configurationassociation-configurationid-seealso"></a>
+ [Broker Architecture](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/amazon-mq-broker-architecture.html) in the *Amazon MQ Developer Guide*