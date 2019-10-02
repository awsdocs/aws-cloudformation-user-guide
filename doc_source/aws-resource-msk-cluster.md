# AWS::MSK::Cluster<a name="aws-resource-msk-cluster"></a>

The `AWS::MSK::Cluster` resource creates an Amazon MSK cluster\. For more information, see [What Is Amazon MSK?](https://docs.aws.amazon.com/msk/latest/developerguide/what-is-msk.html) in the *Amazon MSK Developer Guide*\.

## Syntax<a name="aws-resource-msk-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-msk-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::MSK::Cluster",
  "Properties" : {
      "[BrokerNodeGroupInfo](#cfn-msk-cluster-brokernodegroupinfo)" : [BrokerNodeGroupInfo](aws-properties-msk-cluster-brokernodegroupinfo.md),
      "[ClientAuthentication](#cfn-msk-cluster-clientauthentication)" : [ClientAuthentication](aws-properties-msk-cluster-clientauthentication.md),
      "[ClusterName](#cfn-msk-cluster-clustername)" : String,
      "[ConfigurationInfo](#cfn-msk-cluster-configurationinfo)" : [ConfigurationInfo](aws-properties-msk-cluster-configurationinfo.md),
      "[EncryptionInfo](#cfn-msk-cluster-encryptioninfo)" : [EncryptionInfo](aws-properties-msk-cluster-encryptioninfo.md),
      "[EnhancedMonitoring](#cfn-msk-cluster-enhancedmonitoring)" : String,
      "[KafkaVersion](#cfn-msk-cluster-kafkaversion)" : String,
      "[NumberOfBrokerNodes](#cfn-msk-cluster-numberofbrokernodes)" : Integer,
      "[Tags](#cfn-msk-cluster-tags)" : Json
    }
}
```

### YAML<a name="aws-resource-msk-cluster-syntax.yaml"></a>

```
Type: AWS::MSK::Cluster
Properties: 
  [BrokerNodeGroupInfo](#cfn-msk-cluster-brokernodegroupinfo): 
    [BrokerNodeGroupInfo](aws-properties-msk-cluster-brokernodegroupinfo.md)
  [ClientAuthentication](#cfn-msk-cluster-clientauthentication): 
    [ClientAuthentication](aws-properties-msk-cluster-clientauthentication.md)
  [ClusterName](#cfn-msk-cluster-clustername): String
  [ConfigurationInfo](#cfn-msk-cluster-configurationinfo): 
    [ConfigurationInfo](aws-properties-msk-cluster-configurationinfo.md)
  [EncryptionInfo](#cfn-msk-cluster-encryptioninfo): 
    [EncryptionInfo](aws-properties-msk-cluster-encryptioninfo.md)
  [EnhancedMonitoring](#cfn-msk-cluster-enhancedmonitoring): String
  [KafkaVersion](#cfn-msk-cluster-kafkaversion): String
  [NumberOfBrokerNodes](#cfn-msk-cluster-numberofbrokernodes): Integer
  [Tags](#cfn-msk-cluster-tags): Json
```

## Properties<a name="aws-resource-msk-cluster-properties"></a>

`BrokerNodeGroupInfo`  <a name="cfn-msk-cluster-brokernodegroupinfo"></a>
The setup to be used for brokers in the cluster\.  
*Required*: Yes  
*Type*: [BrokerNodeGroupInfo](aws-properties-msk-cluster-brokernodegroupinfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClientAuthentication`  <a name="cfn-msk-cluster-clientauthentication"></a>
Includes information related to client authentication\.  
*Required*: No  
*Type*: [ClientAuthentication](aws-properties-msk-cluster-clientauthentication.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterName`  <a name="cfn-msk-cluster-clustername"></a>
The name of the cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConfigurationInfo`  <a name="cfn-msk-cluster-configurationinfo"></a>
The Amazon MSK configuration to use for the cluster\.  
*Required*: No  
*Type*: [ConfigurationInfo](aws-properties-msk-cluster-configurationinfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EncryptionInfo`  <a name="cfn-msk-cluster-encryptioninfo"></a>
Includes all encryption\-related information\.  
*Required*: No  
*Type*: [EncryptionInfo](aws-properties-msk-cluster-encryptioninfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EnhancedMonitoring`  <a name="cfn-msk-cluster-enhancedmonitoring"></a>
Specifies the level of monitoring for the MSK cluster\. The possible values are `DEFAULT`, `PER_BROKER`, and `PER_TOPIC_PER_BROKER`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KafkaVersion`  <a name="cfn-msk-cluster-kafkaversion"></a>
The version of Apache Kafka\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NumberOfBrokerNodes`  <a name="cfn-msk-cluster-numberofbrokernodes"></a>
The number of broker nodes you want in the Amazon MSK cluster\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-msk-cluster-tags"></a>
An array of key\-value pairs to apply to this resource\. You can specify tags in JSON or in YAML, depending on which format you use for your template\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-msk-cluster-return-values"></a>

### Ref<a name="aws-resource-msk-cluster-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon MSK cluster ARN\. For example:

 `REF MyTestCluster` 

For the Amazon MSK cluster `MyTestCluster`, Ref returns the ARN of the cluster\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-msk-cluster--examples"></a>

### Create an MSK Cluster Where You Only Specify Values for the Required Properties<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Only_Specify_Values_for_the_Required_Properties"></a>

#### YAML<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Only_Specify_Values_for_the_Required_Properties--yaml"></a>

```
---
Description: "MSK Cluster with required properties."
Resources:
  TestCluster:
    Type: "AWS::MSK::Cluster"
    Properties:
      ClusterName: "ClusterWithRequiredProperties"
      KafkaVersion: "2.1.0"
      NumberOfBrokerNodes: 3
      BrokerNodeGroupInfo:
        InstanceType: "kafka.m5.large"
        ClientSubnets:
        - "ReplaceWithSubnetId1"
        - "ReplaceWithSubnetId2"
        - "ReplaceWithSubnetId3"
```

### Create an MSK Cluster Where You Explicitly Set All Properties<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Explicitly_Set_All_Properties"></a>

#### YAML<a name="aws-resource-msk-cluster--examples--Create_an_MSK_Cluster_Where_You_Explicitly_Set_All_Properties--yaml"></a>

```
---
Description: "MSK Cluster with all properties"
Resources:
  TestCluster:
    Type: "AWS::MSK::Cluster"
    Properties:
      ClusterName: "ClusterWithAllProperties"
      KafkaVersion: "2.1.0"
      NumberOfBrokerNodes: 3
      EnhancedMonitoring: "PER_BROKER"
      EncryptionInfo:
        EncryptionAtRest:
          DataVolumeKMSKeyId: "ReplaceWithKmsKeyArn"
        EncryptionInTransit:
          ClientBroker: "TLS"
          InCluster: true
      ConfigurationInfo:
        Arn: "ReplaceWithConfigurationArn"
        Revision: 1
      ClientAuthentication:
        Tls:
          CertificateAuthorityArnList:
          - "ReplaceWithCAArn"
      Tags:
        MyTagName: "MyTagValue"
      BrokerNodeGroupInfo:
        BrokerAZDistribution: "DEFAULT"
        InstanceType: "kafka.m5.large"
        SecurityGroups:
        - "ReplaceWithSecurityGroupId"
        StorageInfo:
          EBSStorageInfo:
            VolumeSize: 100
        ClientSubnets:
        - "ReplaceWithSubnetId1"
        - "ReplaceWithSubnetId2"
        - "ReplaceWithSubnetId3"
```

## Supported Regions

This ResourceType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `eu-west-3`
- `us-east-1`
- `us-east-2`
- `us-west-2`
