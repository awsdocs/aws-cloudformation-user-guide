# AWS::ManagedBlockchain::Member MemberFabricConfiguration<a name="aws-properties-managedblockchain-member-memberfabricconfiguration"></a>

Configuration properties for Hyperledger Fabric for a member in a Managed Blockchain network using the Hyperledger Fabric framework\.

## Syntax<a name="aws-properties-managedblockchain-member-memberfabricconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-managedblockchain-member-memberfabricconfiguration-syntax.json"></a>

```
{
  "[AdminPassword](#cfn-managedblockchain-member-memberfabricconfiguration-adminpassword)" : String,
  "[AdminUsername](#cfn-managedblockchain-member-memberfabricconfiguration-adminusername)" : String
}
```

### YAML<a name="aws-properties-managedblockchain-member-memberfabricconfiguration-syntax.yaml"></a>

```
  [AdminPassword](#cfn-managedblockchain-member-memberfabricconfiguration-adminpassword): String
  [AdminUsername](#cfn-managedblockchain-member-memberfabricconfiguration-adminusername): String
```

## Properties<a name="aws-properties-managedblockchain-member-memberfabricconfiguration-properties"></a>

`AdminPassword`  <a name="cfn-managedblockchain-member-memberfabricconfiguration-adminpassword"></a>
The password for the member's initial administrative user\. The `AdminPassword` must be at least eight characters long and no more than 32 characters\. It must contain at least one uppercase letter, one lowercase letter, and one digit\. It cannot have a single quotation mark \(‘\), a double quotation marks \(“\), a forward slash\(/\), a backward slash\(\\\), @, or a space\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `8`  
*Maximum*: `32`  
*Pattern*: `^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?!.*[@'\\"/])[a-zA-Z0-9\S]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AdminUsername`  <a name="cfn-managedblockchain-member-memberfabricconfiguration-adminusername"></a>
The user name for the member's initial administrative user\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `16`  
*Pattern*: `^[a-zA-Z][a-zA-Z0-9]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)