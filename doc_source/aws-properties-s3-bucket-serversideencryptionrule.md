# AWS::S3::Bucket ServerSideEncryptionRule<a name="aws-properties-s3-bucket-serversideencryptionrule"></a>

Specifies the default server\-side encryption configuration\.

## Syntax<a name="aws-properties-s3-bucket-serversideencryptionrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-serversideencryptionrule-syntax.json"></a>

```
{
  "[ServerSideEncryptionByDefault](#cfn-s3-bucket-serversideencryptionrule-serversideencryptionbydefault)" : ServerSideEncryptionByDefault
}
```

### YAML<a name="aws-properties-s3-bucket-serversideencryptionrule-syntax.yaml"></a>

```
  [ServerSideEncryptionByDefault](#cfn-s3-bucket-serversideencryptionrule-serversideencryptionbydefault): 
    ServerSideEncryptionByDefault
```

## Properties<a name="aws-properties-s3-bucket-serversideencryptionrule-properties"></a>

`ServerSideEncryptionByDefault`  <a name="cfn-s3-bucket-serversideencryptionrule-serversideencryptionbydefault"></a>
Specifies the default server\-side encryption to apply to new objects in the bucket\. If a PUT Object request doesn't specify any server\-side encryption, this default encryption will be applied\.  
*Required*: No  
*Type*: [ServerSideEncryptionByDefault](aws-properties-s3-bucket-serversideencryptionbydefault.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)