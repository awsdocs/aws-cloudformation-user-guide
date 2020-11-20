# AWS::AmazonMQ::ConfigurationAssociation<a name="aws-resource-amazonmq-configurationassociation"></a>

Use the AWS CloudFormation `AWS::AmazonMQ::ConfigurationAssociation` resource to associate a configuration with a broker, or return information about the specified ConfigurationAssociation\. Only use one per broker, and don't use a configuration on the broker resource if you have associated a configuration with that broker\.

**Note**  
Does not apply to RabbitMQ brokers\.

## Syntax<a name="aws-resource-amazonmq-configurationassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-amazonmq-configurationassociation-syntax.json"></a>

```
{
  "Type" : "AWS::AmazonMQ::ConfigurationAssociation",
  "Properties" : {
      "[Broker](#cfn-amazonmq-configurationassociation-broker)" : String,
      "[Configuration](#cfn-amazonmq-configurationassociation-configuration)" : ConfigurationId
    }
}
```

### YAML<a name="aws-resource-amazonmq-configurationassociation-syntax.yaml"></a>

```
Type: AWS::AmazonMQ::ConfigurationAssociation
Properties: 
  [Broker](#cfn-amazonmq-configurationassociation-broker): String
  [Configuration](#cfn-amazonmq-configurationassociation-configuration): 
    ConfigurationId
```

## Properties<a name="aws-resource-amazonmq-configurationassociation-properties"></a>

`Broker`  <a name="cfn-amazonmq-configurationassociation-broker"></a>
The broker to associate with a configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Configuration`  <a name="cfn-amazonmq-configurationassociation-configuration"></a>
The configuration to associate with a broker\.  
*Required*: Yes  
*Type*: [ConfigurationId](aws-properties-amazonmq-configurationassociation-configurationid.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-amazonmq-configurationassociation-return-values"></a>

### Ref<a name="aws-resource-amazonmq-configurationassociation-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon MQ configurationassociation ID\. For example: 

 `c-1234a5b6-78cd-901e-2fgh-3i45j6k178l9` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-amazonmq-configurationassociation--examples"></a>

### ConfigurationAssociation<a name="aws-resource-amazonmq-configurationassociation--examples--ConfigurationAssociation"></a>

The following example creates an Amazon MQ ActiveMQ ConfigurationAssociation\.

#### JSON<a name="aws-resource-amazonmq-configurationassociation--examples--ConfigurationAssociation--json"></a>

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

#### YAML<a name="aws-resource-amazonmq-configurationassociation--examples--ConfigurationAssociation--yaml"></a>

```
 ConfigurationAssociation1:
    Type: AWS::AmazonMQ::ConfigurationAssociation
    Properties:
      Broker: {Ref: Broker1}
      Configuration:
        Id: {Ref: Configuration1}
        Revision: {'Fn::GetAtt': [Configuration1, Revision]}
```