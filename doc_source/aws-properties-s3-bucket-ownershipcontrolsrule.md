# AWS::S3::Bucket OwnershipControlsRule<a name="aws-properties-s3-bucket-ownershipcontrolsrule"></a>

Specifies an object ownership rule\. Object Ownership is an Amazon S3 bucket setting that you can use to control ownership of new objects that are uploaded to your buckets see [Controlling object ownership](https://docs.aws.amazon.com/AmazonS3/latest/userguide/about-object-ownership.html) in the *Amazon S3 User Guide* for more information\. 

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
Specifies an object ownership rule\.  
*Allowed values*: `ObjectWriter` \| `BucketOwnerPreferred`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples"></a>



### Object ownership<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples--Object_ownership"></a>

The following examples show object ownership set to `BucketOwnerPreferred`\.

#### JSON<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples--Object_ownership--json"></a>

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

#### YAML<a name="aws-properties-s3-bucket-ownershipcontrolsrule--examples--Object_ownership--yaml"></a>

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