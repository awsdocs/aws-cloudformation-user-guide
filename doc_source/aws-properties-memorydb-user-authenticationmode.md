# AWS::MemoryDB::User AuthenticationMode<a name="aws-properties-memorydb-user-authenticationmode"></a>

Denotes the user's authentication properties, such as whether it requires a password to authenticate\. Used in output responses\.

## Syntax<a name="aws-properties-memorydb-user-authenticationmode-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-memorydb-user-authenticationmode-syntax.json"></a>

```
{
  "[Passwords](#cfn-memorydb-user-authenticationmode-passwords)" : [ String, ... ],
  "[Type](#cfn-memorydb-user-authenticationmode-type)" : String
}
```

### YAML<a name="aws-properties-memorydb-user-authenticationmode-syntax.yaml"></a>

```
  [Passwords](#cfn-memorydb-user-authenticationmode-passwords): 
    - String
  [Type](#cfn-memorydb-user-authenticationmode-type): String
```

## Properties<a name="aws-properties-memorydb-user-authenticationmode-properties"></a>

`Passwords`  <a name="cfn-memorydb-user-authenticationmode-passwords"></a>
The password\(s\) used for authentication  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-memorydb-user-authenticationmode-type"></a>
Indicates whether the user requires a password to authenticate\. All newly\-created users require a password\.  
*Required*: No  
*Type*: String  
*Allowed values*: `password`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)