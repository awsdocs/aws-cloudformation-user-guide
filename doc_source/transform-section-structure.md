# Transform<a name="transform-section-structure"></a>

The optional `Transform` section specifies one or more macros that AWS CloudFormation uses to process your template\. The `Transform` section builds on the simple, declarative language of AWS CloudFormation with a powerful macro system\. 

You can declare one or more macros within a template\. AWS CloudFormation executes macros in the order that they are specified\. When you create a change set, AWS CloudFormation generates a change set that includes the processed template content\. You can then review the changes and execute the change set\. For more information, see [Using AWS CloudFormation macros to perform custom processing on templates](template-macros.md)\.

AWS CloudFormation also supports *transforms*, which are macros hosted by AWS CloudFormation\. AWS CloudFormation treats these transforms the same as any macros you create in terms of execution order and scope\. For detailed information regarding specific transforms, see [Transform reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-reference.html)\. 

To declare multiple macros, use a list format and specify one or more macros\.

For example, in the template sample below, AWS CloudFormation evaluates `MyMacro` and then `AWS::Serverless`, both of which can process the contents of the entire template because of their inclusion in the `Transform` section\.

```
// Start of processable content for MyMacro and AWS::Serverless
Transform:
  - MyMacro
  - 'AWS::Serverless'
Resources:
  WaitCondition:
    Type: 'AWS::CloudFormation::WaitCondition'
  MyBucket:
    Type: 'AWS::S3::Bucket'
    Properties: 
        BucketName: MyBucket 
        Tags: [{"key":"value"}] 
        CorsConfiguration:[] 
  MyEc2Instance:
    Type: 'AWS::EC2::Instance' 
    Properties:
        ImageID: "ami-123"
// End of processable content for MyMacro and AWS::Serverless
```