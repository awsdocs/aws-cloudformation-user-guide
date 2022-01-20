# AWS::Backup::Framework<a name="aws-resource-backup-framework"></a>

Creates a framework with one or more controls\. A framework is a collection of controls that you can use to evaluate your backup practices\. By using pre\-built customizable controls to define your policies, you can evaluate whether your backup practices comply with your policies and which resources are not yet in compliance\.

For a sample AWS CloudFormation template, see the [AWS Backup Developer Guide](https://docs.aws.amazon.com/aws-backup/latest/devguide/bam-cfn-integration.html#bam-cfn-frameworks-template)\.

## Syntax<a name="aws-resource-backup-framework-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-backup-framework-syntax.json"></a>

```
{
  "Type" : "AWS::Backup::Framework",
  "Properties" : {
      "[FrameworkControls](#cfn-backup-framework-frameworkcontrols)" : [ FrameworkControl, ... ],
      "[FrameworkDescription](#cfn-backup-framework-frameworkdescription)" : String,
      "[FrameworkName](#cfn-backup-framework-frameworkname)" : String,
      "[FrameworkTags](#cfn-backup-framework-frameworktags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-backup-framework-syntax.yaml"></a>

```
Type: AWS::Backup::Framework
Properties: 
  [FrameworkControls](#cfn-backup-framework-frameworkcontrols): 
    - FrameworkControl
  [FrameworkDescription](#cfn-backup-framework-frameworkdescription): String
  [FrameworkName](#cfn-backup-framework-frameworkname): String
  [FrameworkTags](#cfn-backup-framework-frameworktags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-backup-framework-properties"></a>

`FrameworkControls`  <a name="cfn-backup-framework-frameworkcontrols"></a>
Contains detailed information about all of the controls of a framework\. Each framework must contain at least one control\.  
*Required*: Yes  
*Type*: List of [FrameworkControl](aws-properties-backup-framework-frameworkcontrol.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrameworkDescription`  <a name="cfn-backup-framework-frameworkdescription"></a>
An optional description of the framework with a maximum 1,024 characters\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FrameworkName`  <a name="cfn-backup-framework-frameworkname"></a>
The unique name of a framework\. This name is between 1 and 256 characters, starting with a letter, and consisting of letters \(a\-z, A\-Z\), numbers \(0\-9\), and underscores \(\_\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z][_a-zA-Z0-9]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FrameworkTags`  <a name="cfn-backup-framework-frameworktags"></a>
A list of tags with which to tag your framework\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-backup-framework-return-values"></a>

### Ref<a name="aws-resource-backup-framework-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-backup-framework-return-values-fn--getatt"></a>

#### <a name="aws-resource-backup-framework-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The UTC time when you created your framework\.

`DeploymentStatus`  <a name="DeploymentStatus-fn::getatt"></a>
Depolyment status refers to whether your framework has completed deployment\. This status is usually `Completed`, but might also be `Create in progress` or another status\. For a list of statuses, see [Framework compliance status](https://docs.aws.amazon.com/aws-backup/latest/devguide/viewing-frameworks.html) in the *AWS Backup; Developer Guide*\.

`FrameworkArn`  <a name="FrameworkArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of your framework\.

`FrameworkStatus`  <a name="FrameworkStatus-fn::getatt"></a>
Framework status refers to whether you have turned on resource tracking for all of your resources\. This status is `Active` when you turn on all resources the framework evaluates\. For other statuses and steps to correct them, see [Framework compliance status](https://docs.aws.amazon.com/aws-backup/latest/devguide/viewing-frameworks.html) in the *AWS Backup; Developer Guide*\.