# Listing Stacks That Import an Exported Output Value<a name="using-cfn-stack-imports"></a>

When you export an output value, stacks that are in the same AWS account and region can import that value\. To see which stacks are importing a particular output value, use the list import action\.

To delete or modify exported output values, use the `ListImports` action to track which stacks are importing them, and then modify those stacks to remove the [`Fn::ImportValue`](intrinsic-function-reference-importvalue.md) functions that reference the output values\. You must remove all of the imports that reference exported output values before you can delete or modify the exported output values\.

For more information about exporting and importing output values, see [Exporting Stack Output Values](using-cfn-stack-exports.md)\.

**To list stacks that import an exported output value \(console\)**

1. In the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), from the **CloudFormation** drop\-down menu, choose **Exports**\.  
![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-cfn-exports.png)

1. From the list of exported output values, choose the value\. The `Imports` section of the detail page lists all of the stacks that are importing the value\.

**To list stacks that import an exported output value \(CLI\)**
+ Run the [aws cloudformation list\-imports](http://docs.aws.amazon.com/cli/latest/reference/cloudformation/list-imports.html) command, providing the name of the exported output value\.

  AWS CloudFormation returns a list of stacks that are importing the value\.

**To list stacks that import an exported output value \(API\)**
+ Run the [http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ListImports.html](http://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ListImports.html) API, providing the name of the exported output value\.

  AWS CloudFormation returns a list of stacks that are importing the value\.