# CodeDeploy DeploymentGroup Ec2TagSet<a name="aws-properties-codedeploy-deploymentgroup-ec2tagset"></a>

<a name="aws-properties-codedeploy-deploymentgroup-ec2tagset-description"></a>The `Ec2TagSet` property type specifies information about groups of tags applied to EC2 instances\. The deployment group will include only EC2 instances identified by all the tag groups\. Cannot be used in the same template as EC2TagFilters\.

For information on using tags and tag groups to help manage your Amazon EC2 instances and on\-premises instances, see [Tagging Instances for Deployment Groups in AWS CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-tagging.html) in the *AWS CodeDeploy User Guide*\.

<a name="aws-properties-codedeploy-deploymentgroup-ec2tagset-inheritance"></a> `Ec2TagSet` is a property of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) resource type\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-ec2tagset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-ec2tagset-syntax.json"></a>

```
{
  "[Ec2TagSetList](#cfn-codedeploy-deploymentgroup-ec2tagset-ec2tagsetlist)" : [[*Ec2TagSetListObject*](aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject.md), ...]
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-ec2tagset-syntax.yaml"></a>

```
[Ec2TagSetList](#cfn-codedeploy-deploymentgroup-ec2tagset-ec2tagsetlist): 
  - [*Ec2TagSetListObject*](aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject.md)
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-ec2tagset-properties"></a>

`Ec2TagSetList`  <a name="cfn-codedeploy-deploymentgroup-ec2tagset-ec2tagsetlist"></a>
A list containing other lists of EC2 instance tag groups\. In order for an instance to be included in the deployment group, it must be identified by all the tag groups in the list\.  
Duplicates are not allowed\.  
 *Required*: No  
 *Type*: List of [EC2TagSetListObject](aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-codedeploy-deploymentgroup-ec2tagset-seealso"></a>
+ [EC2TagSet](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_EC2TagSet.html) in the *AWS CodeDeploy API Reference*