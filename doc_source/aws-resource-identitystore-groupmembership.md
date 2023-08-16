# AWS::IdentityStore::GroupMembership<a name="aws-resource-identitystore-groupmembership"></a>

Contains the identifiers for a group, a group member, and a `GroupMembership` object in the identity store\.

## Syntax<a name="aws-resource-identitystore-groupmembership-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-identitystore-groupmembership-syntax.json"></a>

```
{
  "Type" : "AWS::IdentityStore::GroupMembership",
  "Properties" : {
      "[GroupId](#cfn-identitystore-groupmembership-groupid)" : String,
      "[IdentityStoreId](#cfn-identitystore-groupmembership-identitystoreid)" : String,
      "[MemberId](#cfn-identitystore-groupmembership-memberid)" : MemberId
    }
}
```

### YAML<a name="aws-resource-identitystore-groupmembership-syntax.yaml"></a>

```
Type: AWS::IdentityStore::GroupMembership
Properties: 
  [GroupId](#cfn-identitystore-groupmembership-groupid): String
  [IdentityStoreId](#cfn-identitystore-groupmembership-identitystoreid): String
  [MemberId](#cfn-identitystore-groupmembership-memberid): 
    MemberId
```

## Properties<a name="aws-resource-identitystore-groupmembership-properties"></a>

`GroupId`  <a name="cfn-identitystore-groupmembership-groupid"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityStoreId`  <a name="cfn-identitystore-groupmembership-identitystoreid"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MemberId`  <a name="cfn-identitystore-groupmembership-memberid"></a>
An object containing the identifier of a group member\. Setting `MemberId`'s `UserId` field to a specific User's ID indicates we should consider that User as a group member\.  
*Required*: Yes  
*Type*: [MemberId](aws-properties-identitystore-groupmembership-memberid.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-identitystore-groupmembership-return-values"></a>

### Ref<a name="aws-resource-identitystore-groupmembership-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-identitystore-groupmembership-return-values-fn--getatt"></a>

#### <a name="aws-resource-identitystore-groupmembership-return-values-fn--getatt-fn--getatt"></a>

`MembershipId`  <a name="MembershipId-fn::getatt"></a>
The identifier for a `GroupMembership` in the identity store\.