# AWS::AmazonMQ::Configuration<a name="aws-resource-amazonmq-configuration"></a>

A *configuration* contains all of the settings for your ActiveMQ broker, in XML format\.

The `AWS::AmazonMQ::Configuration` resource lets you create Amazon MQ configurations, add configuration changes or modify users, and return information about the specified configuration\. For more information, see [Configuration](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/configuration.html) and [Amazon MQ Broker Configuration Parameters](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/amazon-mq-broker-configuration-parameters.html) in the *Amazon MQ Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-amazonmq-configuration-syntax)
+ [Properties](#aws-resource-amazonmq-configuration-properties)
+ [Return Values](#aws-resource-amazonmq-configuration-returnvalues)
+ [Examples](#aws-resource-amazonmq-configuration-examples)

## Syntax<a name="aws-resource-amazonmq-configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-amazonmq-configuration-syntax.json"></a>

```
{
  "Type" : "AWS::AmazonMQ::Configuration",
  "Properties" : {
    "[Data](#cfn-amazonmq-configuration-data)" : String,
    "[Description](#cfn-amazonmq-configuration-description)" : String,
    "[EngineType](#cfn-amazonmq-configuration-enginetype)" : String,
    "[EngineVersion](#cfn-amazonmq-configuration-engineversion)" : String,
    "[Name](#cfn-amazonmq-configuration-name)" : String
  }
}
```

### YAML<a name="aws-resource-amazonmq-configuration-syntax.yaml"></a>

```
Type: "AWS::AmazonMQ::Configuration"
Properties:
  [Data](#cfn-amazonmq-configuration-data): String
  [Description](#cfn-amazonmq-configuration-description): String
  [EngineType](#cfn-amazonmq-configuration-enginetype): String
  [EngineVersion](#cfn-amazonmq-configuration-engineversion): String
  [Name](#cfn-amazonmq-configuration-name): String
```

## Properties<a name="aws-resource-amazonmq-configuration-properties"></a>

`Data`  <a name="cfn-amazonmq-configuration-data"></a>
The base64\-encoded XML configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Description`  <a name="cfn-amazonmq-configuration-description"></a>
The description of the configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`EngineType`  <a name="cfn-amazonmq-configuration-enginetype"></a>
The type of broker engine\.  
Currently, Amazon MQ supports only `ACTIVEMQ`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`EngineVersion`  <a name="cfn-amazonmq-configuration-engineversion"></a>
The version of the broker engine\.  
For a list of supported engine versions, see: [Broker Engine](https://docs.aws.amazon.com/amazon-mq/latest/developer-guide/broker-engine.html)\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-amazonmq-configuration-name"></a>
The name of the configuration\. This value can contain only alphanumeric characters, dashes, periods, underscores, and tildes \(`- . _ ~`\)\. This value must be 1\-150 characters long\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-amazonmq-configuration-returnvalues"></a>

### Ref<a name="aws-resource-amazonmq-configuration-ref"></a>

When you pass the logical ID of an `AWS::AmazonMQ::Configuration` resource to the intrinsic `Ref` function, the function returns the Amazon MQ configuration ID\. For example: 

```
c-1234a5b6-78cd-901e-2fgh-3i45j6k178l9
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-amazonmq-configuration-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the Amazon MQ configuration\.   

```
arn:aws:mq:us-east-2:123456789012:configuration:MyConfigurationDevelopment:c-1234a5b6-78cd-901e-2fgh-3i45j6k178l9
```

`Revision`  
The revision number of the configuration\.  

```
1
```

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-amazonmq-configuration-examples"></a>

### Amazon MQ Configuration<a name="aws-resource-amazonmq-configuration-example1"></a>

The following example creates an Amazon MQ configuration in XML format\.

#### JSON<a name="aws-resource-amazonmq-configuration-example1.json"></a>

```
{
  "Description": "Create an Amazon MQ configuration",
    "Configuration1": {
      "Type": "AWS::AmazonMQ::Configuration",
      "Properties": {
        "Data": {
          "Fn::Base64": "<?xml version=\"1.0\" encoding=\"UTF-8\" standalone=\"yes\"?>\n<broker xmlns=\"http://activemq.apache.org/schema/core\" start=\"false\">\n  <destinationPolicy>\n    <policyMap>\n      <policyEntries>\n        <policyEntry topic=\">\">\n          <pendingMessageLimitStrategy>\n            <constantPendingMessageLimitStrategy limit=\"3000\"/>\n          </pendingMessageLimitStrategy>\n        </policyEntry>\n      </policyEntries>\n    </policyMap>\n  </destinationPolicy>\n  <plugins>\n  </plugins>\n</broker>\n"
        },
        "EngineType": "ACTIVEMQ",
        "EngineVersion": "5.15.0",
        "Name": "my-configuration-1"
      }
   }
}
```

#### YAML<a name="aws-resource-amazonmq-configuration-example1.yaml"></a>

```
--- 
Description: "Create an Amazon MQ configuration"
Resources: 
  Configuration: 
    Type: "AWS::AmazonMQ::Configuration"
    Properties: 
      Data: 
        ? "Fn::Base64"
        : |
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <broker xmlns="http://activemq.apache.org/schema/core" start="false">
              <destinationPolicy>
                <policyMap>
                  <policyEntries>
                    <policyEntry topic=">">
                      <pendingMessageLimitStrategy>
                        <constantPendingMessageLimitStrategy limit="3000"/>
                      </pendingMessageLimitStrategy>
                    </policyEntry>
                  </policyEntries>
                </policyMap>
              </destinationPolicy>
              <plugins>
              </plugins>
            </broker>
      EngineType: ACTIVEMQ
      EngineVersion: "5.15.0"
      Name: my-configuration-1
```