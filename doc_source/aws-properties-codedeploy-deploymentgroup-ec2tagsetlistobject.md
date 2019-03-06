# CodeDeploy DeploymentGroup EC2TagSetListObject<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject"></a>

<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-description"></a>The `EC2TagSetListObject` property type specifies lists of EC2 tags\.

<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-inheritance"></a> `EC2TagSetListObject` is a property of the [CodeDeploy DeploymentGroup EC2TagSet](aws-properties-codedeploy-deploymentgroup-ec2tagset.md) property type\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-syntax.json"></a>

```
{
  "[Ec2TagGroup](#cfn-codedeploy-deploymentgroup-ec2tagsetlistobject-ec2taggroup)" : [[*EC2TagFilter*](aws-properties-codedeploy-deploymentgroup-ec2tagfilters.md), ...]
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-syntax.yaml"></a>

```
[Ec2TagGroup](#cfn-codedeploy-deploymentgroup-ec2tagsetlistobject-ec2taggroup): 
  - [*EC2TagFilter*](aws-properties-codedeploy-deploymentgroup-ec2tagfilters.md)
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-properties"></a>

`Ec2TagGroup`  <a name="cfn-codedeploy-deploymentgroup-ec2tagsetlistobject-ec2taggroup"></a>
The EC2 tags that are already applied to EC2 instances that you want to include in the deployment group\. CodeDeploy includes all EC2 instances identified by any of the tags you specify in this deployment group\.   
Duplicates are not allowed\.  
 *Required*: No  
 *Type*: List of [CodeDeploy DeploymentGroup Ec2TagFilters](aws-properties-codedeploy-deploymentgroup-ec2tagfilters.md)   
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-codedeploy-deploymentgroup-ec2tagsetlistobject-seealso"></a>
+ [EC2TagFilter](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_EC2TagFilter.html) in the *AWS CodeDeploy API Reference*