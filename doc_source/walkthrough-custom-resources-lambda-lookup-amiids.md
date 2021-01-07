# Walkthrough: Looking up Amazon Machine Image IDs<a name="walkthrough-custom-resources-lambda-lookup-amiids"></a>

AWS CloudFormation templates that declare an Amazon Elastic Compute Cloud \(Amazon EC2\) instance must also specify an Amazon Machine Image \(AMI\) ID, which includes an operating system and other software and configuration information used to launch the instance\. The correct AMI ID depends on the instance type and region in which you're launching your stack\. And IDs can change regularly, such as when an AMI is updated with software updates\.

Normally, you might map AMI IDs to specific instance types and regions\. To update the IDs, you manually change them in each of your templates\. By using custom resources and AWS Lambda \(Lambda\), you can create a function that gets the IDs of the latest AMIs for the region and instance type that you're using so that you don't have to maintain mappings\.

This walkthrough shows you how to create a custom resource and associate a Lambda function with it to look up AMI IDs\. Note that the walkthrough assumes that you understand how to use custom resources and Lambda\. For more information, see [Custom resources](template-custom-resources.md) or the [AWS Lambda Developer Guide](https://docs.aws.amazon.com/lambda/latest/dg/)\.

Walkthrough Overview

For this walkthrough, you'll create a stack with a custom resource, a Lambda function, and an EC2 instance\. The walkthrough provides sample code and a sample template that you'll use to create the stack\.

The sample template uses the custom resource type to invoke and send input values to the Lambda function\. When you use the template, AWS CloudFormation invokes the function and sends information to it, such as the request type, input data, and a pre\-signed Amazon Simple Storage Service \(Amazon S3\) URL\. The function uses that information to look up the AMI ID, and then sends a response to the pre\-signed URL\.

After AWS CloudFormation gets a response in the pre\-signed URL location, it proceeds with creating the stack\. When AWS CloudFormation creates the instance, it uses the Lambda function's response to specify the instance's AMI ID\.

The following list summarizes the process\. You need AWS Identity and Access Management \(IAM\) permissions to use all the corresponding services, such as Lambda, Amazon EC2, and AWS CloudFormation\.

**Note**  
AWS CloudFormation is a free service; however, you are charged for the AWS resources, such as the Lambda function and EC2 instance, that you include in your stacks at the current rate for each\. For more information about AWS pricing, see the detail page for each product at [http://aws\.amazon\.com](http://aws.amazon.com)\.

1. [Save the sample Lambda package in an Amazon Simple Storage Service \(Amazon S3\) bucket\.](#walkthrough-custom-resources-lambda-lookup-amiids-savesample)

   The sample package contains everything that's required to create the Lambda function\. You must save the package in a bucket that's in the same region in which you will create your stack\.

1. [Use the sample template to create a stack\.](#walkthrough-custom-resources-lambda-lookup-amiids-createfunction-createstack)

   The stack demonstrates how you associate the Lambda function with a custom resource and how to use the results from the function to specify an AMI ID\. The stack also creates an IAM role \(execution role\), which Lambda uses to make calls to Amazon EC2\.

1. [Delete the stack\.](#walkthrough-custom-resources-lambda-lookup-amiids-createfunction-cleanup)

   Delete the stack to clean up all the stack resources that you created so that you aren't charged for unnecessary resources\.

## Step 1: Downloading and saving the sample package in Amazon S3<a name="walkthrough-custom-resources-lambda-lookup-amiids-savesample"></a>

When you create a stack with a Lambda function, you must specify the location of the Amazon S3 bucket that contains the function's source code\. The bucket must be in the same region in which you create your stack\.

This walkthrough provides a sample package \(a `.zip` file\) that's required to create the Lambda function\. A Lambda package contains the source code for the function and required libraries\. For this walkthrough, the function doesn't require additional libraries\.

The function takes an instance's architecture and region as inputs from an AWS CloudFormation custom resource request and returns the latest AMI ID to a pre\-signed Amazon S3 URL\.

**To download and save the package in Amazon S3**

1. Download the sample package from Amazon S3\. When you save the file, use the same file name as the sample, `amilookup.zip` or `amilookup-win.zip`\.  
**Look up Linux AMI IDs**  
[https://s3\.amazonaws\.com/cloudformation\-examples/lambda/amilookup\.zip](https://s3.amazonaws.com/cloudformation-examples/lambda/amilookup.zip)  
**Look up Windows AMI IDs**  
[https://s3\.amazonaws\.com/cloudformation\-examples/lambda/amilookup\-win\.zip](https://s3.amazonaws.com/cloudformation-examples/lambda/amilookup-win.zip)

1. Open the Amazon S3 console at [https://console\.aws\.amazon\.com/s3/home](https://console.aws.amazon.com/s3/home)\.

1. Choose or create a bucket that's located in the same region in which you'll create your AWS CloudFormation stack\. Record the bucket name\.

   You'll save the sample package in this bucket\. For more information about creating a bucket, see [Creating a bucket](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/CreatingaBucket.html) in the *Amazon Simple Storage Service Console User Guide*\.

1. Upload the sample package to the bucket that you chose or created\.

   For more information about uploading objects, see [Uploading objects](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/UploadingObjectsintoAmazonS3.html) in the *Amazon Simple Storage Service Console User Guide*\.

With the package in Amazon S3, you can now specify its location in the Lambda resource declaration of the AWS CloudFormation template\. The next step demonstrates how you declare the function and invoke it by using a custom resource\. You'll also see how to use the results of the function to specify the AMI ID of an EC2 instance\.

## Step 2: Creating the stack<a name="walkthrough-custom-resources-lambda-lookup-amiids-createfunction-createstack"></a>

To create the sample Amazon EC2 stack, you'll use a sample template that includes a Lambda function, an IAM execution role, a custom resource that invokes the function, and an EC2 instance that uses the results from the function\.

During stack creation, the custom resource invokes the Lambda function and waits until the function sends a response to the pre\-signed Amazon S3 URL\. In the response, the function returns the ID of the latest AMI that corresponds to the EC2 instance type and region in which you are creating the instance\. The data from the function's response is stored as an attribute of the custom resource, which is used to specify the AMI ID of the EC2 instance\.

The following snippets explain relevant parts of the sample template to help you understand how to associate a Lambda function with a custom resource and how to use the function's response\. 

To view the entire sample template, see:

**Linux template**  
[https://s3\.amazonaws\.com/cloudformation\-examples/lambda/LambdaAMILookupSample\.template](https://s3.amazonaws.com/cloudformation-examples/lambda/LambdaAMILookupSample.template)

**Windows template**  
[https://s3\.amazonaws\.com/cloudformation\-examples/lambda/LambdaAMILookupSample\-win\.template](https://s3.amazonaws.com/cloudformation-examples/lambda/LambdaAMILookupSample-win.template)

Stack Template Snippets

To create the Lambda function, you declare the `AWS::Lambda::Function` resource, which requires the function's source code, handler name, runtime environment, and execution role ARN\.

**Example JSON syntax**  

```
"AMIInfoFunction": {
  "Type": "AWS::Lambda::Function",
  "Properties": {
    "Code": {
      "S3Bucket": { "Ref": "S3Bucket" },
      "S3Key": { "Ref": "S3Key" }
    },
    "Handler": { "Fn::Join" : [ "", [{ "Ref": "ModuleName" },".handler"] ] },
    "Runtime": "nodejs8.10",
    "Timeout": "30",
    "Role": { "Fn::GetAtt" : ["LambdaExecutionRole", "Arn"] }
  }
}
```

**Example YAML syntax**  

```
AMIInfoFunction:
  Type: AWS::Lambda::Function
  Properties:
    Code:
      S3Bucket: !Ref S3Bucket
      S3Key: !Ref S3Key
    Handler: !Sub "${ModuleName}.handler"
    Runtime: nodejs8.10
    Timeout: 30
    Role: !GetAtt LambdaExecutionRole.Arn
```

The `Code` property specifies the Amazon S3 location \(bucket name and file name\) where you uploaded the sample package\. The sample template uses input parameters \(`"Ref": "S3Bucket"` and `"Ref": "S3Key"`\) to set the bucket and file names so that you are able to specify the names when you create the stack\. Similarly, the handler name, which corresponds to the name of the source file \(the JavaScript file\) in the `.zip` package, also uses an input parameter \(`"Ref": "ModuleName"`\)\. Because the source file is JavaScript code, the runtime is specified as `nodejs8.10`\.

For this walkthrough, the execution time for the function exceeds the default value of `3` seconds, so the timeout is set to `30` seconds\. If you don't specify a sufficiently long timeout, Lambda might cause a timeout before the function can complete, causing stack creation to fail\.

The execution role, which is declared elsewhere in the template, is specified by using the `Fn::GetAtt` intrinsic function in the `Role` property\. The execution role grants the Lambda function permission to send logs to AWS and to call the EC2 `DescribeImages` API\. The following snippet shows the role and policy that grant the appropriate permission:

**Example JSON syntax**  

```
"LambdaExecutionRole": {
  "Type": "AWS::IAM::Role",
  "Properties": {
    "AssumeRolePolicyDocument": {
      "Version": "2012-10-17",
      "Statement": [{
        "Effect": "Allow",
        "Principal": {"Service": ["lambda.amazonaws.com"]},
        "Action": ["sts:AssumeRole"]
      }]
    },
    "Path": "/",
    "Policies": [{
      "PolicyName": "root",
      "PolicyDocument": {
        "Version": "2012-10-17",
        "Statement": [{
          "Effect": "Allow",
          "Action": ["logs:CreateLogGroup","logs:CreateLogStream","logs:PutLogEvents"],
          "Resource": "arn:aws:logs:*:*:*"
        },
        {
          "Effect": "Allow",
          "Action": ["ec2:DescribeImages"],
          "Resource": "*"
        }]
      }
    }]
  }
}
```

**Example YAML syntax**  

```
LambdaExecutionRole:
  Type: AWS::IAM::Role
  Properties:
    AssumeRolePolicyDocument:
      Version: '2012-10-17'
      Statement:
      - Effect: Allow
        Principal:
          Service:
          - lambda.amazonaws.com
        Action:
        - sts:AssumeRole
    Path: "/"
    Policies:
    - PolicyName: root
      PolicyDocument:
        Version: '2012-10-17'
        Statement:
        - Effect: Allow
          Action:
          - logs:CreateLogGroup
          - logs:CreateLogStream
          - logs:PutLogEvents
          Resource: arn:aws:logs:*:*:*
        - Effect: Allow
          Action:
          - ec2:DescribeImages
          Resource: "*"
```

For both the Linux and Windows templates, the custom resource invokes the Lambda function that is associated with it\. To associate a function with a custom resource, you specify the Amazon Resource Name \(ARN\) of the function for the `ServiceToken` property, using the `Fn::GetAtt` intrinsic function\. AWS CloudFormation sends the additional properties that are included in the custom resource declaration, such as `Region` and `Architecture`, to the Lambda function as inputs\. The Lambda function determines the correct names and values for these input properties\.

**Example JSON syntax**  

```
"AMIInfo": {
  "Type": "Custom::AMIInfo",
  "Properties": {
    "ServiceToken": { "Fn::GetAtt" : ["AMIInfoFunction", "Arn"] },
    "Region": { "Ref": "AWS::Region" },
    "Architecture": { "Fn::FindInMap" : [ "AWSInstanceType2Arch", { "Ref" : "InstanceType" }, "Arch" ] }
  }
}
```

**Example YAML syntax**  

```
AMIInfo:
  Type: Custom::AMIInfo
  Properties:
    ServiceToken: !GetAtt AMIInfoFunction.Arn
    Region: !Ref "AWS::Region"
    Architecture:
      Fn::FindInMap:
      - AWSInstanceType2Arch
      - !Ref InstanceType
      - Arch
```

For Windows, the custom resource provides the Windows version to the Lambda function instead of the instance's architecture\.

**Example JSON syntax**  

```
"AMIInfo": {
  "Type": "Custom::AMIInfo",
  "Properties": {
    "ServiceToken": { "Fn::GetAtt" : ["AMIInfoFunction", "Arn"] },
    "Region": { "Ref": "AWS::Region" },
    "OSName": { "Ref": "WindowsVersion" }
  }
}
```

**Example YAML syntax**  

```
AMIInfo:
  Type: Custom::AMIInfo
  Properties:
    ServiceToken: !GetAtt AMIInfoFunction.Arn
    Region: !Ref "AWS::Region"
    OSName: !Ref "WindowsVersion"
```

When AWS CloudFormation invokes the Lambda function, the function calls the EC2 `DescribeImages` API, using the region and instance architecture or the OS name to filter the list of images\. Then the function sorts the list of images by date and returns the ID of the latest AMI\.

When returning the ID of the latest AMI, the function sends the ID to a pre\-signed URL in the `Data` property of the [response object](crpg-ref-responses.md)\. The data is structured as a name\-value pair, as shown in the following example:

```
"Data": { 
  "Id": "ami-43795473"
}
```

The following snippet shows how to get the data from a Lambda function\. It uses the `Fn::GetAtt` intrinsic function, providing the name of the custom resource and the attribute name of the value that you want to get\. In this walkthrough, the custom resource name is `AMIInfo` and the attribute name is `Id`\.

**Example JSON syntax**  

```
"SampleInstance": {  
  "Type": "AWS::EC2::Instance",
  "Properties": {
    "InstanceType"   : { "Ref" : "InstanceType" },
    "ImageId": { "Fn::GetAtt": [ "AMIInfo", "Id" ] }
  }
}
```

**Example YAML syntax**  

```
SampleInstance:
  Type: AWS::EC2::Instance
  Properties:
    InstanceType: !Ref InstanceType
    ImageId: !GetAtt AMIInfo.Id
```

Now that you understand what the template does, use the sample template to create a stack\.

**To create the stack**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\.

1. Choose **Create Stack**\.

1. In the **Template** section, choose **Specify an Amazon S3 template URL**, and then copy and paste the following URL in the text box:  
**Linux template**  
`[https://s3\.amazonaws\.com/cloudformation\-examples/lambda/LambdaAMILookupSample\.template](https://s3.amazonaws.com/cloudformation-examples/lambda/LambdaAMILookupSample.template)`  
**Windows template**  
`[https://s3\.amazonaws\.com/cloudformation\-examples/lambda/LambdaAMILookupSample\-win\.template](https://s3.amazonaws.com/cloudformation-examples/lambda/LambdaAMILookupSample-win.template)`

1. Choose **Next**\.

1. In the **Stack name** field, type **SampleEC2Instance**\.

1. In the **Parameters** section, specify the name of the Amazon S3 bucket that you created, and then choose **Next**\.

   The default values for the other parameters are the same names that are used in the sample `.zip` package\.

1. For this walkthrough, you don't need to add tags or specify advanced settings, so choose **Next**\.

1. Ensure that the stack name and template URL are correct, and then choose **Create**\.

It might take several minutes for AWS CloudFormation to create your stack\. To monitor progress, view the stack events\. For more information, see [Viewing AWS CloudFormation stack data and resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)\.

If stack creation succeeds, all resources in the stack, such as the Lambda function, custom resource, and EC2 instance, were created\. You successfully used a Lambda function and custom resource to specify the AMI ID of an EC2 instance\. You don't need to create and maintain a mapping of AMI IDs in this template\.

To see which AMI ID AWS CloudFormation used to create the EC2 instance, view the stack outputs\.

If the Lambda function returns an error, view the function's logs in the Amazon CloudWatch Logs [console](https://console.aws.amazon.com/cloudwatch/home#logs:)\. The name of the log stream is the physical ID of the custom resource, which you can find by viewing the stack's resources\. For more information, see [Viewing log data](https://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/ViewingLogData.html) in the *Amazon CloudWatch User Guide*\.

## Step 3: Clean up resources<a name="walkthrough-custom-resources-lambda-lookup-amiids-createfunction-cleanup"></a>

To make sure that you are not charged for unwanted services, delete your stack\.

**To delete the stack**

1. From the AWS CloudFormation console, choose the **SampleEC2Instance** stack\.

1. Choose **Actions** and then **Delete Stack**\.

1. In the confirmation message, choose **Yes, Delete**\.

All the resources that you created are deleted\.

Now that you understand how to create and use Lambda functions with AWS CloudFormation, you can use the sample template and code from this walkthrough to build other stacks and functions\.

## Related information<a name="w7739ab1c27c24c14b7c29"></a>
+ [AWS CloudFormation Custom Resource Reference](crpg-ref.md)