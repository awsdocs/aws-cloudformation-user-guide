# CodeDeploy DeploymentGroup Ec2TagFilters<a name="aws-properties-codedeploy-deploymentgroup-ec2tagfilters"></a>

`Ec2TagFilters` is a property of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) resource that specifies which EC2 instances to associate with the deployment group\.

For information on using tags and tag groups to help manage your Amazon EC2 instances and on\-premises instances, see [Tagging Instances for Deployment Groups in AWS CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-tagging.html) in the *AWS CodeDeploy User Guide*\.

## Syntax<a name="w13ab1c21c10c78c21c33b7"></a>

### JSON<a name="aws-properties-codedeploy-deploymentgroup-ec2tagfilters-syntax.json"></a>

```
{
  "[Key](#cfn-properties-codedeploy-deploymentgroup-ec2tagfilters-key)" : String,
  "[Type](#cfn-properties-codedeploy-deploymentgroup-ec2tagfilters-type)" : String,
  "[Value](#cfn-properties-codedeploy-deploymentgroup-ec2tagfilters-value)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-ec2tagfilters-syntax.yaml"></a>

```
[Key](#cfn-properties-codedeploy-deploymentgroup-ec2tagfilters-key): String
[Type](#cfn-properties-codedeploy-deploymentgroup-ec2tagfilters-type): String
[Value](#cfn-properties-codedeploy-deploymentgroup-ec2tagfilters-value): String
```

## Properties<a name="w13ab1c21c10c78c21c33b9"></a>

`Key`  <a name="cfn-properties-codedeploy-deploymentgroup-ec2tagfilters-key"></a>
Filter instances with this key\.  
*Required*: No  
*Type*: String

`Type`  <a name="cfn-properties-codedeploy-deploymentgroup-ec2tagfilters-type"></a>
The filter type\. For example, you can filter instances by the key, tag value, or both\. For valid values, see [EC2TagFilter](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_EC2TagFilter.html) in the *AWS CodeDeploy API Reference*\.  
*Required*: Yes  
*Type*: String

`Value`  <a name="cfn-properties-codedeploy-deploymentgroup-ec2tagfilters-value"></a>
Filter instances with this tag value\.  
*Required*: No  
*Type*: String