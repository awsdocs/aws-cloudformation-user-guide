# AWS::CodeDeploy::DeploymentGroup EC2TagSetListObject<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject"></a>

The `EC2TagSet` property type specifies information about groups of tags applied to EC2 instances\. The deployment group includes only EC2 instances identified by all the tag groups\. Cannot be used in the same template as EC2TagFilters\.

For more information about using tags and tag groups to help manage your Amazon EC2 instances and on\-premises instances, see [Tagging Instances for Deployment Groups in AWS CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-tagging.html) in the *AWS CodeDeploy User Guide*\.

 `EC2TagSet` is a property of the [DeploymentGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentgroup.html) resource type\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-syntax.json"></a>

```
{
  "[Ec2TagGroup](#cfn-codedeploy-deploymentgroup-ec2tagsetlistobject-ec2taggroup)" : [ EC2TagFilter, ... ]
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-syntax.yaml"></a>

```
  [Ec2TagGroup](#cfn-codedeploy-deploymentgroup-ec2tagsetlistobject-ec2taggroup): 
    - EC2TagFilter
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-properties"></a>

`Ec2TagGroup`  <a name="cfn-codedeploy-deploymentgroup-ec2tagsetlistobject-ec2taggroup"></a>
A list that contains other lists of EC2 instance tag groups\. For an instance to be included in the deployment group, it must be identified by all of the tag groups in the list\.  
*Required*: No  
*Type*: List of [EC2TagFilter](aws-properties-codedeploy-deploymentgroup-ec2tagfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject--seealso"></a>
+  [EC2TagSet](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_EC2TagSet.html) in the *AWS CodeDeploy API Reference*\.

