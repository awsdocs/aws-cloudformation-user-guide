# AWS::IdentityStore::Group<a name="aws-resource-identitystore-group"></a>

A group object, which contains a specified group’s metadata and attributes\.

## Syntax<a name="aws-resource-identitystore-group-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-identitystore-group-syntax.json"></a>

```
{
  "Type" : "AWS::IdentityStore::Group",
  "Properties" : {
      "[Description](#cfn-identitystore-group-description)" : String,
      "[DisplayName](#cfn-identitystore-group-displayname)" : String,
      "[IdentityStoreId](#cfn-identitystore-group-identitystoreid)" : String
    }
}
```

### YAML<a name="aws-resource-identitystore-group-syntax.yaml"></a>

```
Type: AWS::IdentityStore::Group
Properties: 
  [Description](#cfn-identitystore-group-description): String
  [DisplayName](#cfn-identitystore-group-displayname): String
  [IdentityStoreId](#cfn-identitystore-group-identitystoreid): String
```

## Properties<a name="aws-resource-identitystore-group-properties"></a>

`Description`  <a name="cfn-identitystore-group-description"></a>
A string containing the description of the group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-identitystore-group-displayname"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityStoreId`  <a name="cfn-identitystore-group-identitystoreid"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-identitystore-group-return-values"></a>

### Ref<a name="aws-resource-identitystore-group-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-identitystore-group-return-values-fn--getatt"></a>

#### <a name="aws-resource-identitystore-group-return-values-fn--getatt-fn--getatt"></a>

`GroupId`  <a name="GroupId-fn::getatt"></a>
The identifier of the newly created group in the identity store\.