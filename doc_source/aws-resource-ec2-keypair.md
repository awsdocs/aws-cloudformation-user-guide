# AWS::EC2::KeyPair<a name="aws-resource-ec2-keypair"></a>

Specifies a key pair for use with an Amazon Elastic Compute Cloud instance as follows:
+ To import an existing key pair, include the `PublicKeyMaterial` property\.
+ To create a new key pair, omit the `PublicKeyMaterial` property\.

When you import an existing key pair, you specify the public key material for the key\. We assume that you have the private key material for the key\. AWS CloudFormation does not create or return the private key material when you import a key pair\.

When you create a new key pair, the private key is saved to AWS Systems Manager Parameter Store, using a parameter with the following name: `/ec2/keypair/{key_pair_id}`\. For more information about retrieving private key, and the required permissions, see [Create a key pair using AWS CloudFormation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/create-key-pairs.html#create-key-pair-cloudformation) in the *Amazon EC2 User Guide*\.

When AWS CloudFormation deletes a key pair that was created or imported by a stack, it also deletes the parameter that was used to store the private key material in Parameter Store\.

## Syntax<a name="aws-resource-ec2-keypair-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-keypair-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::KeyPair",
  "Properties" : {
      "[KeyName](#cfn-ec2-keypair-keyname)" : String,
      "[KeyType](#cfn-ec2-keypair-keytype)" : String,
      "[PublicKeyMaterial](#cfn-ec2-keypair-publickeymaterial)" : String,
      "[Tags](#cfn-ec2-keypair-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ec2-keypair-syntax.yaml"></a>

```
Type: AWS::EC2::KeyPair
Properties: 
  [KeyName](#cfn-ec2-keypair-keyname): String
  [KeyType](#cfn-ec2-keypair-keytype): String
  [PublicKeyMaterial](#cfn-ec2-keypair-publickeymaterial): String
  [Tags](#cfn-ec2-keypair-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ec2-keypair-properties"></a>

`KeyName`  <a name="cfn-ec2-keypair-keyname"></a>
A unique name for the key pair\.  
Constraints: Up to 255 ASCII characters  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyType`  <a name="cfn-ec2-keypair-keytype"></a>
The type of key pair\. Note that ED25519 keys are not supported for Windows instances\.  
If the `PublicKeyMaterial` property is specified, the `KeyType` property is ignored, and the key type is inferred from the `PublicKeyMaterial` value\.  
Default: `rsa`   
*Required*: No  
*Type*: String  
*Allowed values*: `ed25519 | rsa`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PublicKeyMaterial`  <a name="cfn-ec2-keypair-publickeymaterial"></a>
The public key material\. The `PublicKeyMaterial` property is used to import a key pair\. If this property is not specified, then a new key pair will be created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ec2-keypair-tags"></a>
The tags to apply to the key pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ec2-keypair-return-values"></a>

### Ref<a name="aws-resource-ec2-keypair-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the key pair\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-keypair-return-values-fn--getatt"></a>

#### <a name="aws-resource-ec2-keypair-return-values-fn--getatt-fn--getatt"></a>

`KeyFingerprint`  <a name="KeyFingerprint-fn::getatt"></a>
If you created the key pair using Amazon EC2:  
+ For RSA key pairs, the key fingerprint is the SHA\-1 digest of the DER encoded private key\.
+ For ED25519 key pairs, the key fingerprint is the base64\-encoded SHA\-256 digest, which is the default for OpenSSH, starting with [OpenSSH 6\.8](http://www.openssh.com/txt/release-6.8)\.
If you imported the key pair to Amazon EC2:  
+ For RSA key pairs, the key fingerprint is the MD5 public key fingerprint as specified in section 4 of RFC 4716\.
+ For ED25519 key pairs, the key fingerprint is the base64\-encoded SHA\-256 digest, which is the default for OpenSSH, starting with [OpenSSH 6\.8](http://www.openssh.com/txt/release-6.8)\.

`KeyPairId`  <a name="KeyPairId-fn::getatt"></a>
The ID of the key pair\.

## Examples<a name="aws-resource-ec2-keypair--examples"></a>

### Create a new key pair and specify it when launching an instance<a name="aws-resource-ec2-keypair--examples--Create_a_new_key_pair_and_specify_it_when_launching_an_instance"></a>

The following example omits the `PublicKeyMaterial` property to create a new key pair, and specifies the key pair when launching an instance\.

#### JSON<a name="aws-resource-ec2-keypair--examples--Create_a_new_key_pair_and_specify_it_when_launching_an_instance--json"></a>

```
{
    "Resources": {
        "NewKeyPair": {
            "Type": "AWS::EC2::KeyPair",
            "Properties": {
                "KeyName": "MyKeyPair"
            }
        },
        "Ec2Instance": {
            "Type": "AWS::EC2::Instance",
            "Properties": {
                "ImageId": "ami-02b92c281a4d3dc79",
                "KeyName": {
                    "Ref": "NewKeyPair"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ec2-keypair--examples--Create_a_new_key_pair_and_specify_it_when_launching_an_instance--yaml"></a>

```
Resources:
  NewKeyPair:
    Type: 'AWS::EC2::KeyPair'
    Properties:
      KeyName: MyKeyPair
  Ec2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      ImageId: ami-02b92c281a4d3dc79
      KeyName: !Ref NewKeyPair
```

### Import an existing key pair and specify it when launching an instance<a name="aws-resource-ec2-keypair--examples--Import_an_existing_key_pair_and_specify_it_when_launching_an_instance"></a>

The following example uses the `PublicKeyMaterial` property to import an existing key pair, and specifies the key pair when launching an instance\.

#### JSON<a name="aws-resource-ec2-keypair--examples--Import_an_existing_key_pair_and_specify_it_when_launching_an_instance--json"></a>

```
{
    "Resources": {
        "ImportedKeyPair": {
            "Type": "AWS::EC2::KeyPair",
            "Properties": {
                "KeyName": "NameForMyImportedKeyPair",
                "PublicKeyMaterial": "ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAICfp1F7DhdWZdqkYAUGCzcBsLmJeu9izpIyGpmmg7eCz example"
            }
        },
        "Ec2Instance": {
            "Type": "AWS::EC2::Instance",
            "Properties": {
                "ImageId": "ami-02b92c281a4d3dc79",
                "KeyName": {
                    "Ref": "ImportedKeyPair"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ec2-keypair--examples--Import_an_existing_key_pair_and_specify_it_when_launching_an_instance--yaml"></a>

```
Resources:
  ImportedKeyPair:
    Type: AWS::EC2::KeyPair
    Properties:
      KeyName: NameForMyImportedKeyPair
      PublicKeyMaterial: ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAICfp1F7DhdWZdqkYAUGCzcBsLmJeu9izpIyGpmmg7eCz example
  Ec2Instance: 
    Type: AWS::EC2::Instance
    Properties: 
      ImageId: ami-02b92c281a4d3dc79
      KeyName: 
        Ref: ImportedKeyPair
```

## See also<a name="aws-resource-ec2-keypair--seealso"></a>
+  [CreateKeyPair](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateKeyPair.html) in the *Amazon EC2 API Reference* 
+  [ImportKeyPair](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ImportKeyPair.html) in the *Amazon EC2 API Reference* 
+  [Amazon EC2 key pairs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html) in the *Amazon EC2 User Guide for Linux Instances* 
+  [Amazon EC2 key pairs](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/ec2-key-pairs.html) in the *Amazon EC2 User Guide for Windows Instances* 