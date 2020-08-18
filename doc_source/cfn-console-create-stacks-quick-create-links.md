# Creating quick\-create links for stacks<a name="cfn-console-create-stacks-quick-create-links"></a>

Use quick\-create links to get stacks up and running quickly from the AWS CloudFormation console\. You can specify the template URL, stack name, and template parameters in URL query parameters to prepopulate a single **Create Stack Wizard** page\. This simplifies the process of creating stacks by reducing the number of wizard pages and the amount of user input that's required\. It also optimizes template reuse because you can create multiple URLs that specify different values for the same template\.

## Supported parameters<a name="cfn-console-create-stacks-quick-create-links-parameters"></a>

AWS CloudFormation supports the following URL query parameters:

`templateURL`  
Required\. Specifies the URL of the stack template\. URL encoding is supported, but it isn't required\.

`stackName`  
Optional\. Specifies the stack name\.A stack name can contain only alphanumeric characters \(case\-sensitive\) and hyphens\. It must start with an alphabetic character and can't be longer than 128 characters\.

Any parameter in the stack template that isn't a `NoEcho` parameter type  
Optional\. Use the format `param_parameterName` to specify template parameters in the URL query string\. The URL parameter must include the `param_` prefix, and the parameter name segment must exactly match the parameter name in the template\. For example: `param_DBName`\.  
AWS CloudFormation ignores parameters that don't exist in the template, and any parameters defined with their `NoEcho` property set to `true` types \(typically, user names and passwords\)\. URL parameters override default values that are specified in the template\. You can include as many parameters as needed\.  
Rather than embedding sensitive information directly in your AWS CloudFormation templates, we recommend you use dynamic parameters in the stack template to reference sensitive information that is stored and managed outside of CloudFormation, such as in the AWS Systems Manager Parameter Store or AWS Secrets Manager\.  
For more information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

All query parameter names are case sensitive\. Users can overwrite these values in the console before creating the stack\.

## Example<a name="cfn-console-create-stacks-quick-create-links-example"></a>

The following example is based on the [ WordPress basic single instance](https://s3.eu-central-1.amazonaws.com/cloudformation-templates-eu-central-1/WordPress_Single_Instance.template) sample template\. The query string includes the required `templateURL` parameter and the `stackName`, `DBName`, `InstanceType`, and `KeyName` parameters\.

The following URL has line breaks added for clarity\.

```
https://eu-central-1.console.aws.amazon.com/cloudformation/home?region=eu-central-1#/stacks/create/review
   ?templateURL=https://s3.eu-central-1.amazonaws.com/cloudformation-templates-eu-central-1/WordPress_Single_Instance.template
   &stackName=MyWPBlog
   &param_DBName=mywpblog
   &param_InstanceType=t2.medium
   &param_KeyName=MyKeyPair
```

The following URL includes the same parameters as the previous example, but the line breaks are removed\. This is the actual URL format\.

```
https://eu-central-1.console.aws.amazon.com/cloudformation/home?region=eu-central-1#/stacks/create/review?templateURL=https://s3.eu-central-1.amazonaws.com/cloudformation-templates-eu-central-1/WordPress_Single_Instance.template&stackName=MyWPBlog&param_DBName=mywpblog&param_InstanceType=t2.medium&param_KeyName=MyKeyPair
```

The example URL opens the **Create Stack Wizard** in the console, with the supplied values automatically used for the parameters\.

![\[Parameters in the Create Stack Wizard that are prepopulated with the values from the URL query string.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-quick-create-link-example.png)