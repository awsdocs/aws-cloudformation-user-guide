# AWS CloudFormation configuration properties reference<a name="continuous-delivery-codepipeline-action-reference"></a>

When you build a CodePipeline pipeline, you add a `Deploy` action to the pipeline with AWS CloudFormation as a provider\. You then must specify which AWS CloudFormation action the pipeline invokes and the action's settings\. This topic describes the AWS CloudFormation configuration properties\. To specify properties, you can use the CodePipeline console, or you can create a [JSON object](https://docs.aws.amazon.com/codepipeline/latest/userguide/how-to-create-pipelines.html#how-to-create-pipeline-cli) to use for the AWS CLI, CodePipeline API, or AWS CloudFormation templates\.

**Topics**
+ [Configuration properties \(console\)](#w7739ab1c21c14b7)
+ [Configuration properties \(JSON object\)](#w7739ab1c21c14b9)
+ [See also](#w7739ab1c21c14c13)

## Configuration properties \(console\)<a name="w7739ab1c21c14b7"></a>

The CodePipeline [console](https://console.aws.amazon.com/codepipeline/) shows the configuration properties and indicates the properties that are required based on the action mode that you choose\.

**Note**  
When you create a pipeline, you can specify the **Create or update a stack** or **Create or replace a change set** action modes only\. Properties in the **Advanced** section are available only when you edit a pipeline\.

**Action mode**  
The AWS CloudFormation action that CodePipeline invokes when processing the associated stage\. Choose one of the following action modes:  
+ **Create or replace a change set** creates the change set if it doesn't exist based on the stack name and template that you submit\. If the change set exists, AWS CloudFormation deletes it, and then creates a new one\.
+ **Create or update a stack** creates the stack if the specified stack doesn't exist\. If the stack exists, AWS CloudFormation updates the stack\. Use this action to update existing stacks\. CodePipeline won't replace the stack\.
+ **Delete a stack** deletes a stack\. If you specify a stack that doesn't exist, the action is completed successfully without deleting a stack\.
+ **Execute a change set** executes a change set\.
+ **Replace a failed stack** creates the stack if the specified stack doesn't exist\. If the stack exists and is in a failed state \(reported as `ROLLBACK_COMPLETE`, `ROLLBACK_FAILED`, `CREATE_FAILED`, `DELETE_FAILED`, or `UPDATE_ROLLBACK_FAILED`\), AWS CloudFormation deletes the stack and then creates a new one\. If the stack isn't in a failed state, AWS CloudFormation updates it\. Use this action to replace failed stacks without recovering or troubleshooting them\. You would typically choose this mode for testing\.

**Stack name**  
The name that is associated with an existing stack or a stack you want to create\. The name must be unique in the AWS Region in which you are creating the stack\.  
A stack name can contain only alphanumeric characters \(case sensitive\) and hyphens\. It must start with an alphabetic character and cannot be longer than 128 characters\.

**Change set name**  
The name of an existing change set or a new change set that you want to create for the specified stack\. 

**Template**  
The location of an AWS CloudFormation template file, which follows the format `ArtifactName::TemplateFileName`\.

**Template configuration**  
The location of a template configuration file, which follows the format `ArtifactName::TemplateConfigurationFileName`\. The template configuration file can contain template parameter values, a stack policy, and tags\. If you include sensitive information, such as passwords, restrict access to this file\. For more information, see [AWS CloudFormation artifacts](continuous-delivery-codepipeline-cfn-artifacts.md)\.

**Capabilities**  
For stacks that contain certain resources, explicit acknowledgement that AWS CloudFormation might create or update those resources\. For example, you must specify `CAPABILITY_IAM` if your stack template contains AWS Identity and Access Management \(IAM\) resources\. For more information, see [CreateStack request parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html)\.  
If you have IAM resources in your stack template, you must specify this property\.  
You can specify more than one capability\.

**Role name**  
The name of the IAM service role that AWS CloudFormation assumes when it operates on resources in the specified stack\.

**Output file name**  
In the **Advanced** section, you can specify an output file name, such as `CreateStackOutput.json`, that CodePipeline adds to the [output artifact](https://docs.aws.amazon.com/codepipeline/latest/userguide/concepts.html) after it performs the specified action\. The output artifact contains a JSON file with the contents of the `Outputs` section of the AWS CloudFormation template\.  
If you don't specify a name, CodePipeline doesn't generate an output artifact\.

**Parameter overrides**  
Parameters are defined in your template and allow you to input custom values when you create or update a stack\. You can specify a JSON object that overrides template parameter values in the template configuration file\. All parameter names must be present in the stack template\. For more information, see [Defining a parameter in a template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)\.  
There is a maximum size limit of 1 kilobyte for the JSON object that can be stored in the `ParameterOverrides` property\.
We recommend that you use the template configuration file to specify most of your parameter values\. Use parameter overrides to specify dynamic parameter values only\. Dynamic parameters are unknown until you run the pipeline\.  
The following example defines a value for the `ParameterName` parameter by using a parameter override function\. The function retrieves a value from a CodePipeline input artifact\. For more information about parameter override functions, see [Using parameter override functions with CodePipeline pipelines](continuous-delivery-codepipeline-parameter-override-functions.md)\.  

```
{
  "ParameterName" : { "Fn::GetParam" : ["ArtifactName", "config-file-name.json", "ParamName"]}
}
```

## Configuration properties \(JSON object\)<a name="w7739ab1c21c14b9"></a>

When you specify `CloudFormation` as a provider for a stage action, define the following properties in the `Configuration` property\. Use the [JSON object](https://docs.aws.amazon.com/codepipeline/latest/userguide/how-to-create-pipelines.html#how-to-create-pipeline-cli) for the AWS CLI, CodePipeline API, or AWS CloudFormation templates\. For examples, see [Walkthrough: Building a pipeline for test and production stacks](continuous-delivery-codepipeline-basic-walkthrough.md) and [AWS CloudFormation configuration properties reference](#continuous-delivery-codepipeline-action-reference)\.

`ActionMode`  
The AWS CloudFormation action that CodePipeline invokes when it processes the associated stage\. Specify only one of the following action modes:  
+ `CHANGE_SET_EXECUTE` executes a change set\.
+ `CHANGE_SET_REPLACE` creates the change set, if it doesn't exist, based on the stack name and template that you submit\. If the change set exists, AWS CloudFormation deletes it, and then creates a new one\.
+ `CREATE_UPDATE` creates the stack if the specified stack doesn't exist\. If the stack exists, AWS CloudFormation updates the stack\. Use this action to update existing stacks\. CodePipeline won't replace the stack\.
+ `DELETE_ONLY` deletes a stack\. If you specify a stack that doesn't exist, the action is completed successfully without deleting a stack\.
+ `REPLACE_ON_FAILURE` creates a stack, if the specified stack doesn't exist\. If the stack exists and is in a failed state \(reported as `ROLLBACK_COMPLETE`, `ROLLBACK_FAILED`, `CREATE_FAILED`, `DELETE_FAILED`, or `UPDATE_ROLLBACK_FAILED`\), AWS CloudFormation deletes the stack and then creates a new stack\. If the stack isn't in a failed state, AWS CloudFormation updates it\. Use this action to automatically replace failed stacks without recovering or troubleshooting them\. You would typically choose this mode for testing\.
This property is required\.

`Capabilities`  
For stacks that contain certain resources, explicit acknowledgement that AWS CloudFormation might create or update those resources\. For example, you must specify `CAPABILITY_IAM` if your stack template contains AWS Identity and Access Management \(IAM\) resources\. For more information, see [CreateStack request parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html)\.  
This property is conditional\. If you have IAM resources in your stack template, you must specify this property\.  
You can specify multiple capabilities\. The following example adds the CAPABILITY\_IAM and CAPABILITY\_AUTO\_EXPAND properties to the template:  

```
configuration:
  ActionMode: CHANGE_SET_REPLACE
  Capabilities: CAPABILITY_IAM,CAPABILITY_AUTO_EXPAND
  ChangeSetName: pipeline-changeset
  RoleArn: CloudFormation_Role_ARN
  StackName: my-pipeline-stack
  TemplateConfiguration: 'my-pipeline-stack::template-configuration.json'
  TemplatePath: 'my-pipeline-stack::template-export.yml'
```

```
 "configuration": {
        "ActionMode": "CHANGE_SET_REPLACE",
        "Capabilities": "CAPABILITY_IAM,CAPABILITY_AUTO_EXPAND",
        "ChangeSetName": "pipeline-changeset",
        "RoleArn": "CloudFormation_Role_ARN",
        "StackName": "my-pipeline-stack",
        "TemplateConfiguration": "my-pipeline-stack::template-configuration.json",
        "TemplatePath": "my-pipeline-stack::template-export.yml"
    }
```

`ChangeSetName`  
The name of an existing change set or a new change set that you want to create for the specified stack\.  
This property is required for the following action modes: `CHANGE_SET_REPLACE` and `CHANGE_SET_EXECUTE`\. For all other action modes, this property is ignored\.

`OutputFileName`  
A name for the output file, such as `CreateStackOutput.json`\. CodePipeline adds the file to the [output artifact](https://docs.aws.amazon.com/codepipeline/latest/userguide/concepts.html) after it performs the specified action\. The output artifact contains a JSON file with the contents of the `Outputs` section of the AWS CloudFormation template\.  
This property is optional\. If you don't specify a name, CodePipeline doesn't generate an output artifact\.

`ParameterOverrides`  
Parameters are defined in your template and allow you to input custom values when you create or update a stack\. You can specify a JSON object that overrides template parameter values in the template configuration file\. All parameter names must be present in the stack template\. For more information, see [Defining a parameter in a template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)\.  
The following example adds the `InstanceType` and `KeyName` parameter overrides to the template:  

```
configuration:
  ActionMode: CHANGE_SET_REPLACE
  Capabilities: CAPABILITY_NAMED_IAM
  ChangeSetName: pipeline-changeset
  ParameterOverrides: '{"InstanceType": "t2.small","KeyName": "my-keypair"}'
  RoleArn: CloudFormation_Role_ARN
  StackName: my-pipeline-stack
  TemplateConfiguration: 'my-pipeline-stack::template-configuration.json'
  TemplatePath: 'my-pipeline-stack::template-export.yml'
```

```
"configuration": {
        "ActionMode": "CHANGE_SET_REPLACE",
        "Capabilities": "CAPABILITY_NAMED_IAM",
        "ChangeSetName": "pipeline-changeset",
        "ParameterOverrides": "{\"InstanceType\": \"t2.small\",\"KeyName\": \"my-keypair\"}",
        "RoleArn": "CloudFormation_Role_ARN",
        "StackName": "my-pipeline-stack",
        "TemplateConfiguration": "my-pipeline-stack::template-configuration.json",
        "TemplatePath": "my-pipeline-stack::template-export.yml"
    }
```
The maximum size for the JSON object that can be stored in the `ParameterOverrides` property is 1 kilobyte\.
We recommend that you use the template configuration file to specify most of your parameter values\. Use parameter overrides to specify dynamic parameter values only\. Dynamic parameter values are unknown until you run the pipeline\.  
The following example defines a value for the `ParameterName` parameter by using a parameter override function\. The function retrieves a value from a CodePipeline input artifact\. For more information about parameter override functions, see [Using parameter override functions with CodePipeline pipelines](continuous-delivery-codepipeline-parameter-override-functions.md)\.  

```
{
  "ParameterName" : { "Fn::GetParam" : ["ArtifactName", "config-file-name.json", "ParamName"]}
}
```
This property is optional\.

`RoleArn`  
The Amazon Resource Name \(ARN\) of the IAM service role that AWS CloudFormation assumes when it operates on resources in a stack\.  
This property is required for the following action modes: `CREATE_UPDATE`, `REPLACE_ON_FAILURE`, `DELETE_ONLY`, and `CHANGE_SET_REPLACE`\. `RoleArn` is not applied when executing a change set\. If you do not use CodePipeline to create the change set, make sure that the change set or stack has an associated role\.

`StackName`  
The name of an existing stack or a stack that you want to create\.  
This property is required for all action modes\.

`TemplateConfiguration`  
`TemplateConfiguration` is the template configuration file\. You include the file in an input artifact to this action\. The template configuration filename follows this format:   
`Artifactname::TemplateConfigurationFileName`  
`Artifactname` is the input artifact name as it appears in CodePipeline\. For example, a source stage with the artifact name of `SourceArtifact` and a `test-configuration.json` file name creates a `TemplateConfiguration` name as shown in this example:  

```
"TemplateConfiguration": "SourceArtifact::test-configuration.json"
```
The template configuration file can contain template parameter values and a stack policy\. If you include sensitive information, such as passwords, restrict access to this file\. For an example template configuration file, see [AWS CloudFormation artifacts](continuous-delivery-codepipeline-cfn-artifacts.md)\.  
This property is optional\.

`TemplatePath`  
`TemplatePath` represents the AWS CloudFormation template file\. You include the file in an input artifact to this action\. The file name follows this format:  
`Artifactname::TemplateFileName`  
`Artifactname` is the input artifact name as it appears in CodePipeline\. For example, a source stage with the artifact name of `SourceArtifact` and a `template.yaml` file name creates a `TemplatePath` name, as shown in this example:  

```
"TemplatePath": "SourceArtifact::template.yaml"
```
This property is required for the following action modes: `CREATE_UPDATE`, `REPLACE_ON_FAILURE`, and `CHANGE_SET_REPLACE`\. For all other action modes, this property is ignored\.

## See also<a name="w7739ab1c21c14c13"></a>

The following related resources can help you as you work with these parameters\.
+ For more information about the AWS CloudFormation action parameters in CodePipeline, see the [AWS CloudFormation](https://docs.aws.amazon.com/codepipeline/latest/userguide/action-reference-CloudFormation.html) action configuration reference in the *AWS CodePipeline User Guide*\.
+ For example template values by action provider, such as for the `Owner` field or the `configuration` fields, see the [Action structure reference](https://docs.aws.amazon.com/codepipeline/latest/userguide/action-reference.html) in the *AWS CodePipeline User Guide*\.
+ To download example pipeline stack templates in YAML or JSON format, see the tutorials under [Create a pipeline with AWS CloudFormation](https://docs.aws.amazon.com/codepipeline/latest/userguide/tutorials-cloudformation.html) in the *AWS CodePipeline User Guide*\.
+ For an example template configuration file, see [AWS CloudFormation artifacts](https://docs.aws.amazon.com/codepipeline/latest/userguide/continuous-delivery-codepipeline-cfn-artifacts.html)\.