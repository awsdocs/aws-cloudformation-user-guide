# AWS::MSK::Cluster EncryptionInTransit<a name="aws-properties-msk-cluster-encryptionintransit"></a>

The settings for encrypting data in transit\.

## Syntax<a name="aws-properties-msk-cluster-encryptionintransit-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-msk-cluster-encryptionintransit-syntax.json"></a>

```
{
  "[ClientBroker](#cfn-msk-cluster-encryptionintransit-clientbroker)" : String,
  "[InCluster](#cfn-msk-cluster-encryptionintransit-incluster)" : Boolean
}
```

### YAML<a name="aws-properties-msk-cluster-encryptionintransit-syntax.yaml"></a>

```
  [ClientBroker](#cfn-msk-cluster-encryptionintransit-clientbroker): String
  [InCluster](#cfn-msk-cluster-encryptionintransit-incluster): Boolean
```

## Properties<a name="aws-properties-msk-cluster-encryptionintransit-properties"></a>

`ClientBroker`  <a name="cfn-msk-cluster-encryptionintransit-clientbroker"></a>
Indicates the encryption setting for data in transit between clients and brokers\. The following are the possible values\.   
+ `TLS` means that client\-broker communication is enabled with TLS only\. 
+ `TLS_PLAINTEXT` means that client\-broker communication is enabled for both TLS\-encrypted, as well as plaintext data\. 
+ `PLAINTEXT` means that client\-broker communication is enabled in plaintext only\.
The default value is `TLS`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InCluster`  <a name="cfn-msk-cluster-encryptionintransit-incluster"></a>
When set to true, it indicates that data communication among the broker nodes of the cluster is encrypted\. When set to false, the communication happens in plaintext\. The default value is true\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)