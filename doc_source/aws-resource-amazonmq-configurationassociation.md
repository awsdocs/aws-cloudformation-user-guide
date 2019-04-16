# AWS::AmazonMQ::ConfigurationAssociation<a name="aws-resource-amazonmq-configurationassociation"></a>

Use the AWS CloudFormation `AWS::AmazonMQ::ConfigurationAssociation` resource to associate a Configuration with a Broker, or return information about the specified configurationassociation\. Only use one per broker, and don't use a configuration on the broker resource if you have associated a configuration with that broker\. 

## Syntax<a name="aws-resource-amazonmq-configurationassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-amazonmq-configurationassociation-syntax.json"></a>

```
{
  "Type" : "AWS::AmazonMQ::ConfigurationAssociation",
  "Properties" : {
    "[Broker](#cfn-amazonmq-configurationassociation-broker)" : String,
    "[Configuration](#cfn-amazonmq-configurationassociation-configuration)" : [*ConfigurationId*](aws-properties-amazonmq-configurationassociation-configurationid.md)
  }
}
```

### YAML<a name="aws-resource-amazonmq-configurationassociation-syntax.yaml"></a>

```
Type: "AWS::AmazonMQ::ConfigurationAssociation"
Properties:
  [Broker](#cfn-amazonmq-configurationassociation-broker): String
  [Configuration](#cfn-amazonmq-configurationassociation-configuration): 
    [*ConfigurationId*](aws-properties-amazonmq-configurationassociation-configurationid.md)
```

## Properties<a name="aws-resource-amazonmq-configurationassociation-properties"></a>

`Broker`  <a name="cfn-amazonmq-configurationassociation-broker"></a>
The broker to associate with a configuration\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Configuration`  <a name="cfn-amazonmq-configurationassociation-configuration"></a>
The configuration to associate with a broker\.  
 *Required*: Yes  
 *Type*: [ConfigurationId](aws-properties-amazonmq-configurationassociation-configurationid.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-amazonmq-configurationassociation-returnvalues"></a>

### Ref<a name="aws-resource-amazonmq-configurationassociation-ref"></a>

When you pass the logical ID of an `AWS::AmazonMQ::ConfigurationAssociation` resource to the intrinsic `Ref` function, the function returns the Amazon MQ configurationassociation ID\. For example: 

```
c-1234a5b6-78cd-901e-2fgh-3i45j6k178l9
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-amazonmq-configurationassociation-examples"></a>

### ConfigurationAssociation<a name="aws-resource-amazonmq-configurationassociation-example1"></a>

The following example creates an Amazon MQ `ConfigurationAssociation`\.

#### JSON<a name="aws-resource-amazonmq-configurationassociation-example1.json"></a>

```
"ConfigurationAssociation1": {
		"Type": "AWS::AmazonMQ::ConfigurationAssociation",
		"Properties": {
			"Broker": {
				"Ref": "Broker1"
			},
			"Configuration": {
				"Id": {
					"Ref": "Configuration1"
				},
				"Revision": {
					"Fn::GetAtt": [
						"Configuration1",
						"Revision"
					]
				}
			}
		}
	}
```

#### YAML<a name="aws-resource-amazonmq-configurationassociation-example1.yaml"></a>

```
 ConfigurationAssociation1:
    Type: AWS::AmazonMQ::ConfigurationAssociation
    Properties:
      Broker: {Ref: Broker1}
      Configuration:
        Id: {Ref: Configuration1}
        Revision: {'Fn::GetAtt': [Configuration1, Revision]}
```

## See Also<a name="aws-resource-amazonmq-configurationassociation-seealso"></a>
+  [Broker Architecture](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/amazon-mq-broker-architecture.html) in the *Amazon MQ Developer Guide* 