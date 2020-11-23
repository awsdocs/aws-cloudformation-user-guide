# Continuous delivery with CodePipeline<a name="continuous-delivery-codepipeline"></a>

Continuous delivery is a release practice in which code changes are automatically built, tested, and prepared for release to production\. With AWS CloudFormation and CodePipeline, you can use continuous delivery to automatically build and test changes to your AWS CloudFormation templates before promoting them to production stacks\. This release process lets you rapidly and reliably make changes to your AWS infrastructure\.

For example, you can create a workflow that automatically builds a test stack when you submit an updated template to a code repository\. After AWS CloudFormation builds the test stack, you can test it and then decide whether to push the changes to a production stack\. For more information about the benefits of continuous delivery, see [What is continuous delivery?](https://aws.amazon.com/devops/continuous-delivery/)\.

Use CodePipeline to build a continuous delivery workflow by building a pipeline for AWS CloudFormation stacks\. CodePipeline has built\-in integration with AWS CloudFormation, so you can specify AWS CloudFormation\-specific actions, such as creating, updating, or deleting a stack, within a pipeline\. For more information about CodePipeline, see the [AWS CodePipeline User Guide](https://docs.aws.amazon.com/codepipeline/latest/userguide/)\.

**Topics**
+ [Walkthrough: Building a pipeline for test and production stacks](continuous-delivery-codepipeline-basic-walkthrough.md)
+ [AWS CloudFormation configuration properties reference](continuous-delivery-codepipeline-action-reference.md)
+ [AWS CloudFormation artifacts](continuous-delivery-codepipeline-cfn-artifacts.md)
+ [Using parameter override functions with CodePipeline pipelines](continuous-delivery-codepipeline-parameter-override-functions.md)