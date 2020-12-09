# Modifying a stack template<a name="using-cfn-updating-stacks-get-template"></a>

If you want to modify resources and properties that are declared in a stack template, you must modify the stack's template\. To ensure that you update only the resources that you intend to update, use the template for the existing stack as a starting point and make your updates to that template\. If you are managing your template in a source control system, use a copy of that template as a starting point\. Otherwise, you can get a copy of a stack template from AWS CloudFormation\.

If you want to modify just the parameters or settings of a stack \(like a stack's Amazon SNS topic\), you can reuse the existing stack template\. You don't need to get a copy of the stack template or make modifications to the stack template\.

**Note**  
If your template includes an unsupported change, AWS CloudFormation returns a message saying that the change is not permitted\. This message might occur asynchronously, however, because resources are created and updated by AWS CloudFormation in a non\-deterministic order by default\.

**Topics**
+ [Update a stack's template \(console\)](#using-cfn-updating-stacks-get-stack.CON)
+ [Get and update a template for a stack \(CLI\)](#using-cfn-updating-stacks-get-stack.CLI)

## Update a stack's template \(console\)<a name="using-cfn-updating-stacks-get-stack.CON"></a>

1. On the **Stacks** page of the [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation), click the name of the stack that you want to update\. 

1. In the stack details pane for the selected stack, select the **Template** pane, and then click **View in Designer**\.

   AWS CloudFormation opens a copy of the stack's template in AWS CloudFormation Designer\.

1. Modify the template\.

   You can use the AWS CloudFormation Designer drag\-and\-drop interface or the integrated JSON and YAML editor to modify the template\. For more information about using AWS CloudFormation Designer, see [What is AWS CloudFormation Designer?](working-with-templates-cfn-designer.md)\.

   Modify only the resources that you want to update\. Use the *same values* as the current stack configuration for resources and properties that you aren't updating\. You can modify the template by completing any of the following actions:
   + Add new resources, or remove existing resources\.

     For most resources, changing the logical name of a resource is equivalent to deleting that resource and replacing it with a new one\. Any other resources that depend on the renamed resource also need to be updated and might cause them to be replaced\. Other resources require you to update a property \(not just the logical name\) in order to trigger an update\.
   + Add, modify, or delete properties of existing resources\.

     Consult the [AWS Resource Types Reference](aws-template-resource-type-ref.md) for information about the effects of updating particular resource properties\. For each property, the effects of an update will be one of the following:
     + *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)
     + *Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)
     + *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)
   + Add, modify, or delete attributes for resources \(`Metadata`, `DependsOn`, `CreationPolicy`, `UpdatePolicy`, and `DeletionPolicy`\)\.
**Important**  
You cannot update the `CreationPolicy`, `DeletionPolicy`\. or `UpdatePolicy` attribute by itself\. You can update them only when you include changes that add, modify, or delete resources\. For example, you can add or modify a metadata attribute of a resource\.
   + Add, modify, or delete parameter declarations\. However, you cannot add, modify, or delete a parameter that is used by a resource that does not support updates\.
   + Add, modify, or delete mapping declarations\.
**Important**  
If the values in a mapping are not being used by your stack, you can't update the mapping by itself\. You need to include changes that add, modify, or delete resources\. For example, you can add or modify a metadata attribute of a resource\. If you update a mapping value that your stack is using, you don't need to make any other changes to trigger an update\.
   + Add, modify, or delete condition declarations\.
**Important**  
You cannot update conditions by themselves\. You can update conditions only when you include changes that add, modify, or delete resources\. For example, you can add or modify a metadata attribute of a resource\.
   + Add, modify, or delete output value declarations\.

   Some resources or properties may have constraints on property values or changes to those values\. For example, changes to the `AllocatedStorage` property of an [ AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) resource must be greater than the current setting\. If the value specified for the update does not meet those constraints, the update for that resource fails\. For the specific constraints on `AllocatedStorage` changes, see [ ModifyDBInstance](http://docs.aws.amazon.com/AmazonRDS/latest/APIReference/API_ModifyDBInstance.html)\.

   Updates to a resource can affect the properties of other resources\. If you used the [ Ref function ](intrinsic-function-reference-ref.md) or the [ Fn::GetAtt function](intrinsic-function-reference-getatt.md) to specify an attribute from an updated resource as part of a property value in another resource in the template, AWS CloudFormation also updates the resource that contains the reference to the property that has changed\. For example, if you updated the `MasterUsername` property of an `AWS::RDS::DBInstance` resource and you had an `AWS::AutoScaling::LaunchConfiguration` resource that had a `UserData` property that contained a reference to the DB instance name using the `Ref` function, AWS CloudFormation would recreate the DB instance with a new name and also update the `LaunchConfiguration` resource\.

1. To check for syntax errors in your template, from the AWS CloudFormation Designer toolbar, choose **Validate template** \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-validate-icon.png)\)\.

   View and fix any errors in the **Messages** pane, and then validate the template again\. If you don't see any errors, your template is syntactically valid\.

1. From the AWS CloudFormation Designer toolbar, choose the **File** menu \(![\[Image NOT FOUND\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/designer-file-menu.png)\) and then **Save** to save the template in an S3 bucket or locally\.

## Get and update a template for a stack \(CLI\)<a name="using-cfn-updating-stacks-get-stack.CLI"></a>

1. To get the template for the stack you want to update, use the command [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/get-template.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/get-template.html)\.

1. Copy the template, paste it into a text file, modify it, and save it\. Copy *only* the template\. The command encloses the template in quotation marks, but do not copy the quotation marks surrounding the template\. The template itself starts with an open brace and ends with the final close brace\. Specify changes to the stack's resources in this file\.