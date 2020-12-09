# AWS::CodeDeploy::DeploymentGroup OnPremisesTagSet<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagset"></a>

The `OnPremisesTagSet` property type specifies a list containing other lists of on\-premises instance tag groups\. In order for an instance to be included in the deployment group, it must be identified by all the tag groups in the list\.

For more information about using tags and tag groups to help manage your Amazon EC2 instances and on\-premises instances, see [Tagging Instances for Deployment Groups in AWS CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-tagging.html) in the *AWS CodeDeploy User Guide*\.

 `OnPremisesTagSet` is a property of the [DeploymentGroup ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentgroup.html) resource\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagset-syntax.json"></a>

```
{
  "[OnPremisesTagSetList](#cfn-codedeploy-deploymentgroup-onpremisestagset-onpremisestagsetlist)" : [ OnPremisesTagSetListObject, ... ]
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagset-syntax.yaml"></a>

```
  [OnPremisesTagSetList](#cfn-codedeploy-deploymentgroup-onpremisestagset-onpremisestagsetlist): 
    - OnPremisesTagSetListObject
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagset-properties"></a>

`OnPremisesTagSetList`  <a name="cfn-codedeploy-deploymentgroup-onpremisestagset-onpremisestagsetlist"></a>
A list that contains other lists of on\-premises instance tag groups\. For an instance to be included in the deployment group, it must be identified by all of the tag groups in the list\.  
Duplicates are not allowed\.   
*Required*: No  
*Type*: List of [OnPremisesTagSetListObject](aws-properties-codedeploy-deploymentgroup-onpremisestagsetlistobject.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)