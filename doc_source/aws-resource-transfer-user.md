# AWS::Transfer::User<a name="aws-resource-transfer-user"></a>

Creates a user and associates them with an existing Secure File Transfer Protocol \(SFTP\) server\. You can only create and associate users with SFTP servers that have the `IdentityProviderType` set to `SERVICE_MANAGED`\. Using parameters for `CreateUser`, you can specify the user name, set the home directory, store the user's public key, and assign the user's AWS Identity and Access Management \(IAM\) role\. You can also optionally add a scope\-down policy, and assign metadata with tags that can be used to group and search for users\.

## Syntax<a name="aws-resource-transfer-user-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-user-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::User",
  "Properties" : {
      "[HomeDirectory](#cfn-transfer-user-homedirectory)" : String,
      "[Policy](#cfn-transfer-user-policy)" : String,
      "[Role](#cfn-transfer-user-role)" : String,
      "[ServerId](#cfn-transfer-user-serverid)" : String,
      "[SshPublicKeys](#cfn-transfer-user-sshpublickeys)" : [ [SshPublicKey](aws-properties-transfer-user-sshpublickey.md), ... ],
      "[Tags](#cfn-transfer-user-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[UserName](#cfn-transfer-user-username)" : String
    }
}
```

### YAML<a name="aws-resource-transfer-user-syntax.yaml"></a>

```
Type: AWS::Transfer::User
Properties: 
  [HomeDirectory](#cfn-transfer-user-homedirectory): String
  [Policy](#cfn-transfer-user-policy): String
  [Role](#cfn-transfer-user-role): String
  [ServerId](#cfn-transfer-user-serverid): String
  [SshPublicKeys](#cfn-transfer-user-sshpublickeys): 
    - [SshPublicKey](aws-properties-transfer-user-sshpublickey.md)
  [Tags](#cfn-transfer-user-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserName](#cfn-transfer-user-username): String
```

## Properties<a name="aws-resource-transfer-user-properties"></a>

`HomeDirectory`  <a name="cfn-transfer-user-homedirectory"></a>
The landing directory \(folder\) for a user when they log in to the server using their SFTP client\. An example is `/home/username `\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^$|/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policy`  <a name="cfn-transfer-user-policy"></a>
A scope\-down policy for your user so you can use the same IAM role across multiple users\. This policy scopes down user access to portions of their Amazon S3 bucket\. Variables that you can use inside this policy include `${Transfer:UserName}`, `${Transfer:HomeDirectory}`, and `${Transfer:HomeBucket}`\.  
For scope\-down policies, AWS Transfer for SFTP stores the policy as a JSON blob, instead of the Amazon Resource Name \(ARN\) of the policy\. You save the policy as a JSON blob and pass it in the `Policy` argument\.  
For an example of a scope\-down policy, see [Creating a Scope\-Down Policy](https://docs.aws.amazon.com/transfer/latest/userguide/users.html#users-policies-scope-down)\.  
For more information, see [AssumeRole](https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html) in the *AWS Security Token Service API Reference*\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-transfer-user-role"></a>
The IAM role that controls your user's access to your Amazon S3 bucket\. The policies attached to this role will determine the level of access you want to provide your users when transferring files into and out of your Amazon S3 bucket or buckets\. The IAM role should also contain a trust relationship that allows the SFTP server to access your resources when servicing your SFTP user's transfer requests\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerId`  <a name="cfn-transfer-user-serverid"></a>
A system\-assigned unique identifier for an SFTP server instance\. This is the specific SFTP server that you added your user to\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^s-([0-9a-f]{17})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SshPublicKeys`  <a name="cfn-transfer-user-sshpublickeys"></a>
This property contains the public key portion of the Secure Shell \(SSH\) keys stored for the described user\.  
*Required*: No  
*Type*: List of [SshPublicKey](aws-properties-transfer-user-sshpublickey.md)  
*Maximum*: `5`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-transfer-user-tags"></a>
Key\-value pairs that can be used to group and search for users\. Tags are metadata attached to users for any purpose\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserName`  <a name="cfn-transfer-user-username"></a>
A unique string that identifies a user and is associated with a server as specified by the `ServerId`\. This user name must be a minimum of 3 and a maximum of 32 characters long\. The following are valid characters: a\-z, A\-Z, 0\-9, underscore, and hyphen\. The user name can't start with a hyphen\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9_][a-zA-Z0-9_-]{2,31}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-transfer-user-return-values"></a>

### Ref<a name="aws-resource-transfer-user-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the username, such as `sftp_user`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-transfer-user-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-transfer-user-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name associated with the AWS Transfer SFTP user, in the form `arn:aws:transfer:region:account-id:user/server-id/username`\.  
An example of a user ARN is: `arn:aws:transfer:us-east-1:123456789012:user/user1`\.

`ServerId`  <a name="ServerId-fn::getatt"></a>
The ID of the SFTP server to which the user is attached\.  
An example `ServerId` is `s-01234567890abcdef`\.

`UserName`  <a name="UserName-fn::getatt"></a>
A unique string that identifies a user account associated with an SFTP server\.  
An example `UserName` is `sftp-user-1`\.