# AWS CodeDeploy DeploymentGroup OnPremisesTagSetListObject<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagsetlistobject"></a>

<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagsetlistobject-description"></a>The `OnPremisesTagSetListObject` property type specifies lists of on\-premises instance tag groups\. In order for an instance to be included in the deployment group, it must be identified by all the tag groups in the list\.

<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagsetlistobject-inheritance"></a> `OnPremisesTagSetListObject` is a property of the [AWS CodeDeploy DeploymentGroup OnPremisesTagSet](aws-properties-codedeploy-deploymentgroup-onpremisestagset.md) property type\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagsetlistobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagsetlistobject-syntax.json"></a>

```
{
  "[OnPremisesTagGroup](#cfn-codedeploy-deploymentgroup-onpremisestagsetlistobject-onpremisestaggroup)" : [ [*TagFilter*](aws-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters.md), ... ] 
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagsetlistobject-syntax.yaml"></a>

```
[OnPremisesTagGroup](#cfn-codedeploy-deploymentgroup-onpremisestagsetlistobject-onpremisestaggroup)
  - [*TagFilter*](aws-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters.md)
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagsetlistobject-properties"></a>

`OnPremisesTagGroup`  <a name="cfn-codedeploy-deploymentgroup-onpremisestagsetlistobject-onpremisestaggroup"></a>
Lists of on\-premises instance tag groups\.  
Duplicates are not allowed\.  
*Required*: No  
 *Type*: List of [AWS CodeDeploy DeploymentGroup TagFilters](aws-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters.md)   
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-codedeploy-deploymentgroup-onpremisestagsetlistobject-seealso"></a>
+ [OnPremisesTagSet](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_OnPremisesTagSet.html) in the *AWS CodeDeploy API Reference*