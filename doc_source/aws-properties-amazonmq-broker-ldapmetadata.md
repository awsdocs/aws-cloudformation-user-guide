# AWS::AmazonMQ::Broker LdapMetadata<a name="aws-properties-amazonmq-broker-ldapmetadata"></a>

<a name="aws-properties-amazonmq-broker-ldapmetadata-description"></a>The `LdapMetadata` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::AmazonMQ::Broker](aws-resource-amazonmq-broker.md)\.

## Syntax<a name="aws-properties-amazonmq-broker-ldapmetadata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-broker-ldapmetadata-syntax.json"></a>

```
{
  "[InterBrokerCreds](#cfn-amazonmq-broker-ldapmetadata-interbrokercreds)" : [ InterBrokerCred, ... ],
  "[ServerMetadata](#cfn-amazonmq-broker-ldapmetadata-servermetadata)" : ServerMetadata
}
```

### YAML<a name="aws-properties-amazonmq-broker-ldapmetadata-syntax.yaml"></a>

```
  [InterBrokerCreds](#cfn-amazonmq-broker-ldapmetadata-interbrokercreds): 
    - InterBrokerCred
  [ServerMetadata](#cfn-amazonmq-broker-ldapmetadata-servermetadata): 
    ServerMetadata
```

## Properties<a name="aws-properties-amazonmq-broker-ldapmetadata-properties"></a>

`InterBrokerCreds`  <a name="cfn-amazonmq-broker-ldapmetadata-interbrokercreds"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [InterBrokerCred](aws-properties-amazonmq-broker-interbrokercred.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerMetadata`  <a name="cfn-amazonmq-broker-ldapmetadata-servermetadata"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: [ServerMetadata](aws-properties-amazonmq-broker-servermetadata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)