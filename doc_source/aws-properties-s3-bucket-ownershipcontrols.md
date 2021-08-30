# AWS::S3::Bucket OwnershipControls<a name="aws-properties-s3-bucket-ownershipcontrols"></a>

Specifies the container element for object ownership rules\.

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
Specifies the container element for object ownership rules\.  
*Required*: Yes  
*Type*: List of [OwnershipControlsRule](aws-properties-s3-bucket-ownershipcontrolsrule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-s3-bucket-ownershipcontrols--examples"></a>



### Object ownership<a name="aws-properties-s3-bucket-ownershipcontrols--examples--Object_ownership"></a>

The following examples show object ownership set to `BucketOwnerPreferred`\.

#### JSON<a name="aws-properties-s3-bucket-ownershipcontrols--examples--Object_ownership--json"></a>

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

#### YAML<a name="aws-properties-s3-bucket-ownershipcontrols--examples--Object_ownership--yaml"></a>

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