# AWS::ManagedBlockchain::Member NetworkFrameworkConfiguration<a name="aws-properties-managedblockchain-member-networkframeworkconfiguration"></a>

 Configuration properties relevant to the network for the blockchain framework that the network uses\. 

## Syntax<a name="aws-properties-managedblockchain-member-networkframeworkconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-managedblockchain-member-networkframeworkconfiguration-syntax.json"></a>

```
{
  "[NetworkFabricConfiguration](#cfn-managedblockchain-member-networkframeworkconfiguration-networkfabricconfiguration)" : NetworkFabricConfiguration
}
```

### YAML<a name="aws-properties-managedblockchain-member-networkframeworkconfiguration-syntax.yaml"></a>

```
  [NetworkFabricConfiguration](#cfn-managedblockchain-member-networkframeworkconfiguration-networkfabricconfiguration): 
    NetworkFabricConfiguration
```

## Properties<a name="aws-properties-managedblockchain-member-networkframeworkconfiguration-properties"></a>

`NetworkFabricConfiguration`  <a name="cfn-managedblockchain-member-networkframeworkconfiguration-networkfabricconfiguration"></a>
Configuration properties for Hyperledger Fabric for a member in a Managed Blockchain network using the Hyperledger Fabric framework\.  
*Required*: No  
*Type*: [NetworkFabricConfiguration](aws-properties-managedblockchain-member-networkfabricconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)