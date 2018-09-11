# Metadata Attribute<a name="aws-attribute-metadata"></a>

The Metadata attribute enables you to associate structured data with a resource\. By adding a Metadata attribute to a resource, you can add data in JSON or YAML to the resource declaration\. In addition, you can use intrinsic functions \(such as [GetAtt](intrinsic-function-reference-getatt.md) and [Ref](intrinsic-function-reference-ref.md)\), parameters, and pseudo parameters within the Metadata attribute to add those interpreted values\.

**Note**  
AWS CloudFormation does not validate the syntax within the Metadata attribute\.

You can retrieve this data using the AWS command [http://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-resource.html](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stack-resource.html) or the [DescribeStackResource action](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeStackResource.html)\.

## Example<a name="w3ab2c21c23c19b9"></a>

The following template contains an Amazon S3 bucket resource with a Metadata attribute\.

### JSON<a name="aws-attribute-metadata-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Resources" : {
      "MyS3Bucket" : {
         "Type" : "AWS::S3::Bucket",
         "Metadata" : { "Object1" : "Location1",  "Object2" : "Location2" }
      }
   }
}
```

### YAML<a name="aws-attribute-metadata-example.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  MyS3Bucket:
    Type: AWS::S3::Bucket
    Metadata:
      Object1: Location1
      Object2: Location2
```