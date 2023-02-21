# AWS::MemoryDB::User<a name="aws-resource-memorydb-user"></a>

Specifies a MemoryDB user\. For more information, see [Authenticating users with Access Contol Lists \(ACLs\)](https://docs.aws.amazon.com/memorydb/latest/devguide/clusters.acls.html)\.

## Syntax<a name="aws-resource-memorydb-user-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-memorydb-user-syntax.json"></a>

```
{
  "Type" : "AWS::MemoryDB::User",
  "Properties" : {
      "[AccessString](#cfn-memorydb-user-accessstring)" : String,
      "[AuthenticationMode](#cfn-memorydb-user-authenticationmode)" : AuthenticationMode,
      "[Tags](#cfn-memorydb-user-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserName](#cfn-memorydb-user-username)" : String
    }
}
```

### YAML<a name="aws-resource-memorydb-user-syntax.yaml"></a>

```
Type: AWS::MemoryDB::User
Properties: 
  [AccessString](#cfn-memorydb-user-accessstring): 
    String
  [AuthenticationMode](#cfn-memorydb-user-authenticationmode): 
    AuthenticationMode
  [Tags](#cfn-memorydb-user-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserName](#cfn-memorydb-user-username): String
```

## Properties<a name="aws-resource-memorydb-user-properties"></a>

`AccessString`  <a name="cfn-memorydb-user-accessstring"></a>
Access permissions string used for this user\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AuthenticationMode`  <a name="cfn-memorydb-user-authenticationmode"></a>
Denotes whether the user requires a password to authenticate\.  
**Example:**   

```
mynewdbuser:
     Type: AWS::MemoryDB::User
     Properties: 
     AccessString: on ~* &* +@all
     AuthenticationMode: 
         Passwords: '1234567890123456'
         Type: password
     UserName: mynewdbuser
     
     AuthenticationMode:
     {
         "Passwords": ["1234567890123456"],
         "Type": "Password"
     }
```
*Required*: Yes  
*Type*: [AuthenticationMode](aws-properties-memorydb-user-authenticationmode.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-memorydb-user-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserName`  <a name="cfn-memorydb-user-username"></a>
The name of the user\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-memorydb-user-return-values"></a>

### Fn::GetAtt<a name="aws-resource-memorydb-user-return-values-fn--getatt"></a>

#### <a name="aws-resource-memorydb-user-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
When you pass the logical ID of this resource to the intrinsic `Ref` function, Ref returns the ARN of the user, such as `arn:aws:memorydb:us-east-1:123456789012:user/user1`

`Status`  <a name="Status-fn::getatt"></a>
Indicates the user status\.  
*Valid values*: `active` \| `modifying` \| `deleting`