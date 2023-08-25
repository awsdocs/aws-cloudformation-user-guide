# AWS::MSK::Cluster<a name="aws-resource-msk-cluster"></a>

Creates a new MSK cluster\. The following Python 3\.6 examples shows how you can create a cluster that's distributed over two Availability Zones\. Before you run this Python script, replace the example subnet and security\-group IDs with the IDs of your subnets and security group\. When you create an MSK cluster, its brokers get evenly distributed over a number of Availability Zones that's equal to the number of subnets that you specify in the `BrokerNodeGroupInfo` parameter\. In this example, you can add a third subnet to get a cluster that's distributed over three Availability Zones\.

```
import boto3

client = boto3.client('kafka')

response = client.create_cluster(
    BrokerNodeGroupInfo={
        'BrokerAZDistribution': 'DEFAULT',
        'ClientSubnets': [
            'subnet-012345678901fedcba',
            'subnet-9876543210abcdef01'
        ],
        'InstanceType': 'kafka.m5.large',
        'SecurityGroups': [
            'sg-012345abcdef789789'
        ]
    },
    ClusterName='SalesCluster',
    EncryptionInfo={
        'EncryptionInTransit': {
            'ClientBroker': 'TLS_PLAINTEXT',
            'InCluster': True
        }
    },
    EnhancedMonitoring='PER_TOPIC_PER_BROKER',
    KafkaVersion='2.2.1',
    NumberOfBrokerNodes=2
)

print(response)
```

## Syntax<a name="aws-resource-msk-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-msk-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::MSK::Cluster",
  "Properties" : {
      "[BrokerNodeGroupInfo](#cfn-msk-cluster-brokernodegroupinfo)" : BrokerNodeGroupInfo,
      "[ClientAuthentication](#cfn-msk-cluster-clientauthentication)" : ClientAuthentication,
      "[ClusterName](#cfn-msk-cluster-clustername)" : String,
      "[ConfigurationInfo](#cfn-msk-cluster-configurationinfo)" : ConfigurationInfo,
      "[CurrentVersion](#cfn-msk-cluster-currentversion)" : String,
      "[EncryptionInfo](#cfn-msk-cluster-encryptioninfo)" : EncryptionInfo,
      "[EnhancedMonitoring](#cfn-msk-cluster-enhancedmonitoring)" : String,
      "[KafkaVersion](#cfn-msk-cluster-kafkaversion)" : String,
      "[LoggingInfo](#cfn-msk-cluster-logginginfo)" : LoggingInfo,
      "[NumberOfBrokerNodes](#cfn-msk-cluster-numberofbrokernodes)" : Integer,
      "[OpenMonitoring](#cfn-msk-cluster-openmonitoring)" : OpenMonitoring,
      "[StorageMode](#cfn-msk-cluster-storagemode)" : String,
      "[Tags](#cfn-msk-cluster-tags)" : {Key: Value, ...}
    }
}
```

### YAML<a name="aws-resource-msk-cluster-syntax.yaml"></a>

```
Type: AWS::MSK::Cluster
Properties: 
  [BrokerNodeGroupInfo](#cfn-msk-cluster-brokernodegroupinfo): 
    BrokerNodeGroupInfo
  [ClientAuthentication](#cfn-msk-cluster-clientauthentication): 
    ClientAuthentication
  [ClusterName](#cfn-msk-cluster-clustername): String
  [ConfigurationInfo](#cfn-msk-cluster-configurationinfo): 
    ConfigurationInfo
  [CurrentVersion](#cfn-msk-cluster-currentversion): String
  [EncryptionInfo](#cfn-msk-cluster-encryptioninfo): 
    EncryptionInfo
  [EnhancedMonitoring](#cfn-msk-cluster-enhancedmonitoring): String
  [KafkaVersion](#cfn-msk-cluster-kafkaversion): String
  [LoggingInfo](#cfn-msk-cluster-logginginfo): 
    LoggingInfo
  [NumberOfBrokerNodes](#cfn-msk-cluster-numberofbrokernodes): Integer
  [OpenMonitoring](#cfn-msk-cluster-openmonitoring): 
    OpenMonitoring
  [StorageMode](#cfn-msk-cluster-storagemode): String
  [Tags](#cfn-msk-cluster-tags): 
    Key: Value
```

## Properties<a name="aws-resource-msk-cluster-properties"></a>

`BrokerNodeGroupInfo`  <a name="cfn-msk-cluster-brokernodegroupinfo"></a>
Information about the broker nodes in the cluster\.  
*Required*: Yes  
*Type*: [BrokerNodeGroupInfo](aws-properties-msk-cluster-brokernodegroupinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientAuthentication`  <a name="cfn-msk-cluster-clientauthentication"></a>
Includes all client authentication related information\.  
*Required*: No  
*Type*: [ClientAuthentication](aws-properties-msk-cluster-clientauthentication.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClusterName`  <a name="cfn-msk-cluster-clustername"></a>
The name of the cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationInfo`  <a name="cfn-msk-cluster-configurationinfo"></a>
Represents the configuration that you want MSK to use for the cluster\.  
*Required*: No  
*Type*: [ConfigurationInfo](aws-properties-msk-cluster-configurationinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CurrentVersion`  <a name="cfn-msk-cluster-currentversion"></a>
The version of the cluster that you want to update\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionInfo`  <a name="cfn-msk-cluster-encryptioninfo"></a>
Includes all encryption\-related information\.  
*Required*: No  
*Type*: [EncryptionInfo](aws-properties-msk-cluster-encryptioninfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnhancedMonitoring`  <a name="cfn-msk-cluster-enhancedmonitoring"></a>
Specifies the level of monitoring for the MSK cluster\. The possible values are `DEFAULT`, `PER_BROKER`, and `PER_TOPIC_PER_BROKER`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KafkaVersion`  <a name="cfn-msk-cluster-kafkaversion"></a>
The version of Apache Kafka\. You can use Amazon MSK to create clusters that use Apache Kafka versions 1\.1\.1 and 2\.2\.1\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingInfo`  <a name="cfn-msk-cluster-logginginfo"></a>
Logging Info details\.  
*Required*: No  
*Type*: [LoggingInfo](aws-properties-msk-cluster-logginginfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumberOfBrokerNodes`  <a name="cfn-msk-cluster-numberofbrokernodes"></a>
The number of broker nodes in the cluster\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpenMonitoring`  <a name="cfn-msk-cluster-openmonitoring"></a>
The settings for open monitoring\.  
*Required*: No  
*Type*: [OpenMonitoring](aws-properties-msk-cluster-openmonitoring.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StorageMode`  <a name="cfn-msk-cluster-storagemode"></a>
This controls storage mode for supported storage tiers\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-msk-cluster-tags"></a>
Create tags when creating the cluster\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-msk-cluster-return-values"></a>

### Ref<a name="aws-resource-msk-cluster-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-msk-cluster-return-values-fn--getatt"></a>

#### <a name="aws-resource-msk-cluster-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.