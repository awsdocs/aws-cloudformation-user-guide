# AWS CloudFormation Configuration Properties Reference<a name="continuous-delivery-codepipeline-action-reference"></a>

When you build an AWS CodePipeline pipeline, you add a `Deploy` action to the pipeline with AWS CloudFormation as a provider\. You then must specify which AWS CloudFormation action the pipeline invokes and the action's settings\. This topic describes the AWS CloudFormation configuration properties\. To specify properties, you can use the AWS CodePipeline console, or you can create a [JSON object](http://docs.aws.amazon.com/codepipeline/latest/userguide/how-to-create-pipelines.html#how-to-create-pipeline-cli) to use for the AWS CLI, AWS CodePipeline API, or AWS CloudFormation templates\.

**Topics**
+ [Configuration Properties \(Console\)](#w3ab2c13c13b7)
+ [Configuration Properties \(JSON Object\)](#w3ab2c13c13b9)

## Configuration Properties \(Console\)<a name="w3ab2c13c13b7"></a>

The AWS CodePipeline [console](https://console.aws.amazon.com/codepipeline/) shows the configuration properties and indicates the properties that are required based on the `Action mode` that you choose\.

**Note**  
When you create a new pipeline, you can specify only the **Create or update a stack** or **Create or replace a change set** action modes\. Also, properties in the **Advanced** section are available only when you edit an existing pipeline\.

**Action mode**  
The AWS CloudFormation action that AWS CodePipeline invokes when processing the associated stage\. Choose one of the following action modes:  
+ **Create or replace a change set** creates the change set if it doesn't exist based on the stack name and template that you submit\. If the change set exists, AWS CloudFormation deletes it, and then creates a new one\.
+ **Create or update a stack** creates the stack if the specified stack doesn't exist\. If the stack exists, AWS CloudFormation updates the stack\. Use this action to update existing stacks\. AWS CodePipeline won't replace the stack\.
+ **Delete a stack** deletes a stack\. If you specify a stack that doesn't exist, the action completes successfully without deleting a stack\.
+ **Execute a change set** executes a change set\.
+ **Replace a failed stack** creates the stack if the specified stack doesn't exist\. If the stack exists and is in a failed state \(reported as `ROLLBACK_COMPLETE`, `ROLLBACK_FAILED`, `CREATE_FAILED`, `DELETE_FAILED`, or `UPDATE_ROLLBACK_FAILED`\), AWS CloudFormation deletes the stack and then creates a new stack\. If the stack isn't in a failed state, AWS CloudFormation updates it\. Use this action to automatically replace failed stacks without recovering or troubleshooting them\. You would typically choose this mode for testing\.

**Stack name**  
The name of an existing stack or a stack that you want to create\.

**Change set name**  
The name of an existing change set or a new change set that you want to create for the specified stack\.

**Template**  
The location of an AWS CloudFormation template file, which follows the format `ArtifactName::TemplateFileName`\.

**Template configuration**  
The location of a template configuration file, which follows the format `ArtifactName::TemplateConfigurationFileName`\. The template configuration file can contain template parameter values and a stack policy\. If you include sensitive information, such as passwords, restrict access to this file\. For more information, see [AWS CloudFormation Artifacts](continuous-delivery-codepipeline-cfn-artifacts.md)\.

**Capabilities**  
For stacks that contain certain resources, explicit acknowledgement that AWS CloudFormation might create or update those resources\. For example, you must specify `CAPABILITY_IAM` if your stack template contains AWS Identity and Access Management \(IAM\) resources\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](using-iam-template.md#using-iam-capabilities)\.  
If you have IAM resources in your stack template, you must specify this property\.

**Role name**  
The name of the IAM service role that AWS CloudFormation assumes when it operates on resources in the specified stack\.

**Output file name**  
In the **Advanced** section, you can specify an output file name, such as `CreateStackOutput.json`, that AWS CodePipeline adds to the [output artifact](http://docs.aws.amazon.com/codepipeline/latest/userguide/concepts.html) after performing the specified action\.  
If you don't specify a name, AWS CodePipeline doesn't generate an output artifact\.

**Parameter overrides**  
In the **Advanced** section, you can specify a JSON object that overrides template parameter values in the template configuration file\. All parameter names must be present in the stack template\.  
There is a maximum size limit of 1 kilobyte for the JSON object that can be stored in the `ParameterOverrides` property\.
We recommend that you use the template configuration file to specify most of your parameter values\. Use parameter overrides to specify only dynamic parameter values \(values that are unknown until you run the pipeline\)\.  
The following example defines a value for the `ParameterName` parameter by using a parameter override function\. The function retrieves a value from an AWS CodePipeline input artifact\. For more information about parameter override functions, see [Using Parameter Override Functions with AWS CodePipeline Pipelines](continuous-delivery-codepipeline-parameter-override-functions.md)\.  

```
{
  "ParameterName" : { "Fn::GetParam" : ["ArtifactName", "config-file-name.json", "ParamName"]}
}
```

## Configuration Properties \(JSON Object\)<a name="w3ab2c13c13b9"></a>

When you specify `CloudFormation` as a provider for a stage action, define the following properties within the `Configuration` property\. Use the [JSON object](http://docs.aws.amazon.com/codepipeline/latest/userguide/how-to-create-pipelines.html#how-to-create-pipeline-cli) for the AWS CLI, AWS CodePipeline API, or AWS CloudFormation templates\. For examples, see [Walkthrough: Building a Pipeline for Test and Production Stacks](continuous-delivery-codepipeline-basic-walkthrough.md)

`ActionMode`  
The AWS CloudFormation action that AWS CodePipeline invokes when processing the associated stage\. Specify only one of the following action modes:  
+ `CHANGE_SET_EXECUTE` executes a change set\.
+ `CHANGE_SET_REPLACE` creates the change set if it doesn't exist based on the stack name and template that you submit\. If the change set exists, AWS CloudFormation deletes it, and then creates a new one\.
+ `CREATE_UPDATE` creates the stack if the specified stack doesn't exist\. If the stack exists, AWS CloudFormation updates the stack\. Use this action to update existing stacks\. AWS CodePipeline won't replace the stack\.
+ `DELETE_ONLY` deletes a stack\. If you specify a stack that doesn't exist, the action completes successfully without deleting a stack\.
+ `REPLACE_ON_FAILURE` creates a stack if the specified stack doesn't exist\. If the stack exists and is in a failed state \(reported as `ROLLBACK_COMPLETE`, `ROLLBACK_FAILED`, `CREATE_FAILED`, `DELETE_FAILED`, or `UPDATE_ROLLBACK_FAILED`\), AWS CloudFormation deletes the stack and then creates a new stack\. If the stack isn't in a failed state, AWS CloudFormation updates it\. Use this action to automatically replace failed stacks without recovering or troubleshooting them\. You would typically choose this mode for testing\.
This property is required\.

`Capabilities`  
For stacks that contain certain resources, explicit acknowledgement that AWS CloudFormation might create or update those resources\. For example, you must specify `CAPABILITY_IAM` if your stack template contains AWS Identity and Access Management \(IAM\) resources\. For more information, see [Acknowledging IAM Resources in AWS CloudFormation Templates](using-iam-template.md#using-iam-capabilities)\.  
This property is conditional\. If you have IAM resources in your stack template, you must specify this property\.

`ChangeSetName`  
The name of an existing change set or a new change set that you want to create for the specified stack\.  
This property is required for the following action modes: `CHANGE_SET_REPLACE` and `CHANGE_SET_EXECUTE`\. For all other action modes, this property is ignored\.

`OutputFileName`  
A name for the output file, such as `CreateStackOutput.json`\. AWS CodePipeline adds the file to the [output artifact](http://docs.aws.amazon.com/codepipeline/latest/userguide/concepts.html) after performing the specified action\.  
This property is optional\. If you don't specify a name, AWS CodePipeline doesn't generate an output artifact\.

`ParameterOverrides`  
A JSON object that specifies values for template parameters\. If you specify parameters that are also specified in the template configuration file, these values override them\. All parameter names must be present in the stack template\.  
There is a maximum size limit of 1 kilobyte for the JSON object that can be stored in the `ParameterOverrides` property\.
We recommend that you use the template configuration file to specify most of your parameter values\. Use parameter overrides to specify only dynamic parameter values \(values that are unknown until you run the pipeline\)\.  
The following example defines a value for the `ParameterName` parameter by using a parameter override function\. The function retrieves a value from an AWS CodePipeline input artifact\. For more information about parameter override functions, see [Using Parameter Override Functions with AWS CodePipeline Pipelines](continuous-delivery-codepipeline-parameter-override-functions.md)\.  

```
{
  "ParameterName" : { "Fn::GetParam" : ["ArtifactName", "config-file-name.json", "ParamName"]}
}
```
This property is optional\.

`RoleArn`  
The Amazon Resource Name \(ARN\) of the IAM service role that AWS CloudFormation assumes when it operates on resources in a stack\.  
This property is required for the following action modes: `CREATE_UPDATE`, `REPLACE_ON_FAILURE`, `DELETE_ONLY`, and `CHANGE_SET_REPLACE`\. Note: `RoleArn` is not applied when executing a change set\. If you do not use CodePipeline to create the change set, you must ensure that the change set or stack has an associated role\.

`StackName`  
The name of an existing stack or a stack that you want to create\.  
This property is required for all action modes\.

`TemplateConfiguration`  
The location of a template configuration file, which follows the format `ArtifactName::TemplateConfigurationFileName`\. The template configuration file can contain template parameter values and a stack policy\. Note that if you include sensitive information, such as passwords, restrict access to this file\. For more information, see [AWS CloudFormation Artifacts](continuous-delivery-codepipeline-cfn-artifacts.md)\.  
This property is optional\.

`TemplatePath`  
The location of an AWS CloudFormation template file, which follows the format `ArtifactName::TemplateFileName`\.   
This property is required for the following action modes: `CREATE_UPDATE`, `REPLACE_ON_FAILURE`, and `CHANGE_SET_REPLACE`\. For all other action modes, this property is ignored\.