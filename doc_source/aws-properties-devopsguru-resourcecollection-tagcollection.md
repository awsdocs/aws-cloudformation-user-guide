# AWS::DevOpsGuru::ResourceCollection TagCollection<a name="aws-properties-devopsguru-resourcecollection-tagcollection"></a>

A collection of AWS tags\.

Tags help you identify and organize your AWS resources\. Many AWS services support tagging, so you can assign the same tag to resources from different services to indicate that the resources are related\. For example, you can assign the same tag to an Amazon DynamoDB table resource that you assign to an AWS Lambda function\. For more information about using tags, see the [Tagging best practices](https://docs.aws.amazon.com/whitepapers/latest/tagging-best-practices/tagging-best-practices.html) whitepaper\. 

Each AWS tag has two parts\. 
+ A tag *key* \(for example, `CostCenter`, `Environment`, `Project`, or `Secret`\)\. Tag *keys* are case\-sensitive\.
+ An optional field known as a tag *value* \(for example, `111122223333`, `Production`, or a team name\)\. Omitting the tag *value* is the same as using an empty string\. Like tag *keys*, tag *values* are case\-sensitive\.

Together these are known as *key*\-*value* pairs\.

**Important**  
The string used for a *key* in a tag that you use to define your resource coverage must begin with the prefix `Devops-guru-`\. The tag *key* might be `DevOps-Guru-deployment-application` or `devops-guru-rds-application`\. When you create a *key*, the case of characters in the *key* can be whatever you choose\. After you create a *key*, it is case\-sensitive\. For example, DevOps Guru works with a *key* named `devops-guru-rds` and a *key* named `DevOps-Guru-RDS`, and these act as two different *keys*\. Possible *key*/*value* pairs in your application might be `Devops-Guru-production-application/RDS` or `Devops-Guru-production-application/containers`\.

## Syntax<a name="aws-properties-devopsguru-resourcecollection-tagcollection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-devopsguru-resourcecollection-tagcollection-syntax.json"></a>

```
{
  "[AppBoundaryKey](#cfn-devopsguru-resourcecollection-tagcollection-appboundarykey)" : String,
  "[TagValues](#cfn-devopsguru-resourcecollection-tagcollection-tagvalues)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-devopsguru-resourcecollection-tagcollection-syntax.yaml"></a>

```
  [AppBoundaryKey](#cfn-devopsguru-resourcecollection-tagcollection-appboundarykey): String
  [TagValues](#cfn-devopsguru-resourcecollection-tagcollection-tagvalues): 
    - String
```

## Properties<a name="aws-properties-devopsguru-resourcecollection-tagcollection-properties"></a>

`AppBoundaryKey`  <a name="cfn-devopsguru-resourcecollection-tagcollection-appboundarykey"></a>
An AWS tag *key* that is used to identify the AWS resources that DevOps Guru analyzes\. All AWS resources in your account and Region tagged with this *key* make up your DevOps Guru application and analysis boundary\.  
The string used for a *key* in a tag that you use to define your resource coverage must begin with the prefix `Devops-guru-`\. The tag *key* might be `DevOps-Guru-deployment-application` or `devops-guru-rds-application`\. When you create a *key*, the case of characters in the *key* can be whatever you choose\. After you create a *key*, it is case\-sensitive\. For example, DevOps Guru works with a *key* named `devops-guru-rds` and a *key* named `DevOps-Guru-RDS`, and these act as two different *keys*\. Possible *key*/*value* pairs in your application might be `Devops-Guru-production-application/RDS` or `Devops-Guru-production-application/containers`\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^([\p{L}\p{Z}\p{N}_.:/=+\-@]*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagValues`  <a name="cfn-devopsguru-resourcecollection-tagcollection-tagvalues"></a>
The values in an AWS tag collection\.  
The tag's *value* is an optional field used to associate a string with the tag *key* \(for example, `111122223333`, `Production`, or a team name\)\. The *key* and *value* are the tag's *key* pair\. Omitting the tag *value* is the same as using an empty string\. Like tag *keys*, tag *values* are case\-sensitive\. You can specify a maximum of 256 characters for a tag value\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)