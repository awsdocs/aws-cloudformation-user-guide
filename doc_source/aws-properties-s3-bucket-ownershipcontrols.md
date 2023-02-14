# AWS::S3::Bucket OwnershipControls<a name="aws-properties-s3-bucket-ownershipcontrols"></a>

Specifies the container element for Object Ownership rules\.

S3 Object Ownership is an Amazon S3 bucket\-level setting that you can use to disable access control lists \(ACLs\) and take ownership of every object in your bucket, simplifying access management for data stored in Amazon S3\. For more information, see [Controlling ownership of objects and disabling ACLs](https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html) in the *Amazon S3 User Guide*\. 

## Syntax<a name="aws-properties-s3-bucket-ownershipcontrols-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-s3-bucket-ownershipcontrols-syntax.json"></a>

```
{
  "[Rules](#cfn-s3-bucket-ownershipcontrols-rules)" : [ OwnershipControlsRule, ... ]
}
```

### YAML<a name="aws-properties-s3-bucket-ownershipcontrols-syntax.yaml"></a>

```
  [Rules](#cfn-s3-bucket-ownershipcontrols-rules): 
    - OwnershipControlsRule
```

## Properties<a name="aws-properties-s3-bucket-ownershipcontrols-properties"></a>

`Rules`  <a name="cfn-s3-bucket-ownershipcontrols-rules"></a>
Specifies the container element for Object Ownership rules\.  
*Required*: Yes  
*Type*: List of [OwnershipControlsRule](aws-properties-s3-bucket-ownershipcontrolsrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-ownershipcontrols--examples"></a>



### Object ownership \- BucketOwnerEnforced<a name="aws-properties-s3-bucket-ownershipcontrols--examples--Object_ownership_-_BucketOwnerEnforced"></a>

The following examples show Object Ownership set to `BucketOwnerEnforced`\.

#### JSON<a name="aws-properties-s3-bucket-ownershipcontrols--examples--Object_ownership_-_BucketOwnerEnforced--json"></a>

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

#### YAML<a name="aws-properties-s3-bucket-ownershipcontrols--examples--Object_ownership_-_BucketOwnerEnforced--yaml"></a>

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

### Object Ownership \- BucketOwnerPreferred<a name="aws-properties-s3-bucket-ownershipcontrols--examples--Object_Ownership_-_BucketOwnerPreferred"></a>

The following examples show Object Ownership set to `BucketOwnerPreferred`\.

#### JSON<a name="aws-properties-s3-bucket-ownershipcontrols--examples--Object_Ownership_-_BucketOwnerPreferred--json"></a>

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

#### YAML<a name="aws-properties-s3-bucket-ownershipcontrols--examples--Object_Ownership_-_BucketOwnerPreferred--yaml"></a>

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