# AWS::CodeArtifact::Domain<a name="aws-resource-codeartifact-domain"></a>

The `AWS::CodeArtifact::Domain` resource creates an AWS CodeArtifact domain\. CodeArtifact *domains* make it easier to manage multiple repositories across an organization\. You can use a domain to apply permissions across many repositories owned by different AWS accounts\. For more information about domains, see the [Domain concepts information](https://docs.aws.amazon.com/codeartifact/latest/ug/codeartifact-concepts.html#welcome-concepts-domain) in the *CodeArtifact User Guide*\. For more information about the `CreateDomain` API, see [CreateDomain](https://docs.aws.amazon.com/codeartifact/latest/APIReference/API_CreateDomain.html) in the *CodeArtifact API Reference*\.

## Syntax<a name="aws-resource-codeartifact-domain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codeartifact-domain-syntax.json"></a>

```
{
  "Type" : "AWS::CodeArtifact::Domain",
  "Properties" : {
      "[DomainName](#cfn-codeartifact-domain-domainname)" : String,
      "[EncryptionKey](#cfn-codeartifact-domain-encryptionkey)" : String,
      "[PermissionsPolicyDocument](#cfn-codeartifact-domain-permissionspolicydocument)" : Json,
      "[Tags](#cfn-codeartifact-domain-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-codeartifact-domain-syntax.yaml"></a>

```
Type: AWS::CodeArtifact::Domain
Properties: 
  [DomainName](#cfn-codeartifact-domain-domainname): String
  [EncryptionKey](#cfn-codeartifact-domain-encryptionkey): String
  [PermissionsPolicyDocument](#cfn-codeartifact-domain-permissionspolicydocument): Json
  [Tags](#cfn-codeartifact-domain-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-codeartifact-domain-properties"></a>

`DomainName`  <a name="cfn-codeartifact-domain-domainname"></a>
 A string that specifies the name of the requested domain\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `50`  
*Pattern*: `[a-z][a-z0-9\-]{0,48}[a-z0-9]`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EncryptionKey`  <a name="cfn-codeartifact-domain-encryptionkey"></a>
 The key used to encrypt the domain\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1011`  
*Pattern*: `\S+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PermissionsPolicyDocument`  <a name="cfn-codeartifact-domain-permissionspolicydocument"></a>
The document that defines the resource policy that is set on a domain\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-codeartifact-domain-tags"></a>
A list of tags to be applied to the domain\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-codeartifact-domain-return-values"></a>

### Ref<a name="aws-resource-codeartifact-domain-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource arn\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-codeartifact-domain-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-codeartifact-domain-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
When you pass the logical ID of this resource, the function returns the Amazon Resource Name \(ARN\) of the domain\. 

`EncryptionKey`  <a name="EncryptionKey-fn::getatt"></a>
When you pass the logical ID of this resource, the function returns the key used to encrypt the domain\.

`Name`  <a name="Name-fn::getatt"></a>
When you pass the logical ID of this resource, the function returns the name of the domain\.

`Owner`  <a name="Owner-fn::getatt"></a>
When you pass the logical ID of this resource, the function returns the 12\-digit account number of the AWS account that owns the domain\.

## Examples<a name="aws-resource-codeartifact-domain--examples"></a>

The following examples can help you create CodeArtifact domains using CloudFormation\.

### Create a domain<a name="aws-resource-codeartifact-domain--examples--Create_a_domain"></a>

The following example creates a CodeArtifact domain named *my\-domain*\.

#### YAML<a name="aws-resource-codeartifact-domain--examples--Create_a_domain--yaml"></a>

```
Resources:
  MyCodeArtifactDomain:
    Type: 'AWS::CodeArtifact::Domain'
    Properties:
      DomainName: "my-domain"
```

#### JSON<a name="aws-resource-codeartifact-domain--examples--Create_a_domain--json"></a>

```
{
  "Resources": {
    "MyCodeArtifactDomain": {
      "Type": "AWS::CodeArtifact::Domain",
      "Properties": {
        "DomainName": "my-domain"
      }
    }
  }
}
```

### Create a domain with an attached AWS KMS encryption key and IAM permissions policy<a name="aws-resource-codeartifact-domain--examples--Create_a_domain_with_an_attached_AWS_KMS_encryption_key_and_IAM_permissions_policy"></a>

The following example creates a CodeArtifact domain named *my\-domain* and attaches an AWS KMS encryption key and IAM permissions policy\.

#### YAML<a name="aws-resource-codeartifact-domain--examples--Create_a_domain_with_an_attached_AWS_KMS_encryption_key_and_IAM_permissions_policy--yaml"></a>

```
Resources:
  MyCodeArtifactDomain:
    Type: 'AWS::CodeArtifact::Domain'
    Properties:
      DomainName: "my-domain"
      EncryptionKey: arn:aws:kms:us-west-2:123456789012:key/12345678-9abc-def1-2345-6789abcdef12
      PermissionsPolicyDocument:
          Version: 2012-10-17
          Statement:
            - Action:
                - codeartifact:ReadFromRepository
                - codeartifact:DescribePackageVersion
                - codeartifact:DescribeRepository
                - codeartifact:GetPackageVersionReadme
                - codeartifact:GetRepositoryEndpoint
                - codeartifact:ListPackageVersionAssets
                - codeartifact:ListPackageVersionDependencies
                - codeartifact:ListPackageVersions
                - codeartifact:ListPackages
                - codeartifact:ReadFromRepository
              Effect: Allow
              Principal:
                AWS: "arn:aws:iam::123456789012:root"
              Resource: "*"
```

#### JSON<a name="aws-resource-codeartifact-domain--examples--Create_a_domain_with_an_attached_AWS_KMS_encryption_key_and_IAM_permissions_policy--json"></a>

```
{
  "Resources": {
    "MyCodeArtifactDomain": {
      "Type": "AWS::CodeArtifact::Domain",
      "Properties": {
        "DomainName": "my-domain",
        "EncryptionKey": "arn:aws:kms:us-west-2:123456789012:key/12345678-9abc-def1-2345-6789abcdef12",
        "PermissionsPolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Action": [
                "codeartifact:ReadFromRepository",
                "codeartifact:DescribePackageVersion",
                "codeartifact:DescribeRepository",
                "codeartifact:GetPackageVersionReadme",
                "codeartifact:GetRepositoryEndpoint",
                "codeartifact:ListPackageVersionAssets",
                "codeartifact:ListPackageVersionDependencies",
                "codeartifact:ListPackageVersions",
                "codeartifact:ListPackages",
                "codeartifact:ReadFromRepository"
              ],
              "Effect": "Allow",
              "Principal": {
                "AWS": "arn:aws:iam::123456789012:root"
              },
              "Resource": "*"
            }
          ]
        }
      }
    }
  }
}
```