# AWS CodeDeploy DeploymentGroup TagFilters<a name="aws-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters"></a>

`TagFilter` is a property type of the [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) resource that specifies which on\-premises instances to associate with the deployment group\. To register on\-premise instances with AWS CodeDeploy, see [Configure Existing On\-Premises Instances by Using AWS CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/how-to-configure-on-premises-host.html) in the *AWS CodeDeploy User Guide*\.

For information on using tags and tag groups to help manage your Amazon EC2 instances and on\-premises instances, see [Tagging Instances for Deployment Groups in AWS CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-tagging.html) in the *AWS CodeDeploy User Guide*\.

## Syntax<a name="w4ab1c21c10c72c21c69b7"></a>

### JSON<a name="aws-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-syntax.json"></a>

```
{
  "[Key](#cfn-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-key)" : String,
  "[Type](#cfn-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-type)" : String,
  "[Value](#cfn-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-value)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-syntax.yaml"></a>

```
[Key](#cfn-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-key): String
[Type](#cfn-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-type): String
[Value](#cfn-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-value): String
```

## Properties<a name="w4ab1c21c10c72c21c69b9"></a>

`Key`  <a name="cfn-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-key"></a>
Filter on\-premises instances with this key\.  
*Required*: No  
*Type*: String

`Type`  <a name="cfn-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-type"></a>
The filter type\. For example, you can filter on\-premises instances by the key, tag value, or both\. For valid values, see [EC2TagFilter](https://docs.aws.amazon.com/codedeploy/latest/APIReference/API_EC2TagFilter.html) in the *AWS CodeDeploy API Reference*\.  
*Required*: No  
*Type*: String

`Value`  <a name="cfn-properties-codedeploy-deploymentgroup-onpremisesinstancetagfilters-value"></a>
Filter on\-premises instances with this tag value\.  
*Required*: No  
*Type*: String