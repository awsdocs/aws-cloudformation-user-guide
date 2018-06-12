# AWS::CodeDeploy::Application<a name="aws-resource-codedeploy-application"></a>

The `AWS::CodeDeploy::Application` resource creates an AWS CodeDeploy application\. In AWS CodeDeploy, an application is a name that functions as a container to ensure that the correct combination of revision, deployment configuration, and deployment group are referenced during a deployment\. You can use the `AWS::CodeDeploy::DeploymentGroup` resource to associate the application with an AWS CodeDeploy deployment group\. For more information, see [AWS CodeDeploy Deployments](http://docs.aws.amazon.com/codedeploy/latest/userguide/deployment-steps.html) in the *AWS CodeDeploy User Guide*\.

**Topics**
+ [Syntax](#aws-resource-codedeploy-application-syntax)
+ [Properties](#aws-resource-codedeploy-application-properties)
+ [Return Value](#aws-resource-codedeploy-application-returnvalues)
+ [Example](#aws-resource-codedeploy-application-examples)
+ [Related Resources](#w3ab2c21c10d250c15)

## Syntax<a name="aws-resource-codedeploy-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codedeploy-application-syntax.json"></a>

```
{
  "Type" : "AWS::CodeDeploy::Application",
  "Properties" : {
    "[ApplicationName](#cfn-codedeploy-application-applicationname)" : String,
    "[ComputePlatform](#cfn-codedeploy-application-computeplatform)" : String
  }
}
```

### YAML<a name="aws-resource-codedeploy-application-syntax.yaml"></a>

```
Type: "AWS::CodeDeploy::Application"
Properties:
  [ApplicationName](#cfn-codedeploy-application-applicationname): String	    
  [ComputePlatform](#cfn-codedeploy-application-computeplatform): String
```

## Properties<a name="aws-resource-codedeploy-application-properties"></a>

`ApplicationName`  <a name="cfn-codedeploy-application-applicationname"></a>
A name for the application\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the application name\. For more information, see [Name Type](aws-properties-name.md)\.  
*Required*: No  
*Type*: String  
*Update requires*: Updates are not supported\.

`ComputePlatform`  <a name="cfn-codedeploy-application-computeplatform"></a>
The compute platform that AWS CodeDeploy deploys the application to\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Value<a name="aws-resource-codedeploy-application-returnvalues"></a>

### Ref<a name="w3ab2c21c10d250c11b2"></a>

When you pass the logical ID of an `AWS::CodeDeploy::Application` resource to the intrinsic `Ref` function, the function returns the application name, such as `myapplication-a123d0d1`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="aws-resource-codedeploy-application-examples"></a>

The following example creates an AWS CodeDeploy application with a `Lambda` compute platform\.

### JSON<a name="aws-resource-codedeploy-application-example.json"></a>

```
"CodeDeployApplication": {
  "Type": "AWS::CodeDeploy::Application",
  "Properties": {
    "ComputePlatform": "Lambda"
  }
}
```

### YAML<a name="aws-resource-codedeploy-application-example.yaml"></a>

```
CodeDeployApplication:
  Type: 'AWS::CodeDeploy::Application'
  Properties:
    ComputePlatform: Lambda
```

## Related Resources<a name="w3ab2c21c10d250c15"></a>

For configuring your deployment and specifying your application revisions, see [AWS::CodeDeploy::DeploymentConfig](aws-resource-codedeploy-deploymentconfig.md) and [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md)\.