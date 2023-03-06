# AWS::Lambda::Function RuntimeManagementConfig<a name="aws-properties-lambda-function-runtimemanagementconfig"></a>

Sets the runtime management configuration for a function's version\. For more information, see [Runtime updates](https://docs.aws.amazon.com/lambda/latest/dg/runtimes-update.html)\.

## Syntax<a name="aws-properties-lambda-function-runtimemanagementconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-function-runtimemanagementconfig-syntax.json"></a>

```
{
  "[RuntimeVersionArn](#cfn-lambda-function-runtimemanagementconfig-runtimeversionarn)" : String,
  "[UpdateRuntimeOn](#cfn-lambda-function-runtimemanagementconfig-updateruntimeon)" : String
}
```

### YAML<a name="aws-properties-lambda-function-runtimemanagementconfig-syntax.yaml"></a>

```
  [RuntimeVersionArn](#cfn-lambda-function-runtimemanagementconfig-runtimeversionarn): String
  [UpdateRuntimeOn](#cfn-lambda-function-runtimemanagementconfig-updateruntimeon): String
```

## Properties<a name="aws-properties-lambda-function-runtimemanagementconfig-properties"></a>

`RuntimeVersionArn`  <a name="cfn-lambda-function-runtimemanagementconfig-runtimeversionarn"></a>
The ARN of the runtime version you want the function to use\.  
This is only required if you're using the **Manual** runtime update mode\.
*Required*: No  
*Type*: String  
*Minimum*: `26`  
*Maximum*: `2048`  
*Pattern*: `^arn:(aws[a-zA-Z-]*):lambda:[a-z]{2}((-gov)|(-iso(b?)))?-[a-z]+-\d{1}::runtime:.+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateRuntimeOn`  <a name="cfn-lambda-function-runtimemanagementconfig-updateruntimeon"></a>
Specify the runtime update mode\.  
+ **Auto \(default\)** \- Automatically update to the most recent and secure runtime version using a [Two\-phase runtime version rollout](https://docs.aws.amazon.com/lambda/latest/dg/runtimes-update.html#runtime-management-two-phase)\. This is the best choice for most customers to ensure they always benefit from runtime updates\.
+ **FunctionUpdate** \- Lambda updates the runtime of you function to the most recent and secure runtime version when you update your function\. This approach synchronizes runtime updates with function deployments, giving you control over when runtime updates are applied and allowing you to detect and mitigate rare runtime update incompatibilities early\. When using this setting, you need to regularly update your functions to keep their runtime up\-to\-date\.
+ **Manual** \- You specify a runtime version in your function configuration\. The function will use this runtime version indefinitely\. In the rare case where a new runtime version is incompatible with an existing function, this allows you to roll back your function to an earlier runtime version\. For more information, see [Roll back a runtime version](https://docs.aws.amazon.com/lambda/latest/dg/runtimes-update.html#runtime-management-rollback)\.
*Valid Values*: `Auto` \| `FunctionUpdate` \| `Manual`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)