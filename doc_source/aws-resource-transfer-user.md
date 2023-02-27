# AWS::Transfer::User<a name="aws-resource-transfer-user"></a>

The `AWS::Transfer::User` resource creates a user and associates them with an existing server\. You can only create and associate users with servers that have the `IdentityProviderType` set to `SERVICE_MANAGED`\. Using parameters for `CreateUser`, you can specify the user name, set the home directory, store the user's public key, and assign the user's AWS Identity and Access Management \(IAM\) role\. You can also optionally add a session policy, and assign metadata with tags that can be used to group and search for users\.

## Syntax<a name="aws-resource-transfer-user-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-user-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::User",
  "Properties" : {
      "[HomeDirectory](#cfn-transfer-user-homedirectory)" : String,
      "[HomeDirectoryMappings](#cfn-transfer-user-homedirectorymappings)" : [ HomeDirectoryMapEntry, ... ],
      "[HomeDirectoryType](#cfn-transfer-user-homedirectorytype)" : String,
      "[Policy](#cfn-transfer-user-policy)" : String,
      "[PosixProfile](#cfn-transfer-user-posixprofile)" : PosixProfile,
      "[Role](#cfn-transfer-user-role)" : String,
      "[ServerId](#cfn-transfer-user-serverid)" : String,
      "[SshPublicKeys](#cfn-transfer-user-sshpublickeys)" : [ SshPublicKey, ... ],
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
  [HomeDirectoryMappings](#cfn-transfer-user-homedirectorymappings): 
    - HomeDirectoryMapEntry
  [HomeDirectoryType](#cfn-transfer-user-homedirectorytype): String
  [Policy](#cfn-transfer-user-policy): String
  [PosixProfile](#cfn-transfer-user-posixprofile): 
    PosixProfile
  [Role](#cfn-transfer-user-role): String
  [ServerId](#cfn-transfer-user-serverid): String
  [SshPublicKeys](#cfn-transfer-user-sshpublickeys): 
    - SshPublicKey
  [Tags](#cfn-transfer-user-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [UserName](#cfn-transfer-user-username): String
```

## Properties<a name="aws-resource-transfer-user-properties"></a>

`HomeDirectory`  <a name="cfn-transfer-user-homedirectory"></a>
The landing directory \(folder\) for a user when they log in to the server using the client\.  
A `HomeDirectory` example is `/bucket_name/home/mydirectory`\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Pattern*: `^$|/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HomeDirectoryMappings`  <a name="cfn-transfer-user-homedirectorymappings"></a>
Logical directory mappings that specify what Amazon S3 paths and keys should be visible to your user and how you want to make them visible\. You will need to specify the "`Entry`" and "`Target`" pair, where `Entry` shows how the path is made visible and `Target` is the actual Amazon S3 path\. If you only specify a target, it will be displayed as is\. You will need to also make sure that your IAM role provides access to paths in `Target`\. The following is an example\.  
 `'[ { "Entry": "/", "Target": "/bucket3/customized-reports/" } ]'`   
In most cases, you can use this value instead of the session policy to lock your user down to the designated home directory \("chroot"\)\. To do this, you can set `Entry` to '/' and set `Target` to the HomeDirectory parameter value\.  
If the target of a logical directory entry does not exist in Amazon S3, the entry will be ignored\. As a workaround, you can use the Amazon S3 API to create 0 byte objects as place holders for your directory\. If using the CLI, use the `s3api` call instead of `s3` so you can use the put\-object operation\. For example, you use the following: `AWS s3api put-object --bucket bucketname --key path/to/folder/`\. Make sure that the end of the key name ends in a '/' for it to be considered a folder\.
*Required*: No  
*Type*: List of [HomeDirectoryMapEntry](aws-properties-transfer-user-homedirectorymapentry.md)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HomeDirectoryType`  <a name="cfn-transfer-user-homedirectorytype"></a>
The type of landing directory \(folder\) that you want your users' home directory to be when they log in to the server\. If you set it to `PATH`, the user will see the absolute Amazon S3 bucket or EFS paths as is in their file transfer protocol clients\. If you set it `LOGICAL`, you need to provide mappings in the `HomeDirectoryMappings` for how you want to make Amazon S3 or Amazon EFS paths visible to your users\.  
*Required*: No  
*Type*: String  
*Allowed values*: `LOGICAL | PATH`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Policy`  <a name="cfn-transfer-user-policy"></a>
A session policy for your user so you can use the same IAM role across multiple users\. This policy restricts user access to portions of their Amazon S3 bucket\. Variables that you can use inside this policy include `${Transfer:UserName}`, `${Transfer:HomeDirectory}`, and `${Transfer:HomeBucket}`\.  
For session policies, AWS Transfer Family stores the policy as a JSON blob, instead of the Amazon Resource Name \(ARN\) of the policy\. You save the policy as a JSON blob and pass it in the `Policy` argument\.  
For an example of a session policy, see [Example session policy](https://docs.aws.amazon.com/transfer/latest/userguide/session-policy.html)\.  
For more information, see [AssumeRole](https://docs.aws.amazon.com/STS/latest/APIReference/API_AssumeRole.html) in the *AWS Security Token Service API Reference*\.
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PosixProfile`  <a name="cfn-transfer-user-posixprofile"></a>
Specifies the full POSIX identity, including user ID \(`Uid`\), group ID \(`Gid`\), and any secondary groups IDs \(`SecondaryGids`\), that controls your users' access to your Amazon Elastic File System \(Amazon EFS\) file systems\. The POSIX permissions that are set on files and directories in your file system determine the level of access your users get when transferring files into and out of your Amazon EFS file systems\.  
*Required*: No  
*Type*: [PosixProfile](aws-properties-transfer-user-posixprofile.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Role`  <a name="cfn-transfer-user-role"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role that controls your users' access to your Amazon S3 bucket or Amazon EFS file system\. The policies attached to this role determine the level of access that you want to provide your users when transferring files into and out of your Amazon S3 bucket or Amazon EFS file system\. The IAM role should also contain a trust relationship that allows the server to access your resources when servicing your users' transfer requests\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerId`  <a name="cfn-transfer-user-serverid"></a>
A system\-assigned unique identifier for a server instance\. This is the specific server that you added your user to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `19`  
*Maximum*: `19`  
*Pattern*: `^s-([0-9a-f]{17})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SshPublicKeys`  <a name="cfn-transfer-user-sshpublickeys"></a>
Specifies the public key portion of the Secure Shell \(SSH\) keys stored for the described user\.  
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
A unique string that identifies a user and is associated with a `ServerId`\. This user name must be a minimum of 3 and a maximum of 100 characters long\. The following are valid characters: a\-z, A\-Z, 0\-9, underscore '\_', hyphen '\-', period '\.', and at sign '@'\. The user name can't start with a hyphen, period, or at sign\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `100`  
*Pattern*: `^[\w][\w@.-]{2,99}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-transfer-user-return-values"></a>

### Ref<a name="aws-resource-transfer-user-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the username, such as `transfer_user`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-transfer-user-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-transfer-user-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name associated with the user, in the form `arn:aws:transfer:region:account-id:user/server-id/username`\.  
An example of a user ARN is: `arn:aws:transfer:us-east-1:123456789012:user/user1`\.

`ServerId`  <a name="ServerId-fn::getatt"></a>
The ID of the server to which the user is attached\.  
An example `ServerId` is `s-01234567890abcdef`\.

`UserName`  <a name="UserName-fn::getatt"></a>
A unique string that identifies a Transfer Family user account associated with a server\.  
An example `UserName` is `transfer-user-1`\.

## Examples<a name="aws-resource-transfer-user--examples"></a>



### Associate a user with a server<a name="aws-resource-transfer-user--examples--Associate_a_user_with_a_server"></a>

The following example associates a user with a server\.

#### JSON<a name="aws-resource-transfer-user--examples--Associate_a_user_with_a_server--json"></a>

```
"User": {
      "Type": "AWS::Transfer::User",
      "Properties": {
         "HomeDirectoryMappings": [
            {
               "Entry": "/",
               "Target": "/my-bucket/"
            }
         ],
         "HomeDirectoryType": "LOGICAL",
         "Policy": {
           "Fn::Sub": "{
             \"Version\": \"2012-10-17T00:00:00.000Z\",
             \"Statement\": {
                \"Sid\": \"AllowFullAccessToBucket\",
                \"Action\": \"s3:*\",
                \"Effect\": \"Allow\",
                \"Resource\": [
                   \"arn:${AWS::Partition}:s3:::my-bucket\",
                   \"arn:${AWS::Partition}:s3:::my-bucket/*\"
               ]
             }
          }"
       },
       "Role": {
         "Fn::Sub": "arn:aws:iam::${AWS::AccountId}:role/Admin"
       },
       "ServerId": {
         "Fn::GetAtt": "Server.ServerId"
       },
       "SshPublicKeys": [
         "ssh-rsa AAAAB3NzaC1yc2EAAAABJQAAAQEAn5ZA7REHaFT40KsZzYnuS7vzdP8n46akEpXLpzrOkbRPEqoOXlDk8f+2SrnANUGfjVVnTqhdrI7S90B4lyBIdWdinhVUK+W0we8j6nCMhtnjigXs6dtxvESUEzrWLWlQpPNJXDSnZEEWoQ/q7W4xXynD6GM3pko36ipA5Xv6hQWC7faYOb2FWLzN1NsngaowO1R6FRau+/oIu"
       ],
       "Tags": [
         {
           "Key": "KeyName",
           "Value": "ValueName"
         }
       ],
       "UserName": "my-user"
     }
}
```

#### YAML<a name="aws-resource-transfer-user--examples--Associate_a_user_with_a_server--yaml"></a>

```
User:
  Type: AWS::Transfer::User
  Properties:
    HomeDirectoryMappings:
      - Entry: /
        Target: /my-bucket/
    HomeDirectoryType: LOGICAL
    Policy:
      Fn::Sub: |
        {
          "Version": "2012-10-17",
          "Statement": {
            "Sid": "AllowFullAccessToBucket",
            "Action": "s3:*",
            "Effect": "Allow",
            "Resource": [
              "arn:aws:s3:::my-bucket",
              "arn:aws:s3:::my-bucket/*"
            ]
          }
        }
    Role:
      Fn::Sub: arn:aws:iam::${AWS::AccountId}:role/Admin
    ServerId:
      Fn::GetAtt: Server.ServerId
    SshPublicKeys:
     - ssh-rsa AAAAB3NzaC1yc2EAAAABJQAAAQEAn5ZA7REHaFT40KsZzYnuS7vzdP8n46akEpXLpzrOkbRPEqoOXlDk8f+2SrnANUGfjVVnTqhdrI7S90B4lyBIdWdinhVUK+W0we8j6nCMhtnjigXs6dtxvESUEzrWLWlQpPNJXDSnZEEWoQ/q7W4xXynD6GM3pko36ipA5Xv6hQWC7faYOb2FWLzN1NsngaowO1R6FRau+/oIu
    Tags:
      - Key: KeyName
        Value: ValueName
    UserName: my-user
```

## See also<a name="aws-resource-transfer-user--seealso"></a>

[CreateUser](https://docs.aws.amazon.com/transfer/latest/userguide/API_CreateUser.html) in the *AWS Transfer Family User Guide*\.