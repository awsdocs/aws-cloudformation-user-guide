# AWS::CodeDeploy::DeploymentGroup EC2TagFilter<a name="aws-properties-codedeploy-deploymentgroup-ec2tagfilter"></a>

Information about an EC2 tag filter\.

For more information about using tags and tag groups to help manage your Amazon EC2 instances and on\-premises instances, see [ Tagging Instances for Deployment Groups in AWS CodeDeploy](https://docs.aws.amazon.com/codedeploy/latest/userguide/instances-tagging.html) in the *AWS CodeDeploy User Guide*\.

## Syntax<a name="aws-properties-codedeploy-deploymentgroup-ec2tagfilter-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codedeploy-deploymentgroup-ec2tagfilter-syntax.json"></a>

```
{
  "[Key](#cfn-codedeploy-deploymentgroup-ec2tagfilter-key)" : String,
  "[Type](#cfn-codedeploy-deploymentgroup-ec2tagfilter-type)" : String,
  "[Value](#cfn-codedeploy-deploymentgroup-ec2tagfilter-value)" : String
}
```

### YAML<a name="aws-properties-codedeploy-deploymentgroup-ec2tagfilter-syntax.yaml"></a>

```
  [Key](#cfn-codedeploy-deploymentgroup-ec2tagfilter-key): String
  [Type](#cfn-codedeploy-deploymentgroup-ec2tagfilter-type): String
  [Value](#cfn-codedeploy-deploymentgroup-ec2tagfilter-value): String
```

## Properties<a name="aws-properties-codedeploy-deploymentgroup-ec2tagfilter-properties"></a>

`Key`  <a name="cfn-codedeploy-deploymentgroup-ec2tagfilter-key"></a>
The tag filter key\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-codedeploy-deploymentgroup-ec2tagfilter-type"></a>
The tag filter type:  
+  `KEY_ONLY`: Key only\.
+  `VALUE_ONLY`: Value only\.
+  `KEY_AND_VALUE`: Key and value\.
*Required*: No  
*Type*: String  
*Allowed values*: `KEY_AND_VALUE | KEY_ONLY | VALUE_ONLY`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-codedeploy-deploymentgroup-ec2tagfilter-value"></a>
The tag filter value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)