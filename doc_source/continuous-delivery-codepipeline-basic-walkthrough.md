# Walkthrough: Building a pipeline for test and production stacks<a name="continuous-delivery-codepipeline-basic-walkthrough"></a>

Imagine a release process where you submit an AWS CloudFormation template, which AWS CloudFormation then uses to automatically build a test stack\. After you review the test stack, you can preview how your changes will modify your production stack, and then choose whether to implement them\. To accomplish this workflow, you could use AWS CloudFormation to build your test stack, delete the test stack, create a change set, and then execute the change set\. However, with each action, you need to manually interact with AWS CloudFormation\. In this walkthrough, we'll build a CodePipeline pipeline that automates many of these actions, helping you achieve a continuous delivery workflow with your AWS CloudFormation stacks\.

## Prerequisites<a name="w7739ab1c21c11b5"></a>

This walkthrough assumes that you have used CodePipeline and AWS CloudFormation, and know how pipelines and AWS CloudFormation templates and stacks work\. For more information about CodePipeline, see the [AWS CodePipeline User Guide](https://docs.aws.amazon.com/codepipeline/latest/userguide/)\. You also need to have an Amazon S3 [bucket](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingBucket.html) in the same AWS region in which you will create your pipeline\.

**Important**  
The sample WordPress template creates an EC2 instance that requires a connection to the Internet\. Check that you have a default VPC and subnet that allow traffic to the Internet\.

## Walkthrough overview<a name="w7739ab1c21c11b7"></a>

This walkthrough builds a pipeline for a sample WordPress site in a stack\. The pipeline is separated into three stages\. Each stage must contain at least one action, which is a task the pipeline performs on your artifacts \(your input\)\. A stage organizes actions in a pipeline\. CodePipeline must complete all actions in a stage before the stage processes new artifacts, for example, if you submitted new input to rerun the pipeline\.

By the end of this walkthrough, you'll have a pipeline that performs the following workflow:

1. The first stage of the pipeline retrieves a source artifact \(an AWS CloudFormation template and its configuration files\) from a repository\.

   You'll prepare an artifact that includes a sample WordPress template and upload it to an S3 bucket\.

1. In the second stage, the pipeline creates a test stack and then waits for your approval\.

   After you review the test stack, you can choose to continue with the original pipeline or create and submit another artifact to make changes\. If you approve, this stage deletes the test stack, and then the pipeline continues to the next stage\.

1. In the third stage, the pipeline creates a change set against a production stack, and then waits for your approval\.

   In your initial run, you won't have a production stack\. The change set shows you all of the resources that AWS CloudFormation will create\. If you approve, this stage executes the change set and builds your production stack\.

**Note**  
AWS CloudFormation is a free service\. However, you are charged for the AWS resources, such as the EC2 instance, that you include in your stack at the current rate for each\. For more information about AWS pricing, see the detail page for each product at [http://aws\.amazon\.com](http://aws.amazon.com)\.

## Step 1: Edit the artifact and upload it to an S3 Bucket<a name="w7739ab1c21c11b9"></a>

Before you build your pipeline, you must set up your source repository and files\. CodePipeline copies these source files into your pipeline's [artifact store](https://docs.aws.amazon.com/codepipeline/latest/userguide/concepts.html), and then uses them to perform actions in your pipeline, such as creating an AWS CloudFormation stack\.

When you use Amazon Simple Storage Service \(Amazon S3\) as the source repository, CodePipeline requires you to zip your source files before uploading them to an S3 bucket\. The zipped file is a CodePipeline artifact that can contain an AWS CloudFormation template, a template configuration file, or both\. We provide an artifact that contains a sample WordPress template and two template configuration files\. The two configuration files specify parameter values for the WordPress template\. CodePipeline uses them when it creates the WordPress stacks\. One file contains parameter values for a test stack, and the other for a production stack\. You'll need to edit the configuration files, for example, to specify an existing EC2 key\-pair name that you own\. For more information about artifacts, see [AWS CloudFormation artifacts](continuous-delivery-codepipeline-cfn-artifacts.md)\.

After you build your artifact, you'll upload it to an S3 bucket\.

**To edit and upload the artifact**

1. Download and open the sample artifact: [https://s3\.amazonaws\.com/cloudformation\-examples/user\-guide/continuous\-deployment/wordpress\-single\-instance\.zip](https://s3.amazonaws.com/cloudformation-examples/user-guide/continuous-deployment/wordpress-single-instance.zip)\.

   The artifact contains three files:
   + The sample WordPress template: `wordpress-single-instance.yaml`
   + The template configuration file for the test stack\.: `test-stack-configuration.json` 
   + The template configuration file for the production stack: `prod-stack-configuration.json`

1. Extract all of the files, and then use any text editor to modify the template configuration files\.

   Open the configuration files to see that they contain key\-value pairs that map to the WordPress template's parameters\. The configuration files specify the parameter values that your pipeline uses when it creates the test and production stacks\.

   Edit the `test-stack-configuration.json` file to specify parameter values for the test stack and the `prod-stack-configuration.json` file for the production stack\.
   + Change the values of the `DBPassword` and `DBRootPassword` keys to passwords that you can use to log in to your WordPress database\. As defined in the WordPress template, the parameter values must contain only alphanumeric characters\.
   + Change the value of the `KeyName` key to an existing EC2 key\-pair name in the region in which you will create your pipeline\.

1. Add the modified configuration files to the original artifact \(`.zip`\) file, replacing duplicate files\.

   You now have a customized artifact that you can upload to an S3 bucket\.

1. [Upload the artifact to an S3 bucket that you own\.](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/UploadingObjectsintoAmazonS3.html)

   Note the file's location\. You'll specify the location of this file when you build your pipeline\.

   Notes about the artifact and S3 bucket:
   + Use a bucket that is in the same AWS region in which you will create your pipeline\.
   + CodePipeline requires that the bucket is [versioning enabled](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/enable-bucket-versioning.html)\.
   + You can also use services that don't require you to zip your files before uploading them, like GitHub or CodeCommit, for your source repository\.
   + Artifacts can contain sensitive information such as passwords\. [Limit access](https://docs.aws.amazon.com/AmazonS3/latest/user-guide/EditingPermissionsonanObject.html) so that only permitted users can view the file\. When you do, ensure that CodePipeline can still access the file\.

You now have an artifact that CodePipeline can pull in to your pipeline\. In the next step, you'll specify the artifact's location and build the WordPress pipeline\.

## Step 2: Create the pipeline stack<a name="w7739ab1c21c11c11"></a>

To create the WordPress pipeline, you'll use a sample AWS CloudFormation template\. In addition to building the pipeline, the template sets up AWS Identity and Access Management \(IAM\) service roles for CodePipeline and AWS CloudFormation, an S3 bucket for the CodePipeline artifact store, and an Amazon Simple Notification Service \(Amazon SNS\) topic to which the pipeline sends notifications, such as notifications about reviews\. The sample template makes it easy to provision and configure these resources in a single AWS CloudFormation stack\.

For more details about the configuration of the pipeline, see [What the pipeline does](#codepipeline-basic-walkthrough-template-details)\.

**Important**  
The sample WordPress template creates an EC2 instance that requires a connection to the Internet\. Check that your default VPC and subnet allow traffic to the Internet\.

**To create the pipeline stack**

1. Download the sample template at [https://s3\.amazonaws\.com/cloudformation\-examples/user\-guide/continuous\-deployment/basic\-pipeline\.yml](https://s3.amazonaws.com/cloudformation-examples/user-guide/continuous-deployment/basic-pipeline.yml)\. Save it on your computer\.

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\.

1. Choose an AWS region that supports CodePipeline and AWS CloudFormation\.

   For more information, see [AWS Regions and endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html) in the *AWS General Reference*\.

1. Choose **Create stack**\.

1. Under **Specify template**, choose **Upload a template file**, and then choose the template that you just downloaded, `basic-pipeline.yml`\.

1. Choose **Next**\.

1. For **Stack name**, type `sample-WordPress-pipeline`\.

1. In the **Parameters** section, specify the following parameter values, and then choose **Next**\. When setting stack parameters, if you kept the same names for the WordPress template and its configuration files, you can use the default values\. If not, specify the filenames that you used\.  
**PipelineName**  
The name of your pipeline, such as `WordPress-test-pipeline`\.  
**S3Bucket**  
The name of the S3 bucket where you saved your artifact \(`.zip` file\)\.  
**SourceS3Key**  
The filename of your artifact\. If you saved the artifact in a folder, include it as part of the filename, such as `folder/subfolder/wordpress-single-instance.zip`\.  
**Email**  
The email address to which CodePipeline sends pipeline notification, such as `myemail@example.com`\.

1. For this walkthrough, you don't need to add tags or specify advanced settings, so choose **Next**\.

1. Ensure that the stack name and template URL are correct, and then choose **Create stack**\.

1. To acknowledge that you're aware that AWS CloudFormation might create IAM resources, choose the checkbox\.

It might take several minutes for AWS CloudFormation to create your stack\. To monitor progress, view the stack events\. For more information, see [Viewing AWS CloudFormation stack data and resources on the AWS Management Console](cfn-console-view-stack-data-resources.md)\.

After your stack has been created, CodePipeline starts your new pipeline\. To view its status, see the [CodePipeline console](https://console.aws.amazon.com/codepipeline/)\. From the list of pipelines, choose **WordPress\-test\-pipeline**\.

### What the pipeline does<a name="codepipeline-basic-walkthrough-template-details"></a>

This section explains the pipeline's three stages, using snippets from the sample WordPress pipeline template\.

#### Stage 1: Source<a name="w7739ab1c21c11c11c15b5"></a>

The first stage of the pipeline is a source stage in which you specify the location of your source code\. Every time you push a revision to this location, CodePipeline reruns your pipeline\.

The source code is located in an S3 bucket and is identified by its filename\. You specified these values as input parameter values when you created the pipeline stack\. To allow using the source artifact in subsequent stages, the snippet specifies the `OutputArtifacts` property, with the name `TemplateSource`\. To use this artifact in later stages, you specify `TemplateSource` as an input artifact\.

```
- Name: S3Source
  Actions:
    - Name: TemplateSource
      ActionTypeId:
        Category: Source
        Owner: AWS
        Provider: S3
        Version: '1'
      Configuration:
        S3Bucket: !Ref 'S3Bucket'
        S3ObjectKey: !Ref 'SourceS3Key'
      OutputArtifacts:
        - Name: TemplateSource
```

#### Stage 2: TestStage<a name="w7739ab1c21c11c11c15b7"></a>

In the `TestStage` stage, the pipeline creates the test stack, waits for approval, and then deletes the test stack\.

For the `CreateStack` action, the pipeline uses the test configuration file and WordPress template to create the test stack\. Both files are contained in the `TemplateSource` input artifact, which is brought in from the source stage\. The snippet uses the `REPLACE_ON_FAILURE` action mode\. If stack creation fails, the pipeline replaces it so that you don't need to clean up or troubleshoot the stack before you can rerun the pipeline\. The action mode is useful for quickly iterating on test stacks\. For the `RoleArn` property, the value is an AWS CloudFormation service role that is declared elsewhere in the template\.

The `ApproveTestStack` action pauses the pipeline and sends a notification to the email address that you specified when you created the pipeline stack\. While the pipeline is paused, you can check the WordPress test stack and its resources\. Use CodePipeline to [approve or reject](https://docs.aws.amazon.com/codepipeline/latest/userguide/approvals-approve-or-reject.html) this action\. The `CustomData` property includes a description of the action you're approving, which the pipeline adds to the notification email\.

After you approve this action, CodePipeline moves to the `DeleteTestStack` action and deletes the test WordPress stack and its resources\.

```
- Name: TestStage
  Actions:
    - Name: CreateStack
      ActionTypeId:
        Category: Deploy
        Owner: AWS
        Provider: CloudFormation
        Version: '1'
      InputArtifacts:
        - Name: TemplateSource
      Configuration:
        ActionMode: REPLACE_ON_FAILURE
        RoleArn: !GetAtt [CFNRole, Arn]
        StackName: !Ref TestStackName
        TemplateConfiguration: !Sub "TemplateSource::${TestStackConfig}"
        TemplatePath: !Sub "TemplateSource::${TemplateFileName}"
      RunOrder: '1'
    - Name: ApproveTestStack
      ActionTypeId:
        Category: Approval
        Owner: AWS
        Provider: Manual
        Version: '1'
      Configuration:
        NotificationArn: !Ref CodePipelineSNSTopic
        CustomData: !Sub 'Do you want to create a change set against the production stack and delete the ${TestStackName} stack?'
      RunOrder: '2'
    - Name: DeleteTestStack
      ActionTypeId:
        Category: Deploy
        Owner: AWS
        Provider: CloudFormation
        Version: '1'
      Configuration:
        ActionMode: DELETE_ONLY
        RoleArn: !GetAtt [CFNRole, Arn]
        StackName: !Ref TestStackName
      RunOrder: '3'
```

#### Stage 3: ProdStage<a name="w7739ab1c21c11c11c15b9"></a>

The `ProdStage` stage of the pipeline creates a change set against the existing production stack, waits for approval, and then executes the change set\.

A change set provides a preview of all modifications AWS CloudFormation will make to your production stack before implementing them\. On your first pipeline run, you won't have a running production stack\. The change set shows the actions that AWS CloudFormation performed when creating the test stack\. To create the change set, the `CreateChangeSet` action uses the WordPress sample template and the production template configuration from the `TemplateSource` input artifact\.

Similar to the previous stage, the `ApproveChangeSet` action pauses the pipeline and sends an email notification\. While the pipeline is paused, you can view the change set to check all of the proposed modifications to the production WordPress stack\. Use CodePipeline to [approve or reject](https://docs.aws.amazon.com/codepipeline/latest/userguide/approvals-approve-or-reject.html) this action to continue or stop the pipeline, respectively\.

After you approve this action, the `ExecuteChangeSet` action executes the changes set, so that AWS CloudFormation performs all of the actions described in the change set\. For the initial run, AWS CloudFormation creates the WordPress production stack\. On subsequent runs, AWS CloudFormation updates the stack\.

```
- Name: ProdStage
  Actions:
    - Name: CreateChangeSet
      ActionTypeId:
        Category: Deploy
        Owner: AWS
        Provider: CloudFormation
        Version: '1'
      InputArtifacts:
        - Name: TemplateSource
      Configuration:
        ActionMode: CHANGE_SET_REPLACE
        RoleArn: !GetAtt [CFNRole, Arn]
        StackName: !Ref ProdStackName
        ChangeSetName: !Ref ChangeSetName
        TemplateConfiguration: !Sub "TemplateSource::${ProdStackConfig}"
        TemplatePath: !Sub "TemplateSource::${TemplateFileName}"
      RunOrder: '1'
    - Name: ApproveChangeSet
      ActionTypeId:
        Category: Approval
        Owner: AWS
        Provider: Manual
        Version: '1'
      Configuration:
        NotificationArn: !Ref CodePipelineSNSTopic
        CustomData: !Sub 'A new change set was created for the ${ProdStackName} stack. Do you want to implement the changes?'
      RunOrder: '2'
    - Name: ExecuteChangeSet
      ActionTypeId:
        Category: Deploy
        Owner: AWS
        Provider: CloudFormation
        Version: '1'
      Configuration:
        ActionMode: CHANGE_SET_EXECUTE
        ChangeSetName: !Ref ChangeSetName
        RoleArn: !GetAtt [CFNRole, Arn]
        StackName: !Ref ProdStackName
      RunOrder: '3'
```

## Step 3: View the WordPress stack<a name="w7739ab1c21c11c13"></a>

As CodePipeline runs through the pipeline, it uses AWS CloudFormation to create test and production stacks\. To see the status of these stacks and their output, use the AWS CloudFormation console\.

**To view a stack**

1. Open the AWS CloudFormation console at [https://console\.aws\.amazon\.com/cloudformation/](https://console.aws.amazon.com/cloudformation/)\.

1. Depending on whether your pipeline is in the test or production stage, choose the `Test-MyWordPressSite` or the `Prod-MyWordPressSite` stack\.

1. To check the status of your stack, view the stack [events](cfn-console-view-stack-data-resources.md)\.

If the stack is in a failed state, view the status reason to find the stack error\. Fix the error, and then rerun the pipeline\. If the stack is in the `CREATE_COMPLETE` state, view its outputs to get the URL of your WordPress site\.

You've successfully used CodePipeline to build a continuous delivery workflow for a sample WordPress site\. If you submit changes to the S3 bucket, CodePipeline automatically detects a new version, and then reruns your pipeline\. This workflow makes it easier to submit and test changes before making changes to your production site\.

## Step 4: Clean up resources<a name="w7739ab1c21c11c15"></a>

To make sure that you are not charged for unwanted services, delete your resources\.

**Important**  
Delete the test and production WordPress stacks before deleting the pipeline stack\. The pipeline stack contains a service role that's required to delete the WordPress stacks\. If you deleted the pipeline stack first, you can [associate another service role Amazon Resource Name \(ARN\)](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DeleteStack.html) with the WordPress stacks, and then delete them\.

**To delete objects in the artifact store**

1. Open the Amazon S3 console at [https://console\.aws\.amazon\.com/s3/](https://console.aws.amazon.com/s3/)\.

1. Choose the S3 bucket that CodePipeline used as your pipeline's artifact store\.

   The bucket's name follows the format: `stackname-artifactstorebucket-id`\. If you followed this walkthrough, the bucket's name might look similar to the following example: `sample-WordPress-pipeline-artifactstorebucket-12345abcd12345`\.

1. Delete all of the objects in the artifact store S3 bucket\.

   When you delete the pipeline stack in the next step, this bucket must be empty\. Otherwise, AWS CloudFormation won't be able to delete the bucket\.

**To delete stacks**

1. From the AWS CloudFormation console, choose the stack that you want to delete\.

   If the WordPress stacks that were created by the pipeline are still running, choose them first\. By default, the stack names are `Test-MyWordPressSite` and `Prod-MyWordPressSite`\.

   If you already deleted the WordPress stacks, choose the `sample-WordPress-pipeline` stack\.

1. Choose **Actions**, and then choose **Delete Stack**\.

1. In the confirmation message, choose **Yes, Delete**\.

AWS CloudFormation deletes the stack all of the stack's resources, such as the EC2 instance, notification topic, service role, and the pipeline\.

Now that you understand how to build a basic AWS CloudFormation workflow with CodePipeline, you can use the sample template and artifacts as a starting point for building your own\.

## See also<a name="w7739ab1c21c11c19"></a>

The following related resources can help you as you work with these parameters\.
+ For more information about the AWS CloudFormation action parameters in CodePipeline, see the [AWS CloudFormation](https://docs.aws.amazon.com/codepipeline/latest/userguide/action-reference-CloudFormation.html) action configuration reference in the *AWS CodePipeline User Guide*\.
+ For example template values by action provider, such as for the `Owner` field or the `configuration` fields, see the [Action structure reference](https://docs.aws.amazon.com/codepipeline/latest/userguide/action-reference.html) in the *AWS CodePipeline User Guide*\.
+ To download example pipeline stack templates in YAML or JSON format, see the tutorials under [Create a pipeline with AWS CloudFormation](https://docs.aws.amazon.com/codepipeline/latest/userguide/tutorials-cloudformation.html) in the *AWS CodePipeline User Guide*\.
+ For an example template configuration file, see [AWS CloudFormation artifacts](https://docs.aws.amazon.com/codepipeline/latest/userguide/continuous-delivery-codepipeline-cfn-artifacts.html)\.