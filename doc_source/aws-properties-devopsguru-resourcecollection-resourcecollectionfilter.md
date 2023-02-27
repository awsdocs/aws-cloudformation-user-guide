# AWS::DevOpsGuru::ResourceCollection ResourceCollectionFilter<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter"></a>

 Information about a filter used to specify which AWS resources are analyzed for anomalous behavior by DevOps Guru\. 

## Syntax<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter-syntax.json"></a>

```
{
  "[CloudFormation](#cfn-devopsguru-resourcecollection-resourcecollectionfilter-cloudformation)" : CloudFormationCollectionFilter,
  "[Tags](#cfn-devopsguru-resourcecollection-resourcecollectionfilter-tags)" : [ TagCollection, ... ]
}
```

### YAML<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter-syntax.yaml"></a>

```
  [CloudFormation](#cfn-devopsguru-resourcecollection-resourcecollectionfilter-cloudformation): 
    CloudFormationCollectionFilter
  [Tags](#cfn-devopsguru-resourcecollection-resourcecollectionfilter-tags): 
    - TagCollection
```

## Properties<a name="aws-properties-devopsguru-resourcecollection-resourcecollectionfilter-properties"></a>

`CloudFormation`  <a name="cfn-devopsguru-resourcecollection-resourcecollectionfilter-cloudformation"></a>
 Information about AWS CloudFormation stacks\. You can use up to 500 stacks to specify which AWS resources in your account to analyze\. For more information, see [Stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacks.html) in the * AWS CloudFormation User Guide*\.   
*Required*: No  
*Type*: [CloudFormationCollectionFilter](aws-properties-devopsguru-resourcecollection-cloudformationcollectionfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-devopsguru-resourcecollection-resourcecollectionfilter-tags"></a>
The AWS tags used to filter the resources in the resource collection\.  
Tags help you identify and organize your AWS resources\. Many AWS services support tagging, so you can assign the same tag to resources from different services to indicate that the resources are related\. For example, you can assign the same tag to an Amazon DynamoDB table resource that you assign to an AWS Lambda function\. For more information about using tags, see the [Tagging best practices](https://docs.aws.amazon.com/whitepapers/latest/tagging-best-practices/tagging-best-practices.html) whitepaper\.   
Each AWS tag has two parts\.   
+ A tag *key* \(for example, `CostCenter`, `Environment`, `Project`, or `Secret`\)\. Tag *keys* are case\-sensitive\.
+ An optional field known as a tag *value* \(for example, `111122223333`, `Production`, or a team name\)\. Omitting the tag *value* is the same as using an empty string\. Like tag *keys*, tag *values* are case\-sensitive\.
Together these are known as *key*\-*value* pairs\.  
The string used for a *key* in a tag that you use to define your resource coverage must begin with the prefix `Devops-guru-`\. The tag *key* might be `DevOps-Guru-deployment-application` or `devops-guru-rds-application`\. When you create a *key*, the case of characters in the *key* can be whatever you choose\. After you create a *key*, it is case\-sensitive\. For example, DevOps Guru works with a *key* named `devops-guru-rds` and a *key* named `DevOps-Guru-RDS`, and these act as two different *keys*\. Possible *key*/*value* pairs in your application might be `Devops-Guru-production-application/RDS` or `Devops-Guru-production-application/containers`\.
*Required*: No  
*Type*: List of [TagCollection](aws-properties-devopsguru-resourcecollection-tagcollection.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)