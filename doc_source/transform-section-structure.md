# Transform<a name="transform-section-structure"></a>

The optional `Transform` section specifies one or more macros that AWS CloudFormation uses to process your template\. The `Transform` section builds on the simple, declarative language of AWS CloudFormation with a powerful macro system\. 

You can declare one or more macros within a template\. AWS CloudFormation executes macros in the order that they are specified\. When you create a change set, AWS CloudFormation generates a change set that includes the processed template content\. You can then review the changes and execute the change set\. For more information, see [Using AWS CloudFormation Macros to Perform Custom Processing on Templates](template-macros.md)\.

AWS CloudFormation also supports the `AWS::Serverless` and `AWS::Include` transforms, which are macros hosted by AWS CloudFormation\. AWS CloudFormation treats these transforms the same as any macros you create in terms of execution order and scope\.
+ The `AWS::Serverless` transform specifies the version of the AWS Serverless Application Model \(AWS SAM\) to use\. This model defines the AWS SAM syntax that you can use and how AWS CloudFormation processes it\. For more information about serverless applications and AWS SAM, see [Deploying Lambda\-based Applications](https://docs.aws.amazon.com/lambda/latest/dg/deploying-lambda-apps.html) in the *AWS Lambda Developer Guide*\.
+ The `AWS::Include` transform works with template snippets that are stored separately from the main AWS CloudFormation template\. You can insert these snippets into your main template when [Creating a Change Set](using-cfn-updating-stacks-changesets-create.md) or [Updating Stacks Using Change Sets](using-cfn-updating-stacks-changesets.md)\.

To declare multiple macros, use a list format and specify one or more macros\.

For example, in the template sample below, AWS CloudFormation evaluates `MyMacro` and then `AWS::Serverless`, both of which can process the contents of the entire template because of their inclusion in the `Transform` section\.

```
// Start of processable content for MyMacro and AWS::Serverless
AWSTemplateFormatVersion: 2010-09-09 
 Transform: [MyMacro, AWS::Serverless]
 Resources:
    WaitCondition:
      Type: AWS::CloudFormation::WaitCondition
    MyBucket:
      Type: 'AWS::S3::Bucket'  
      Properties:
        BucketName: MyBucket 
        Tags: [{"key":"value"}] 
        CorsConfiguration:[]   
    MyEc2Instance:
      Type: 'AWS::EC2::Instance' Properties:
        ImageID: "ami-123"
// End of processable content for MyMacro and AWS::Serverless
```

**Topics**
+ [AWS::Serverless Transform](transform-aws-serverless.md)
+ [AWS::Include Transform](create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform.md)