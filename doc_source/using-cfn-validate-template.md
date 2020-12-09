# Validating a template<a name="using-cfn-validate-template"></a>

To check your template file for syntax errors, you can use the [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/validate-template.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/validate-template.html) command\.

**Note**  
The `aws cloudformation validate-template` command is designed to check only the syntax of your template\. It does not ensure that the property values that you have specified for a resource are valid for that resource\. Nor does it determine the number of resources that will exist when the stack is created\.

To check the operational validity, you need to attempt to create the stack\. There is no sandbox or test area for AWS CloudFormation stacks, so you are charged for the resources you create during testing\.

During validation, AWS CloudFormation first checks if the template is valid JSON\. If it isn't, AWS CloudFormation checks if the template is valid YAML\. If both checks fail, AWS CloudFormation returns a template validation error\. You can validate templates locally by using the `--template-body` parameter, or remotely with the `--template-url` parameter\. The following example validates a template in a remote location:

```
PROMPT> aws cloudformation validate-template --template-url https://s3.amazonaws.com/cloudformation-templates-us-east-1/S3_Bucket.template
{
    "Description": "AWS CloudFormation Sample Template S3_Bucket: Sample template showing how to create a publicly accessible S3 bucket. **WARNING** This template creates an S3 bucket.
You will be billed for the AWS resources used if you create a stack from this template.",
    "Parameters": [],
    "Capabilities": []
}
```

The expected result is no error message, with information about all parameters listed\.

The following example shows an error with a local template file:

```
PROMPT> aws cloudformation validate-template --template-body file:///home/local/test/sampletemplate.json
{
    "ResponseMetadata": {
        "RequestId": "4ae33ec0-1988-11e3-818b-e15a6df955cd"
    },
    "Errors": [
        {
            "Message": "Template format error: JSON not well-formed. (line 11, column 8)",
            "Code": "ValidationError",
            "Type": "Sender"
        }
    ],
    "Capabilities": [],
    "Parameters": []
}
A client error (ValidationError) occurred: Template format error: JSON not well-formed. (line 11, column 8)
```