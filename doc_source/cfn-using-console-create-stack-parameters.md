# Specifying stack name and parameters<a name="cfn-using-console-create-stack-parameters"></a>

After selecting a stack template, specify the stack name and values for the parameters that were defined in the template\.

With parameters, you can customize your stack at creation time\. Your parameter values can be used in the stack template to modify how resources are configured\. That way you don't have to hard code values in multiple templates to specify different settings\. For more information about parameters in an AWS CloudFormation template, see [Parameters](parameters-section-structure.md)\.

**To specify the stack name and parameter values**

1. On the **Specify stack details** page, type a stack name in the **Stack name** box\.

   The stack name is an identifier that helps you find a particular stack from a list of stacks\. A stack name can contain only alphanumeric characters \(case\-sensitive\) and hyphens\. It must start with an alphabetic character and can't be longer than 128 characters\.

1. In the **Parameters** section, specify parameters that are defined in the stack template\.

   You can use or change any parameters with default values\.

1. When you are satisfied with the parameter values, click **Next** to proceed with [setting options for your stack](cfn-console-add-tags.md)\.

## AWS\-specific parameter types<a name="cfn-using-console-create-stack-parameters-awstypes"></a>

When you create stacks that contain AWS\-specific parameter types, the AWS CloudFormation console provides drop\-down lists of valid values for those parameters\. Depending on the parameter type, you can search for values by ID, name, or the value of the `Name` tag\. For example, with the `AWS::EC2::VPC::Id` parameter type, you can search for a specific VPC ID, such as `vpc-b47658d1`\. If the VPC was tagged with a name, such as `Name:TestVPC`, you can also search for `TestVPC`\. Currently, you can search only for tag values with the `Name` key\.

![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stack-parameters-name-example.png)

**Note**  
The console doesn't provide a drop\-down list or enable you to search for values with the `AWS::EC2::Image::Id` parameter type; AWS CloudFormation only verifies if the input values are valid Amazon Elastic Compute Cloud image IDs\.

## Group and sort parameters<a name="cfn-using-console-create-stack-parameters-sort"></a>

The console alphabetically lists input parameters by their logical ID\. When you create a template, you can use the `AWS::CloudFormation::Interface` metadata key to override the default ordering\. For more information and an example of the `AWS::CloudFormation::Interface` metadata key, see [AWS::CloudFormation::Interface](aws-resource-cloudformation-interface.md)\.