# AWS::ManagedBlockchain::Node NodeConfiguration<a name="aws-properties-managedblockchain-node-nodeconfiguration"></a>

Configuration properties of a peer node within a membership\.

## Syntax<a name="aws-properties-managedblockchain-node-nodeconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-managedblockchain-node-nodeconfiguration-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-managedblockchain-node-nodeconfiguration-availabilityzone)" : String,
  "[InstanceType](#cfn-managedblockchain-node-nodeconfiguration-instancetype)" : String
}
```

### YAML<a name="aws-properties-managedblockchain-node-nodeconfiguration-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-managedblockchain-node-nodeconfiguration-availabilityzone): String
  [InstanceType](#cfn-managedblockchain-node-nodeconfiguration-instancetype): String
```

## Properties<a name="aws-properties-managedblockchain-node-nodeconfiguration-properties"></a>

`AvailabilityZone`  <a name="cfn-managedblockchain-node-nodeconfiguration-availabilityzone"></a>
The Availability Zone in which the node exists\. Required for Ethereum nodes\. Ethereum on Managed Blockchain is in preview release and is subject to change\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-managedblockchain-node-nodeconfiguration-instancetype"></a>
The Amazon Managed Blockchain instance type for the node\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)