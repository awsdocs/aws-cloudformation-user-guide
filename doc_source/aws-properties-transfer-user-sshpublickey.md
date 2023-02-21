# AWS::Transfer::User SshPublicKey<a name="aws-properties-transfer-user-sshpublickey"></a>

Provides information about the public Secure Shell \(SSH\) key that is associated with a Transfer Family user account for the specific file transfer protocol\-enabled server \(as identified by `ServerId`\)\. The information returned includes the date the key was imported, the public key contents, and the public key ID\. A user can store more than one SSH public key associated with their user name on a specific server\.

**SshPublicKeyBody**

Specifies the content of the SSH public key as specified by the `PublicKeyId`\.

AWS Transfer Family accepts RSA, ECDSA, and ED25519 keys\.

Type: String

Length Constraints: Maximum length of 2048\.

Required: Yes

## See also<a name="aws-properties-transfer-user-sshpublickey--seealso"></a>

[SshPublicKey](https://docs.aws.amazon.com/transfer/latest/userguide/API_SshPublicKey.html) in the *AWS Transfer Family User Guide*\.