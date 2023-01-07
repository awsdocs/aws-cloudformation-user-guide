# AWS::OpsWorks::UserProfile<a name="aws-resource-opsworks-userprofile"></a>

Describes a user's SSH information\.

## Syntax<a name="aws-resource-opsworks-userprofile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

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
Type: AWS::OpsWorks::UserProfile
Properties: 
  [AllowSelfManagement](#cfn-opsworks-userprofile-allowselfmanagement): Boolean
  [IamUserArn](#cfn-opsworks-userprofile-iamuserarn): String
  [SshPublicKey](#cfn-opsworks-userprofile-sshpublickey): String
  [SshUsername](#cfn-opsworks-userprofile-sshusername): String
```

## Properties<a name="aws-resource-opsworks-userprofile-properties"></a>

`AllowSelfManagement`  <a name="cfn-opsworks-userprofile-allowselfmanagement"></a>
Whether users can specify their own SSH public key through the My Settings page\. For more information, see [Managing User Permissions](https://docs.aws.amazon.com/opsworks/latest/userguide/security-settingsshkey.html)\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IamUserArn`  <a name="cfn-opsworks-userprofile-iamuserarn"></a>
The user's IAM ARN\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SshPublicKey`  <a name="cfn-opsworks-userprofile-sshpublickey"></a>
The user's SSH public key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SshUsername`  <a name="cfn-opsworks-userprofile-sshusername"></a>
The user's SSH user name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-opsworks-userprofile-return-values"></a>

### Ref<a name="aws-resource-opsworks-userprofile-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IAM user ARN, such as `arn:aws:iam::123456789012:user/opsworksuser`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-opsworks-userprofile-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-opsworks-userprofile-return-values-fn--getatt-fn--getatt"></a>

`SshUsername`  <a name="SshUsername-fn::getatt"></a>
The user's SSH user name, as a string\.

## Examples<a name="aws-resource-opsworks-userprofile--examples"></a>

### Template Snippet<a name="aws-resource-opsworks-userprofile--examples--Template_Snippet"></a>

The following example registers a public key to the `testUser` IAM user\. Users can also use self\-management to specify their own public keys\.

#### JSON<a name="aws-resource-opsworks-userprofile--examples--Template_Snippet--json"></a>

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

#### YAML<a name="aws-resource-opsworks-userprofile--examples--Template_Snippet--yaml"></a>

```
userProfile:
  Type: AWS::OpsWorks::UserProfile
  Properties:
    IamUserArn: !GetAtt [testUser, Arn]
    AllowSelfManagement: 'true'
    SshPublicKey: xyz1234567890
```

## See also<a name="aws-resource-opsworks-userprofile--seealso"></a>
+  [CreateUserProfile](https://docs.aws.amazon.com/opsworks/latest/APIReference/API_CreateUserProfile.html) in the *AWS OpsWorks API Reference*\.
+  [Managing AWS OpsWorks Stacks User Permissions](https://docs.aws.amazon.com/opsworks/latest/userguide/opsworks-security-users.html) in the *AWS OpsWorks User Guide*\.

