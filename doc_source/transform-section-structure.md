# Transform<a name="transform-section-structure"></a>

The optional `Transform` section specifies one or more transforms that AWS CloudFormation uses to process your template\. The `Transform` section builds on the simple, declarative language of AWS CloudFormation with a powerful macro system\.

AWS CloudFormation transforms help simplify template authoring by condensing the expression of AWS infrastructure as code and enabling reuse of template components\. For example, you can condense a multiple\-line resource declaration into a single line in your template\.

AWS CloudFormation supports `AWS::Serverless` and `AWS::Include` transform types:
+ An `AWS::Serverless` transform specifies the version of the AWS Serverless Application Model \(AWS SAM\) to use\. This model defines the AWS SAM syntax that you can use and how AWS CloudFormation processes it\. When you create a change set, AWS CloudFormation resolves all `Transform` functions\. For more information about serverless applications and AWS SAM, see [Deploying Lambda\-based Applications](http://docs.aws.amazon.com/lambda/latest/dg/deploying-lambda-apps.html) in the *AWS Lambda Developer Guide*\.
+ An `AWS::Include` transform works with template snippets that are stored separately from the main AWS CloudFormation template\. You can insert these snippets into your main template when [Creating a Change Set](using-cfn-updating-stacks-changesets-create.md) or [Updating Stacks Using Change Sets](using-cfn-updating-stacks-changesets.md)\.

You can declare a single transform or multiple transforms within a template\. AWS CloudFormation executes transformations in the order that they are specified\.

To declare multiple transforms, use a list format and specify one or more `AWS::Include` transforms and \(optionally\) an `AWS::Serverless` transform\. The following example declares two `AWS::Include` transforms\.

## JSON<a name="transform-section-example.json"></a>

```
{
  "Resources": {
    "MyBucket": {
      "Type": "AWS::S3::Bucket",
      "Properties": {
        "Fn::Transform": [
          {
            "Name": "AWS::Include",
            "Parameters": {
              "Location": "s3://bucket/myBucketName.json"
            }
          },
          {
            "Name": "AWS::Include",
            "Parameters": {
              "Location": "s3://bucket/myBucketAcl.json"
            }
          }
        ]
      }
    }
  }
}
```

## YAML<a name="transform-section-example.yaml"></a>

```
Resources:
  MyBucket:
    Type: 'AWS::S3::Bucket'
    Properties:
        'Fn::Transform':
            - Name: 'AWS::Include'
              Parameters:
                Location: s3://bucket/myBucketName.yaml
            - Name: 'AWS::Include'
              Parameters:
                Location: s3://bucket/myBucketAcl.yaml
```

For more information and example transforms, see the following topics:

**Topics**
+ [JSON](#transform-section-example.json)
+ [YAML](#transform-section-example.yaml)
+ [AWS::Serverless Transform](transform-aws-serverless.md)
+ [AWS::Include Transform](create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform.md)