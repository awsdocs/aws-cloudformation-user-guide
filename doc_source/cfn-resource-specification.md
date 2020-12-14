# AWS CloudFormation resource specification<a name="cfn-resource-specification"></a>

The AWS CloudFormation resource specification is a JSON\-formatted text file that defines the resources and properties that AWS CloudFormation supports\. The document is a machine\-readable, strongly typed specification that you can use to build tools for creating AWS CloudFormation templates\. For example, you can use the specification to build auto completion and validation functionality for AWS CloudFormation templates in your IDE \(integrated development environment\)\.

The resource specification is organized as both a single file and as a series of files, where each file contains the definition of one resource type\. The single and separated files contain identical information\. Depending on the tool and your implementation, use the file or files that work for you\.

To download the resource specification, see the following table\. 

Resource availability may vary by region\. To check the availability of a resource in a given region, refer to the resource specification for that region\.


**Resource specification**  

|  Region name  |  Region  |  Single file  |  All files  | 
| --- | --- | --- | --- | 
|  US East \(Ohio\)  |  us\-east\-2  |  [\.json](https://dnwj8swjjbsbt.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://dnwj8swjjbsbt.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  US East \(N\. Virginia\)  |  us\-east\-1  |  [\.json](https://d1uauaxba7bl26.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d1uauaxba7bl26.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  US West \(N\. California\)  |  us\-west\-1  |  [\.json](https://d68hl49wbnanq.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d68hl49wbnanq.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  US West \(Oregon\)  |  us\-west\-2  |  [\.json](https://d201a2mn26r7lk.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d201a2mn26r7lk.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Africa \(Cape Town\)  |  af\-south\-1  |  [\.json](https://cfn-resource-specifications-af-south-1-prod.s3.af-south-1.amazonaws.com/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://cfn-resource-specifications-af-south-1-prod.s3.af-south-1.amazonaws.com/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Hong Kong\)  |  ap\-east\-1  |  [\.json](https://cfn-resource-specifications-ap-east-1-prod.s3.ap-east-1.amazonaws.com/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://cfn-resource-specifications-ap-east-1-prod.s3.ap-east-1.amazonaws.com/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Mumbai\)  |  ap\-south\-1  |  [\.json](https://d2senuesg1djtx.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d2senuesg1djtx.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Osaka\-Local\)  |  ap\-northeast\-3  |  [\.json](https://d2zq80gdmjim8k.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d2zq80gdmjim8k.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Seoul\)  |  ap\-northeast\-2  |  [\.json](https://d1ane3fvebulky.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d1ane3fvebulky.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Singapore\)  |  ap\-southeast\-1  |  [\.json](https://doigdx0kgq9el.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://doigdx0kgq9el.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Sydney\)  |  ap\-southeast\-2  |  [\.json](https://d2stg8d246z9di.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d2stg8d246z9di.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Tokyo\)  |  ap\-northeast\-1  |  [\.json](https://d33vqc0rt9ld30.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d33vqc0rt9ld30.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Canada \(Central\)  |  ca\-central\-1  |  [\.json](https://d2s8ygphhesbe7.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d2s8ygphhesbe7.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  China \(Beijing\)  |  cn\-north\-1  |  [\.json](https://cfn-resource-specifications-cn-north-1-prod.s3.cn-north-1.amazonaws.com.cn/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://cfn-resource-specifications-cn-north-1-prod.s3.cn-north-1.amazonaws.com.cn/latest/CloudFormationResourceSpecification.zip)  | 
|  China \(Ningxia\)  |  cn\-northwest\-1  |  [\.json](https://cfn-resource-specifications-cn-northwest-1-prod.s3.cn-northwest-1.amazonaws.com.cn/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://cfn-resource-specifications-cn-northwest-1-prod.s3.cn-northwest-1.amazonaws.com.cn/latest/CloudFormationResourceSpecification.zip)  | 
|  Europe \(Frankfurt\)  |  eu\-central\-1  |  [\.json](https://d1mta8qj7i28i2.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d1mta8qj7i28i2.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Europe \(Ireland\)  |  eu\-west\-1  |  [\.json](https://d3teyb21fexa9r.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d3teyb21fexa9r.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Europe \(London\)  |  eu\-west\-2  |  [\.json](https://d1742qcu2c1ncx.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d1742qcu2c1ncx.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Europe \(Paris\)  |  eu\-west\-3  |  [\.json](https://d2d0mfegowb3wk.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d2d0mfegowb3wk.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Europe \(Stockholm\)  |  eu\-north\-1  |  [\.json](https://diy8iv58sj6ba.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://diy8iv58sj6ba.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Europe \(Milan\)  |  eu\-south\-1  |  [\.json](https://cfn-resource-specifications-eu-south-1-prod.s3.eu-south-1.amazonaws.com/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://cfn-resource-specifications-eu-south-1-prod.s3.eu-south-1.amazonaws.com/latest/CloudFormationResourceSpecification.zip)  | 
|  Middle East \(Bahrain\)  |  me\-south\-1  |  [\.json](https://cfn-resource-specifications-me-south-1-prod.s3.me-south-1.amazonaws.com/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://cfn-resource-specifications-me-south-1-prod.s3.me-south-1.amazonaws.com/latest/CloudFormationResourceSpecification.zip)  | 
|  South America \(São Paulo\)  |  sa\-east\-1  |  [\.json](https://d3c9jyj3w509b0.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [\.zip](https://d3c9jyj3w509b0.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  AWS GovCloud \(US\-East\)  |  us\-gov\-east\-1  |  [\.json](https://s3.us-gov-east-1.amazonaws.com/cfn-resource-specifications-us-gov-east-1-prod/latest/CloudFormationResourceSpecification.json)  |  [\.zip](https://s3.us-gov-east-1.amazonaws.com/cfn-resource-specifications-us-gov-east-1-prod/latest/CloudFormationResourceSpecification.zip)  | 
|  AWS GovCloud \(US\-West\)  |  us\-gov\-west\-1  |  [\.json](https://s3.us-gov-west-1.amazonaws.com/cfn-resource-specifications-us-gov-west-1-prod/latest/CloudFormationResourceSpecification.json)  |  [\.zip](https://s3.us-gov-west-1.amazonaws.com/cfn-resource-specifications-us-gov-west-1-prod/latest/CloudFormationResourceSpecification.zip)  | 

The following example shows the specification for an AWS Key Management Service key resource \(`AWS::KMS::Key`\)\. It shows the properties for the `AWS::KMS::Key` resource, which properties are required, the type of allowed value for each property, and their update behavior\. For details about the specification, see [Specification format](cfn-resource-specification-format.md)\.

```
    "AWS::KMS::Key": {
      "Attributes": {
        "Arn": {
          "PrimitiveType": "String"
        }
      },
      "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html",
      "Properties": {
        "Description": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html#cfn-kms-key-description",
          "PrimitiveType": "String",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "EnableKeyRotation": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html#cfn-kms-key-enablekeyrotation",
          "PrimitiveType": "Boolean",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "Enabled": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html#cfn-kms-key-enabled",
          "PrimitiveType": "Boolean",
          "Required": false,
          "UpdateType": "Mutable"
        },
        "KeyPolicy": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html#cfn-kms-key-keypolicy",
          "PrimitiveType": "Json",
          "Required": true,
          "UpdateType": "Mutable"
        },
        "KeyUsage": {
          "Documentation": "http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html#cfn-kms-key-keyusage",
          "PrimitiveType": "String",
          "Required": false,
          "UpdateType": "Immutable"
        }
      }
    }
```