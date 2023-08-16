# AWS::MSK::Configuration<a name="aws-resource-msk-configuration"></a>

Creates a new MSK configuration\. To see an example of how to use this operation, first save the following text to a file and name the file `config-file.txt`\.

```
auto.create.topics.enable = true

zookeeper.connection.timeout.ms = 1000

log.roll.ms = 604800000
```

Now run the following Python 3\.6 script in the folder where you saved `config-file.txt`\. This script uses the properties specified in `config-file.txt` to create a configuration named `SalesClusterConfiguration`\. This configuration can work with Apache Kafka versions 1\.1\.1 and 2\.1\.0\.

```
import boto3

client = boto3.client('kafka')

config_file = open('config-file.txt', 'r')

server_properties = config_file.read()

response = client.create_configuration(
    Name='SalesClusterConfiguration',
    Description='The configuration to use on all sales clusters.',
    KafkaVersions=['1.1.1', '2.1.0'],
    ServerProperties=server_properties
)

print(response)
```

## Syntax<a name="aws-resource-msk-configuration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-msk-configuration-syntax.json"></a>

```
{
  "Type" : "AWS::MSK::Configuration",
  "Properties" : {
      "[Description](#cfn-msk-configuration-description)" : String,
      "[KafkaVersionsList](#cfn-msk-configuration-kafkaversionslist)" : [ String, ... ],
      "[Name](#cfn-msk-configuration-name)" : String,
      "[ServerProperties](#cfn-msk-configuration-serverproperties)" : String
    }
}
```

### YAML<a name="aws-resource-msk-configuration-syntax.yaml"></a>

```
Type: AWS::MSK::Configuration
Properties: 
  [Description](#cfn-msk-configuration-description): String
  [KafkaVersionsList](#cfn-msk-configuration-kafkaversionslist): 
    - String
  [Name](#cfn-msk-configuration-name): String
  [ServerProperties](#cfn-msk-configuration-serverproperties): String
```

## Properties<a name="aws-resource-msk-configuration-properties"></a>

`Description`  <a name="cfn-msk-configuration-description"></a>
The description of the configuration\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KafkaVersionsList`  <a name="cfn-msk-configuration-kafkaversionslist"></a>
Property description not available\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-msk-configuration-name"></a>
The name of the configuration\. Configuration names are strings that match the regex "^\[0\-9A\-Za\-z\]\[0\-9A\-Za\-z\-\]\{0,\}$"\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerProperties`  <a name="cfn-msk-configuration-serverproperties"></a>
Contents of the `server.properties` file\. When using the API, you must ensure that the contents of the file are base64 encoded\. When using the console, the SDK, or the CLI, the contents of `server.properties` can be in plaintext\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-msk-configuration-return-values"></a>

### Ref<a name="aws-resource-msk-configuration-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-msk-configuration-return-values-fn--getatt"></a>

#### <a name="aws-resource-msk-configuration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.