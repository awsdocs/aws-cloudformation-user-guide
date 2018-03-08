# AWS CloudFormation Resource Specification<a name="cfn-resource-specification"></a>

The AWS CloudFormation resource specification is a JSON\-formatted text file that defines the resources and properties that AWS CloudFormation supports\. The document is a machine\-readable, strongly typed specification that you can use to build tools for creating AWS CloudFormation templates\. For example, you can use the specification to build auto completion and validation functionality for AWS CloudFormation templates in your IDE \(integrated development environment\)\.

The resource specification is organized as both a single file and as a series of files, where each file contains the definition of one resource type\. The single and separated files contain identical information\. Depending on the tool and your implementation, use the file or files that work for you\.

To download the resource specification, see the following table\. 

Resource availability may vary by region\. To check the availability of a resource in a given region, refer to the resource specification for that region\.


**Resource Specification**  

|  Region  |  Single File  |  All Files  | 
| --- | --- | --- | 
|  Asia Pacific \(Mumbai\) Region  |  [CloudFormationResourceSpecification\.json](https://d2senuesg1djtx.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d2senuesg1djtx.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Seoul\) Region  |  [CloudFormationResourceSpecification\.json](https://d1ane3fvebulky.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d1ane3fvebulky.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Sydney\) Region  |  [CloudFormationResourceSpecification\.json](https://d2stg8d246z9di.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d2stg8d246z9di.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Singapore\) Region  |  [CloudFormationResourceSpecification\.json](https://doigdx0kgq9el.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://doigdx0kgq9el.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Asia Pacific \(Tokyo\) Region  |  [CloudFormationResourceSpecification\.json](https://d33vqc0rt9ld30.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d33vqc0rt9ld30.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  Canada \(Central\) Region  |  [CloudFormationResourceSpecification\.json](https://d2s8ygphhesbe7.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d2s8ygphhesbe7.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  EU \(Frankfurt\) Region  |  [CloudFormationResourceSpecification\.json](https://d1mta8qj7i28i2.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d1mta8qj7i28i2.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  EU \(London\) Region  |  [CloudFormationResourceSpecification\.json](https://d1742qcu2c1ncx.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d1742qcu2c1ncx.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  EU \(Ireland\) Region  |  [CloudFormationResourceSpecification\.json](https://d3teyb21fexa9r.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d3teyb21fexa9r.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  South America \(São Paulo\)  |  [CloudFormationResourceSpecification\.json](https://d3c9jyj3w509b0.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d3c9jyj3w509b0.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  US East \(N\. Virginia\)  |  [CloudFormationResourceSpecification\.json](https://d1uauaxba7bl26.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d1uauaxba7bl26.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  US East \(Ohio\)  |  [CloudFormationResourceSpecification\.json](https://dnwj8swjjbsbt.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://dnwj8swjjbsbt.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  US West \(N\. California\)  |  [CloudFormationResourceSpecification\.json](https://d68hl49wbnanq.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d68hl49wbnanq.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 
|  US West \(Oregon\)  |  [CloudFormationResourceSpecification\.json](https://d201a2mn26r7lk.cloudfront.net/latest/gzip/CloudFormationResourceSpecification.json)  |  [CloudFormationResourceSpecification\.zip](https://d201a2mn26r7lk.cloudfront.net/latest/CloudFormationResourceSpecification.zip)  | 

The following example shows the specification for an AWS Key Management Service key resource \(`AWS::KMS::Key`\)\. It shows the properties for the `AWS::KMS::Key` resource, which properties are required, the type of allowed value for each property, and their update behavior\. For details about the specification, see [Specification Format](cfn-resource-specification-format.md)\.

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