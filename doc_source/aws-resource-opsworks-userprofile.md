# AWS::OpsWorks::UserProfile<a name="aws-resource-opsworks-userprofile"></a>

The `AWS::OpsWorks::UserProfile` resource configures SSH access for users who require access to instances in an AWS OpsWorks stack\.

**Topics**
+ [Syntax](#aws-resource-opsworks-userprofile-syntax)
+ [Properties](#aws-resource-opsworks-userprofile-properties)
+ [Return Value](#aws-resource-opsworks-userprofile-returnvalues)
+ [Example](#aws-resource-opsworks-userprofile-examples)

## Syntax<a name="aws-resource-opsworks-userprofile-syntax"></a>

### JSON<a name="aws-resource-opsworks-userprofile-syntax.json"></a>

```
{
  "Type" : "AWS::OpsWorks::UserProfile",
  "Properties" : {
    "[AllowSelfManagement](#cfn-opsworks-userprofile-allowselfmanagement)" : Boolean,
    "[IamUserArn](#cfn-opsworks-userprofile-iamuserarn)" : String,
    "[SshPublicKey](#cfn-opsworks-userprofile-sshpublickey)" : String,
    "[SshUsername](#cfn-opsworks-userprofile-sshusername)" : String
  }
}
```

### YAML<a name="aws-resource-opsworks-userprofile-syntax.yaml"></a>

```
Type: "AWS::OpsWorks::UserProfile"
Properties:
  [AllowSelfManagement](#cfn-opsworks-userprofile-allowselfmanagement): Boolean
  [IamUserArn](#cfn-opsworks-userprofile-iamuserarn): String
  [SshPublicKey](#cfn-opsworks-userprofile-sshpublickey): String
  [SshUsername](#cfn-opsworks-userprofile-sshusername): String
```

## Properties<a name="aws-resource-opsworks-userprofile-properties"></a>

`AllowSelfManagement`  <a name="cfn-opsworks-userprofile-allowselfmanagement"></a>
Indicates whether users can use the AWS OpsWorks **My Settings** page to specify their own SSH public key\. For more information, see [Setting an IAM User's Public SSH Key](http://docs.aws.amazon.com/opsworks/latest/userguide/security-settingsshkey.html) in the *AWS OpsWorks User Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`IamUserArn`  <a name="cfn-opsworks-userprofile-iamuserarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) user to associate with this configuration\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`SshPublicKey`  <a name="cfn-opsworks-userprofile-sshpublickey"></a>
The public SSH key that is associated with the IAM user\. To access instances, the IAM user must have or be given the corresponding private key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SshUsername`  <a name="cfn-opsworks-userprofile-sshusername"></a>
The user's SSH user name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="aws-resource-opsworks-userprofile-returnvalues"></a>

### Ref<a name="w3ab2c21c10d939c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the IAM user ARN, such as `arn:aws:iam::123456789012:user/opsworksuser`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d939c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.
+ `SshUsername`

  The user's SSH user name, as a string\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="aws-resource-opsworks-userprofile-examples"></a>

The following example registers a public key to the `testUser` IAM user\. The user can also use self\-management to specify his or her own public key\.

### JSON<a name="aws-resource-opsworks-userprofile-example.json"></a>

```
"userProfile": {
  "Type": "AWS::OpsWorks::UserProfile",
  "Properties": {
    "IamUserArn": {
      "Fn::GetAtt": ["testUser", "Arn"]
    },
    "AllowSelfManagement": "true",
    "SshPublicKey": "xyz1234567890"
  }
}
```

### YAML<a name="aws-resource-opsworks-userprofile-example.yaml"></a>

```
userProfile:
  Type: AWS::OpsWorks::UserProfile
  Properties:
    IamUserArn: !GetAtt [testUser, Arn]
    AllowSelfManagement: 'true'
    SshPublicKey: xyz1234567890
```