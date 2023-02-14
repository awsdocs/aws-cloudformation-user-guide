# AWS::S3::Bucket OwnershipControlsRule<a name="aws-properties-s3-bucket-ownershipcontrolsrule"></a>

Specifies an Object Ownership rule\.

S3 Object Ownership is an Amazon S3 bucket\-level setting that you can use to disable access control lists \(ACLs\) and take ownership of every object in your bucket, simplifying access management for data stored in Amazon S3\. For more information, see [Controlling ownership of objects and disabling ACLs](https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html) in the *Amazon S3 User Guide*\. 

## Syntax<a name="aws-properties-s3-bucket-ownershipcontrolsrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-ownershipcontrolsrule-syntax.json"></a>

```
{
  "[ObjectOwnership](#cfn-s3-bucket-ownershipcontrolsrule-objectownership)" : String
}
```

### YAML<a name="aws-properties-s3-bucket-ownershipcontrolsrule-syntax.yaml"></a>

```
  [ObjectOwnership](#cfn-s3-bucket-ownershipcontrolsrule-objectownership): String
```

## Properties<a name="aws-properties-s3-bucket-ownershipcontrolsrule-properties"></a>

`ObjectOwnership`  <a name="cfn-s3-bucket-ownershipcontrolsrule-objectownership"></a>
Specifies an Object Ownership rule\.  
*Allowed values*: `BucketOwnerEnforced` \| `ObjectWriter` \| `BucketOwnerPreferred`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples"></a>



### Object Ownership \- BucketOwnerEnforced<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples--Object_Ownership_-_BucketOwnerEnforced"></a>

The following examples show Object Ownership set to `BucketOwnerEnforced`\.

#### JSON<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples--Object_Ownership_-_BucketOwnerEnforced--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "OwnershipControls": {
                    "Rules": [
                        {
                            "ObjectOwnership": "BucketOwnerEnforced"
                        }
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples--Object_Ownership_-_BucketOwnerEnforced--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      OwnershipControls:
        Rules:
          - ObjectOwnership: BucketOwnerEnforced
```

### Object Ownership \- BucketOwnerPreferred<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples--Object_Ownership_-_BucketOwnerPreferred"></a>

The following examples show Object Ownership set to `BucketOwnerPreferred`\.

#### JSON<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples--Object_Ownership_-_BucketOwnerPreferred--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "S3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "OwnershipControls": {
                    "Rules": [
                        {
                            "ObjectOwnership": "BucketOwnerPreferred"
                        }
                    ]
                }
            }
        }
    }
}
```

#### YAML<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples--Object_Ownership_-_BucketOwnerPreferred--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  S3Bucket:
    Type: 'AWS::S3::Bucket'
    Properties:
      OwnershipControls:
        Rules:
          - ObjectOwnership: BucketOwnerPreferred
```