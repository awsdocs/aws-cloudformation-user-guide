# AWS::ManagedBlockchain::Member MemberConfiguration<a name="aws-properties-managedblockchain-member-memberconfiguration"></a>

Configuration properties of the member\.

Applies only to Hyperledger Fabric\.

## Syntax<a name="aws-properties-managedblockchain-member-memberconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-managedblockchain-member-memberconfiguration-syntax.json"></a>

```
{
  "[Description](#cfn-managedblockchain-member-memberconfiguration-description)" : String,
  "[MemberFrameworkConfiguration](#cfn-managedblockchain-member-memberconfiguration-memberframeworkconfiguration)" : MemberFrameworkConfiguration,
  "[Name](#cfn-managedblockchain-member-memberconfiguration-name)" : String
}
```

### YAML<a name="aws-properties-managedblockchain-member-memberconfiguration-syntax.yaml"></a>

```
  [Description](#cfn-managedblockchain-member-memberconfiguration-description): String
  [MemberFrameworkConfiguration](#cfn-managedblockchain-member-memberconfiguration-memberframeworkconfiguration): 
    MemberFrameworkConfiguration
  [Name](#cfn-managedblockchain-member-memberconfiguration-name): String
```

## Properties<a name="aws-properties-managedblockchain-member-memberconfiguration-properties"></a>

`Description`  <a name="cfn-managedblockchain-member-memberconfiguration-description"></a>
An optional description of the member\.  
*Required*: No  
*Type*: String  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemberFrameworkConfiguration`  <a name="cfn-managedblockchain-member-memberconfiguration-memberframeworkconfiguration"></a>
Configuration properties of the blockchain framework relevant to the member\.  
*Required*: No  
*Type*: [MemberFrameworkConfiguration](aws-properties-managedblockchain-member-memberframeworkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-managedblockchain-member-memberconfiguration-name"></a>
The name of the member\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `^(?!-|[0-9])(?!.*-$)(?!.*?--)[a-zA-Z0-9-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)