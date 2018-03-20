# AWS CloudFormation Limits<a name="cloudformation-limits"></a>

Your AWS account has AWS CloudFormation limits that you might need to know when authoring templates and creating stacks\. By understanding these limits, you can avoid limitation errors that would require you to redesign your templates or stacks\.


**AWS CloudFormation limits**  

|  Limit  |  Description  |  Value  |  Tuning Strategy  | 
| --- | --- | --- | --- | 
|  [cfn\-signal wait condition data](cfn-signal.md)  |  Maximum amount of data that cfn\-signal can pass\.  |  4,096 bytes  |  To pass a larger amount, send the data to an Amazon S3 bucket, and then use cfn\-signal to pass the Amazon S3 URL to that bucket\.  | 
|  [Custom resource response](aws-resource-cfn-customresource.md)  |  Maximum amount of data that a custom resource provider can pass\.  |  4,096 bytes  |   | 
|  [Mappings](template-anatomy.md)  |  Maximum number of mappings that you can declare in your AWS CloudFormation template\.  |  100 mappings  |  To specify more mappings, separate your template into multiple templates by using, for example, [nested stacks](aws-properties-stack.md)\.  | 
|  [Mapping attributes](template-anatomy.md)  | Maximum number of mapping attributes for each mapping that you can declare in your AWS CloudFormation template\. |  64 attributes  |  To specify more mapping attributes, separate the attributes into multiple mappings\.  | 
|  [Mapping name and mapping attribute name](template-anatomy.md)  |  Maximum size of each mapping name\.  |  255 characters  |   | 
|  [Outputs](template-anatomy.md)  |  Maximum number of outputs that you can declare in your AWS CloudFormation template\.  |  60 outputs  |   | 
|  [Output name](template-anatomy.md)  |  Maximum size of an output name\.  |  255 characters  |   | 
|  [Parameters](template-anatomy.md)  |  Maximum number of parameters that you can declare in your AWS CloudFormation template\.  |  60 parameters  |  To specify more parameters, you can use mappings or lists in order to assign multiple values to a single parameter\.  | 
|  [Parameter name](template-anatomy.md)  |  Maximum size of a parameter name\.  |  255 characters  |   | 
|  [Parameter value](template-anatomy.md)  |  Maximum size of a parameter value\.  |  4,096 bytes  |  To use a larger parameter value, create multiple parameters and then use `Fn::Join` to append the multiple values into a single value\.  | 
|  [Resources](template-anatomy.md)  |  Maximum number of resources that you can declare in your AWS CloudFormation template\.  |  200 resources  |  To specify more resources, separate your template into multiple templates by using, for example, [nested stacks](aws-properties-stack.md)\.  | 
|  [Resource name](template-anatomy.md)  |  Maximum size of a resource name\.  |  255 characters  |   | 
|  [Stacks](stacks.md)  |  Maximum number of AWS CloudFormation stacks that you can create\.  |  200 stacks  |  To create more stacks, delete stacks that you don't need or request an increase in the maximum number of stacks in your AWS account\. For more information, see [AWS Service Limits](http://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html) in the *AWS General Reference*\.  | 
|  [StackSets](what-is-cfnstacksets.md)  |  Maximum number of AWS CloudFormation stack sets you can create in your administrator account\.  |  20 stack sets  |   | 
|  [StackSets](what-is-cfnstacksets.md)  |  Maximum number of stack instances you can create per stack set\.  |  500 stack instances per stack set  |   | 
|  [Template body size in a request](template-anatomy.md)  |  Maximum size of a template body that you can pass in a `CreateStack`, `UpdateStack`, or `ValidateTemplate` request\.  |  51,200 bytes  |  To use a larger template body, separate your template into multiple templates by using, for example, [nested stacks](aws-properties-stack.md)\. Or upload the template to an Amazon S3 bucket\.  | 
|  [Template body size in an Amazon S3 object](template-anatomy.md)  |  Maximum size of a template body that you can pass in an Amazon S3 object for a `CreateStack`, `UpdateStack`, `ValidateTemplate` request with an Amazon S3 template URL\.  |  460,800 bytes  |  To use a larger template body, separate your template into multiple templates by using, for example, [nested stacks](aws-properties-stack.md)\.  | 
|  [Template description](template-anatomy.md)  |  Maximum size of a template description\.  |  1,024 bytes  |   | 