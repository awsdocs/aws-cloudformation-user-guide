# AWS::AmazonMQ::Configuration<a name="aws-resource-amazonmq-configuration"></a>

Creates a new configuration for the specified configuration name\. Amazon MQ uses the default configuration \(the engine type and version\)\.

**Note**  
Does not apply to RabbitMQ brokers\.

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
      "[Name](#cfn-amazonmq-configuration-name)" : String,
      "[Tags](#cfn-amazonmq-configuration-tags)" : [ TagsEntry, ... ]
    }
}
```

### YAML<a name="aws-resource-amazonmq-configuration-syntax.yaml"></a>

```
Type: AWS::AmazonMQ::Configuration
Properties: 
  [Data](#cfn-amazonmq-configuration-data): String
  [Description](#cfn-amazonmq-configuration-description): String
  [EngineType](#cfn-amazonmq-configuration-enginetype): String
  [EngineVersion](#cfn-amazonmq-configuration-engineversion): String
  [Name](#cfn-amazonmq-configuration-name): String
  [Tags](#cfn-amazonmq-configuration-tags): 
    - TagsEntry
```

## Properties<a name="aws-resource-amazonmq-configuration-properties"></a>

`Data`  <a name="cfn-amazonmq-configuration-data"></a>
The base64\-encoded XML configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-amazonmq-configuration-description"></a>
The description of the configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineType`  <a name="cfn-amazonmq-configuration-enginetype"></a>
The type of broker engine\. Note: Currently, Amazon MQ only supports ACTIVEMQ for creating and editing broker configurations\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineVersion`  <a name="cfn-amazonmq-configuration-engineversion"></a>
The version of the broker engine\. For a list of supported engine versions, see https://docs\.aws\.amazon\.com/amazon\-mq/latest/developer\-guide/broker\-engine\.html  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-amazonmq-configuration-name"></a>
The name of the configuration\. This value can contain only alphanumeric characters, dashes, periods, underscores, and tildes \(\- \. \_ \~\)\. This value must be 1\-150 characters long\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-amazonmq-configuration-tags"></a>
Create tags when creating the configuration\.  
*Required*: No  
*Type*: List of [TagsEntry](aws-properties-amazonmq-configuration-tagsentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-amazonmq-configuration-return-values"></a>

### Ref<a name="aws-resource-amazonmq-configuration-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon MQ configuration ID\. For example: 

 `c-1234a5b6-78cd-901e-2fgh-3i45j6k178l9` 

### Fn::GetAtt<a name="aws-resource-amazonmq-configuration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-amazonmq-configuration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the Amazon MQ configuration\.  
 `arn:aws:mq:us-east-2:123456789012:configuration:MyConfigurationDevelopment:c-1234a5b6-78cd-901e-2fgh-3i45j6k178l9` 

`Id`  <a name="Id-fn::getatt"></a>
The ID of the Amazon MQ configuration\.  
 `c-1234a5b6-78cd-901e-2fgh-3i45j6k178l9` 

`Revision`  <a name="Revision-fn::getatt"></a>
The revision number of the configuration\.  
 `1` 

## Examples<a name="aws-resource-amazonmq-configuration--examples"></a>

### Amazon MQ Configuration<a name="aws-resource-amazonmq-configuration--examples--Amazon_MQ_Configuration"></a>

#### JSON<a name="aws-resource-amazonmq-configuration--examples--Amazon_MQ_Configuration--json"></a>

```
{
  "Description": "Create an Amazon MQ ActiveMQ configuration",
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

#### YAML<a name="aws-resource-amazonmq-configuration--examples--Amazon_MQ_Configuration--yaml"></a>

```
--- 
Description: "Create an Amazon MQ ActiveMQ configuration"
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