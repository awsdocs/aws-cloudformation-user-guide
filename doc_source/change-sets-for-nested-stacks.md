# Change sets for nested stacks<a name="change-sets-for-nested-stacks"></a>

With *change sets for nested stacks* you can preview the changes to your application and infrastructure resources across the entire nested stack hierarchy and proceed with updates when you’ve confirmed that all the changes are as intended\. 

See the following sections for more details about change sets for nested stacks:
+  [Overview of change sets and nested stacks](#overview-of-change-sets-and-nested-stacks) 
+  [Working with change sets for nested stacks \(console\)](#change-sets-for-nested-stacks-console) 
+  [Working with change sets for nested stacks \(AWS CLI\)](#change-sets-for-nested-stacks-cli) 

## Overview of change sets and nested stacks<a name="overview-of-change-sets-and-nested-stacks"></a>

Change sets for nested stacks combines the following features together to expand the scope of previewing changes to the entire stack hierarchy: 
+ <a name="what_are_change_sets"></a>*Change sets* is an AWS CloudFormation capability that offers a preview of how proposed changes to a stack will impact existing or newly created resources\. Upon creating a change set, AWS CloudFormation provides a list of proposed changes by comparing your stack with the changes to the resources you submitted\. For more information about change sets, see [Updating stacks using change sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets.html)\.
+ <a name="what_are_nested"></a>*Nested stacks* are stacks created as part of other stacks\. To create a nested stack, specify the [AWS::CloudFormation::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html) resource in the `Resource` section of your template\. For example, you might have networking and security related resources in one nested stack and application resources in another\. Partitioning application models this way helps with code maintainability and reuse\. For more information about nested stacks, see [Working with nested stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-nested-stacks.html)\.

## Working with change sets for nested stacks \(console\)<a name="change-sets-for-nested-stacks-console"></a>
+ **Create a change set** – Creates a change set by submitting changes from any level of the stack hierarchy\. You can submit a modified stack template or modified input parameter values and AWS CloudFormation compares your nested stack with the changes that you submitted to generate a change set\. Change sets for nested stacks is enabled by default in the AWS CloudFormation console\. For more information, see [Creating a change set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-create.html)\.  
![\[Create a change set for nested stacks is Enabled by default.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/change-sets-for-nested-sets-enabled-default.png)
**Note**  
A root change set is the change set associated with the stack from which the whole hierarchy of change sets are created\. You must execute or delete change sets for nested stacks from the root change set\. 
+ **View the change set** – Visualize changes to resources inside nested stacks before executing them\. You can view the proposed changes in the **Changes** section of your change set by navigating through the current stack and its nested change sets\. For more information, see [Viewing a change set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-view.html)\.
+ **Execute the change set** – Execute the changes described in the change set that pertain to the current stack and its descendants\. The execute action must be made from the root change set\. For more information, see [Executing a change set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-execute.html)\.
+ **Delete the change set** – Removes the change sets from the current stack\. Deleting a change set helps to prevent you or another user from accidentally initiating a change set that should not be applied\. The delete action must be executed from the root change set\. For more information, see [Deleting a change set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets-delete.html)\.

## Working with change sets for nested stacks \(AWS CLI\)<a name="change-sets-for-nested-stacks-cli"></a>

### create\-change\-set<a name="working-with-change-sets-for-nested-stacks-cli"></a>
+ [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-change-set.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/create-change-set.html) – Change sets for nested stacks is not enabled by default for the AWS CLI\. To create a change set for the entire stack hierarchy, specify the `--include-nested-stacks` parameter\. For more information, see [To create a change set \(AWS CLI\)](using-cfn-updating-stacks-changesets-create.md)\.

The following AWS CLI example is of a `create-change-set` input\.

```
aws cloudformation create-change-set \
    --stack-name my-root-stack \
    --change-set-name my-root-stack-change-set \
    --template-body file://template.yaml \
    --capabilities CAPABILITY_IAM \
    --include-nested-stacks 
```

The following AWS CLI example is of a `create-change-set` output\.

```
{
    "Id":"arn:aws:cloudformation:us-west-2:123456789012:changeSet/my-root-stack-change-set/4eca1a01-e285-xmpl-8026-9a1967bfb4b0",
    "StackId": "arn:aws:cloudformation:us-west-2:123456789012:Stack/my-root-stack/d0a825a0-e4cd-xmpl-b9fb-061c69e99204"
}
```

### describe\-change\-set<a name="working-with-change-set-describe-cli"></a>
+ [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-change-set.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-change-set.html) – Returns a list of changes that AWS CloudFormation will make if you execute the change set\. If the change set specified contains child change sets that belong to nested stacks, then `ChangeSetId` will return information about that change set\. For more information, see [To view a change set \(AWS CLI\)](using-cfn-updating-stacks-changesets-view.md)\.

The following AWS CLI example is of a `describe-change-set` input for the root stack change set\.

```
aws cloudformation describe-change-set \
    --change-set-name my-root-stack-change-set \
    --stack-name my-root-stack
```

The following AWS CLI example is of a `describe-change-set` output for the root stack change set\.

```
{
    "Changes": [
        {
            "Type": "Resource",
            "ResourceChange": {
                "Action": "Modify",
                "LogicalResourceId": "ChildStack",
                "PhysicalResourceId": "arn:aws:cloudformation:us-west-2:123456789012:stack/my-nested-stack/d0a825a0-e4cd-xmpl-b9fb-061c69e99205",
                "ResourceType": "AWS::CloudFormation::Stack",
                "Replacement": "False",
                "ChangeSetId": "arn:aws:cloudformation:us-west-2:123456789012:changeSet/my-nested-stack-change-set/4eca1a01-e285-xmpl-8026-9a1967bfb4b0",
                "Scope": [
                    "Properties"
                ],
                "Details": [
                    {
                        "Target": {
                            "Attribute": "Properties",
                            "RequiresRecreation": "Never"
                        },
                        "Evaluation": "Dynamic",
                        "ChangeSource": "Automatic"
                    }
                ]
            }
        }
    ],
    "ChangeSetName": "my-root-stack-change-set",
    "ChangeSetId": "arn:aws:cloudformation:us-west-2:123456789012:changeSet/my-root-stack-change-set/4eca1a01-e285-xmpl-8026-9a1967bfb4b0",
    "StackId": "arn:aws:cloudformation:us-west-2:123456789012:stack/my-root-stack/d0a825a0-e4cd-xmpl-b9fb-061c69e99204",
    "StackName": "my-root-stack",
    "IncludeNestedStacks": true,
    "ParentChangeSetId": null,
    "RootChangeSetId": null,
    "Description": null,
    "Parameters": null,
    "CreationTime": "2020-11-18T05:20:56.651Z",
    "ExecutionStatus": "AVAILABLE",
    "Status": "CREATE_COMPLETE",
    "StatusReason": null,
    "NotificationARNs": [
        
    ],
    "RollbackConfiguration": {
        
    },
    "Capabilities": [
        "CAPABILITY_IAM"
    ],
    "Tags": null
}
```

The following AWS CLI example is of a `describe-change-set` input for the nested stack change set\.

```
aws cloudformation describe-change-set \
    --change-set-name my-nested-stack-change-set \
    --stack-name my-nested-stack
```

The following AWS CLI example is of a `describe-change-set` output for the nested stack change set\.

```
{
    "Changes": [
        {
            "Type": "Resource",
            "ResourceChange": {
                "Action": "Modify",
                "LogicalResourceId": "function",
                "PhysicalResourceId": "my-function",
                "ResourceType": "AWS::Lambda::Function",
                "Replacement": "False",
                "ChangeSetId": null,
                "Scope": [
                    "Properties"
                ],
                "Details": [
                    {
                        "Target": {
                            "Attribute": "Properties",
                            "Name": "Timeout",
                            "RequiresRecreation": "Never"
                        },
                        "Evaluation": "Static",
                        "ChangeSource": "DirectModification"
                    }
                ]
            }
        }
    ],
    "ChangeSetName": "my-nested-stack-change-set",
    "ChangeSetId": "arn:aws:cloudformation:us-west-2:123456789012:changeSet/my-nested-stack-change-set/4eca1a01-e285-xmpl-8026-9a1967bfb4b0",
    "StackId": "arn:aws:cloudformation:us-west-2:123456789012:stack/my-nested-stack/d0a825a0-e4cd-xmpl-b9fb-061c69e99205",
    "ParentChangeSetId": "arn:aws:cloudformation:us-west-2:123456789012:changeSet/my-root-stack-change-set/4eca1a01-e285-xmpl-8026-9a1967bfb4b0",
    "RootChangeSetId": "arn:aws:cloudformation:us-west-2:123456789012:changeSet/my-root-stack-change-set/4eca1a01-e285-xmpl-8026-9a1967bfb4b0",
    "IncludeNestedStacks": true,
    "StackName": "my-nested-stack",
    "Description": null,
    "Parameters": null,
    "CreationTime": "2020-11-18T05:20:56.651Z",
    "ExecutionStatus": "UNAVAILABLE",
    "Status": "CREATE_COMPLETE",
    "StatusReason": "Executable from root change set",
    "NotificationARNs": [
        
    ],
    "RollbackConfiguration": {
        
    },
    "Capabilities": [
        "CAPABILITY_IAM"
    ],
    "Tags": null
}
```

### execute\-change\-set<a name="working-with-change-set-execute-cli"></a>
+ [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/execute-change-set.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/execute-change-set.html) – Creates or updates a stack using the input information that was provided when the specified change set was created\. To create a change set for the entire stack hierarchy, you must specify the `–include-nested-stacks` parameter during the `create-change-set` process\. For more information, see [To execute a change set \(AWS CLI\)](using-cfn-updating-stacks-changesets-execute.md)\.
**Note**  
`execute-change-set` must be executed from the root change set and will apply the change set on the whole hierarchy of stacks\.

The following AWS CLI example is of an `execute-change-set` input\.

```
aws cloudformation execute-change-set 
    --stack-name my-root-stack \ 
    --change-set-name my-root-stack-change-set
```

### delete\-change\-set<a name="working-with-change-set-delete-cli"></a>
+ [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/delete-change-set.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/delete-change-set.html) – Deletes the specified change set\. Deleting change sets ensures that no one uses the wrong change set\. Deleting change sets is asynchronous for change sets created with the `–include-nested-stacks` parameter\. For more information, see [To delete a change set \(AWS CLI\)](using-cfn-updating-stacks-changesets-delete.md) \.
**Note**  
`delete-change-set` must be executed from the root change set and will delete the whole hierarchy of change sets\. Nested stacks in the `REVIEW_IN_PROGRESS` status will also be deleted if they were created during the `create-change-set` action\.

The following AWS CLI example is of a `delete-change-set` input on the root change set\.

```
aws cloudformation delete-change-set 
    --stack-name my-root-stack \ 
    --change-set-name my-root-stack-change-set
```