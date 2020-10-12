# Exporting stack output values<a name="using-cfn-stack-exports"></a>

To share information between stacks, export a stack's output values\. Other stacks that are in the same AWS account and region can import the exported values\. For example, you might have a single networking stack that exports the IDs of a subnet and security group for public web servers\. Stacks with a public web server can easily import those networking resources\. You don't need to hard code resource IDs in the stack's template or pass IDs as input parameters\.

To export a stack's output value, use the `Export` field in the [Output](outputs-section-structure.md) section of the stack's template\. To import those values, use the [`Fn::ImportValue`](intrinsic-function-reference-importvalue.md) function in the template for the other stacks\. For a walkthrough and sample templates, see [Walkthrough: Refer to resource outputs in another AWS CloudFormation stack](walkthrough-crossstackref.md)\.

**Note**  
After another stack imports an output value, you can't delete the stack that is exporting the output value or modify the exported output value\. All of the imports must be removed before you can delete the exporting stack or modify the output value\.

## Exporting stack output values vs\. using nested stacks<a name="output-vs-nested"></a>

A nested stack is a stack that you create within another stack by using the [AWS::CloudFormation::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html) resource\. With nested stacks, you deploy and manage all resources from a single stack\. You can use outputs from one stack in the nested stack group as inputs to another stack in the group\. This differs from exporting values\.

If you want to isolate information sharing to within a nested stack group, we suggest that you use nested stacks\. To share information with other stacks \(not just within the group of nested stacks\), export values\. For example, you can create a single stack with a subnet and then export its ID\. Other stacks can use that subnet by importing its ID; each stack doesn't need to create its own subnet\. Note that as long as stacks are importing the subnet ID, you can't change or delete it\.

## Listing exported output values<a name="using-cfn-stack-exports-listing"></a>

To see the values that you can import, list all of the exported output values by using the AWS CloudFormation console, AWS CLI, or AWS CloudFormation API\. AWS CloudFormation shows the names and values of the exported outputs for the current region and the stack from which the outputs are exported\. To reference an exported output value in a stack's template, use the export name and the [`Fn::ImportValue`](intrinsic-function-reference-importvalue.md) function\.

**To list exported output values \(console\)**
+ In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), from the **CloudFormation** navigation pane, choose **Exports**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-exports.png)

**To list exported output values \(AWS CLI\)**
+ Run the [aws cloudformation list\-exports](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-exports.html) command\.

**To list exported output values \(API\)**
+ Run the [https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ListExports.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ListExports.html) API\.