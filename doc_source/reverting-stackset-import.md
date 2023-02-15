# Reverting a stack import operation<a name="reverting-stackset-import"></a>

To revert a stack import operation, complete the following tasks:

1. Specify a `DeletionPolicy` attribute of `Retain` for each resource that you want to keep after the stack instance is deleted\. For more information, see [Reverting an import operation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-revert.html)\.

1. Delete stack instances from your stack set\. For more information, see [Delete stack instances from your stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stackinstances-delete.html)\.

1. Delete your stack set\. For more information, see [Delete a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-delete.html)\.

**Results**: The revert operation has deleted the stack instance and retained the stack's resources\.