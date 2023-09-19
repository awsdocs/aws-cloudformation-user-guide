# AWS::Transfer::Connector SftpConfig<a name="aws-properties-transfer-connector-sftpconfig"></a>

A structure that contains the parameters for an SFTP connector object\.

## Syntax<a name="aws-properties-transfer-connector-sftpconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-connector-sftpconfig-syntax.json"></a>

```
{
  "[TrustedHostKeys](#cfn-transfer-connector-sftpconfig-trustedhostkeys)" : [ String, ... ],
  "[UserSecretId](#cfn-transfer-connector-sftpconfig-usersecretid)" : String
}
```

### YAML<a name="aws-properties-transfer-connector-sftpconfig-syntax.yaml"></a>

```
  [TrustedHostKeys](#cfn-transfer-connector-sftpconfig-trustedhostkeys): 
    - String
  [UserSecretId](#cfn-transfer-connector-sftpconfig-usersecretid): String
```

## Properties<a name="aws-properties-transfer-connector-sftpconfig-properties"></a>

`TrustedHostKeys`  <a name="cfn-transfer-connector-sftpconfig-trustedhostkeys"></a>
The public portion of the host key, or keys, that are used to authenticate the user to the external server to which you are connecting\. You can use the `ssh-keyscan` command against the SFTP server to retrieve the necessary key\.  
The three standard SSH public key format elements are `<key type>`, `<body base64>`, and an optional `<comment>`, with spaces between each element\. Specify only the `<key type>` and `<body base64>`: do not enter the `<comment>` portion of the key\.  
For the trusted host key, AWS Transfer Family accepts RSA and ECDSA keys\.  
+ For RSA keys, the key type is `ssh-rsa`\.
+ For ECDSA keys, the key type is either `ecdsa-sha2-nistp256`, `ecdsa-sha2-nistp384`, or `ecdsa-sha2-nistp521`, depending on the size of the key you generated\.
*Required*: No  
*Type*: List of String  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UserSecretId`  <a name="cfn-transfer-connector-sftpconfig-usersecretid"></a>
The identifier for the secret \(in AWS Secrets Manager\) that contains the SFTP user's private key, password, or both\. The identifier can be either the Amazon Resource Name \(ARN\) or the name of the secret\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)