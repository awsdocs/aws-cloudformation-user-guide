# Example change sets<a name="using-cfn-updating-stacks-changesets-samples"></a>

This section provides examples of the change sets that AWS CloudFormation would create for common stack changes\. They show how to edit a template directly; modify a single input parameter; plan for resource recreation \(replacements\), which prevents you from losing data that wasn't backed up or interrupting applications that are running in your stack; and add and remove resources\. To illustrate how change sets work, we'll walk through the changes that were submitted and discuss the resulting change set\. Because each example builds on and assumes that you understand the previous example, we recommend that you read them in order\. For a description of each field in a change set, see the [Change](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_Change.html) data type in the *AWS CloudFormation API Reference*\.

You can use the [console](using-cfn-updating-stacks-changesets-view.md), AWS CLI, or AWS CloudFormation [API](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeChangeSet.html) to view change set details\.

We generated each of the following change sets from a stack with the following [sample template](https://s3.amazonaws.com/cloudformation-examples/user-guide/changesets/ec2-instance.txt):

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Description" : "A sample EC2 instance template for testing change sets.",
  "Parameters" : {
    "Purpose" : {
      "Type" : "String",
      "Default" : "testing",
      "AllowedValues" : ["testing", "production"],
      "Description" : "The purpose of this instance."
    },
    "KeyPairName" : {
      "Type": "AWS::EC2::KeyPair::KeyName",
      "Description" : "Name of an existing EC2 KeyPair to enable SSH access to the instance"
    },
    "InstanceType" : {
      "Type" : "String",
      "Default" : "t2.micro",
      "AllowedValues" : ["t2.micro", "t2.small", "t2.medium"],
      "Description" : "The EC2 instance type."
    }
  },
  "Resources" : {
    "MyEC2Instance" : {
      "Type" : "AWS::EC2::Instance",
      "Properties" : {
        "KeyName" : { "Ref" : "KeyPairName" },
        "InstanceType" : { "Ref" : "InstanceType" },
        "ImageId" : "ami-8fcee4e5",
        "Tags" : [
          {
            "Key" : "Purpose",
            "Value" : { "Ref" : "Purpose" }
          }
        ]
      }
    }
  }
}
```

## Directly editing a template<a name="using-cfn-updating-stacks-changesets-samples-directly-editing-a-template"></a>

When you directly modify resources in the stack's template to generate a change set, AWS CloudFormation classifies the change as a direct modification, as opposed to changes triggered by an updated parameter value\. The following change set, which added a new tag to the `i-1abc23d4` instance, is an example of a direct modification\. All other input values, such as the parameter values and capabilities, are unchanged, so we'll focus on the `Changes` structure\.

```
{
    "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
    "Status": "CREATE_COMPLETE",
    "ChangeSetName": "SampleChangeSet-direct",
    "Parameters": [
        {
            "ParameterValue": "testing",
            "ParameterKey": "Purpose"
        },
        {
            "ParameterValue": "MyKeyName",
            "ParameterKey": "KeyPairName"
        },
        {
            "ParameterValue": "t2.micro",
            "ParameterKey": "InstanceType"
        }
    ],
    "Changes": [
        {
            "ResourceChange": {
                "ResourceType": "AWS::EC2::Instance",
                "PhysicalResourceId": "i-1abc23d4",
                "Details": [
                    {
                        "ChangeSource": "DirectModification",
                        "Evaluation": "Static",
                        "Target": {
                            "Attribute": "Tags",
                            "RequiresRecreation": "Never"
                        }
                    }
                ],
                "Action": "Modify",
                "Scope": [
                    "Tags"
                ],
                "LogicalResourceId": "MyEC2Instance",
                "Replacement": "False"
            },
            "Type": "Resource"
        }
    ],
    "CreationTime": "2020-11-18T23:35:25.813Z",
    "Capabilities": [],
    "StackName": "SampleStack",
    "NotificationARNs": [],
    "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet-direct/1a2345b6-0000-00a0-a123-00abc0abc000"
}
```

In the `Changes` structure, there's only one `ResourceChange` structure\. This structure describes information such as the type of resource AWS CloudFormation will change, the action AWS CloudFormation will take, the ID of the resource, the scope of the change, and whether the change requires a replacement \(where AWS CloudFormation creates a new resource and then deletes the old one\)\. In the example, the change set indicates that AWS CloudFormation will modify the `Tags` attribute of the `i-1abc23d4` EC2 instance, and doesn't require the instance to be replaced\.

In the `Details` structure, AWS CloudFormation labels this change as a direct modification that will never require the instance to be recreated \(replaced\)\. You can confidently execute this change, knowing that AWS CloudFormation won't replace the instance\.

AWS CloudFormation shows this change as a `Static` evaluation\. A static evaluation means that AWS CloudFormation can determine the tag's value before executing the change set\. In some cases, AWS CloudFormation can determine a value only after you execute a change set\. AWS CloudFormation labels those changes as `Dynamic` evaluations\. For example, if you reference an updated resource that is conditionally replaced, AWS CloudFormation can't determine whether the reference to the updated resource will change\.

## Modifying an input parameter value<a name="using-cfn-updating-stacks-changesets-samples-modifying-a-single-input-parameter-value"></a>

When you modify an input parameter value, AWS CloudFormation generates two changes for each resource that uses the updated parameter value\. In this example, we want to highlight what those changes look like and which information you should focus on\. The following example was generated by changing the value of the `Purpose` input parameter only\. 

The `Purpose` parameter specifies a tag key value for the EC2 instance\. In the example, the parameter value was changed from `testing` to `production`\. The new value is shown in the `Parameters` structure\.

```
{
    "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
    "Status": "CREATE_COMPLETE",
    "ChangeSetName": "SampleChangeSet",
    "Parameters": [
        {
            "ParameterValue": "production",
            "ParameterKey": "Purpose"
        },
        {
            "ParameterValue": "MyKeyName",
            "ParameterKey": "KeyPairName"
        },
        {
            "ParameterValue": "t2.micro",
            "ParameterKey": "InstanceType"
        }
    ],
    "Changes": [
        {
            "ResourceChange": {
                "ResourceType": "AWS::EC2::Instance",
                "PhysicalResourceId": "i-1abc23d4",
                "Details": [
                    {
                        "ChangeSource": "DirectModification",
                        "Evaluation": "Dynamic",
                        "Target": {
                            "Attribute": "Tags",
                            "RequiresRecreation": "Never"
                        }
                    },
                    {
                        "CausingEntity": "Purpose",
                        "ChangeSource": "ParameterReference",
                        "Evaluation": "Static",
                        "Target": {
                            "Attribute": "Tags",
                            "RequiresRecreation": "Never"
                        }
                    }
                ],
                "Action": "Modify",
                "Scope": [
                    "Tags"
                ],
                "LogicalResourceId": "MyEC2Instance",
                "Replacement": "False"
            },
            "Type": "Resource"
        }
    ],
    "CreationTime": "2020-11-18T23:59:18.447Z",
    "Capabilities": [],
    "StackName": "SampleStack",
    "NotificationARNs": [],
    "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet/1a2345b6-0000-00a0-a123-00abc0abc000"
}
```

The `Changes` structure functions similar to way it does in the [Directly Editing a Template](#using-cfn-updating-stacks-changesets-samples-directly-editing-a-template) example\. There's only one `ResourceChange` structure; it describes a change to the `Tags` attribute of the `i-1abc23d4` EC2 instance\.

However, in the `Details` structure, the change set shows two changes for the `Tags` attribute, even though only a single parameter value was changed\. Resources that reference a changed parameter value \(using the `Ref` intrinsic function\) always result in two changes: one with a `Dynamic` evaluation and another with a `Static` evaluation\. You can see these types of changes by viewing the following fields:
+ For the `Static` evaluation change, view the `ChangeSource` field\. In this example, the `ChangeSource` field equals `ParameterReference`, meaning that this change is a result of an updated parameter reference value\. The change set must contain a similar `Dynamic` evaluation change\.
+ You can find the matching `Dynamic` evaluation change by comparing the `Target` structure for both changes, which will contain the same information\. In this example, the `Target` structures for both changes contain the same values for the `Attribute` and `RequireRecreation` fields\.

For these types of changes, focus on the static evaluation, which gives you the most detailed information about the change\. In this example, the static evaluation shows that the change is the result of a change in a parameter reference value \(`ParameterReference`\)\. The exact parameter that was changed is indicated by the `CauseEntity` field \(the `Purpose` parameter\)\.

## Determining the value of the replacement field<a name="using-cfn-updating-stacks-changesets-samples-determining-the-value-of-the-replacement-field"></a>

The `Replacement` field in a `ResourceChange` structure indicates whether AWS CloudFormation will recreate the resource\. Planning for resource recreation \(replacements\) prevents you from losing data that wasn't backed up or interrupting applications that are running in your stack\.

The value in the `Replacement` field depends on whether a change requires a replacement, indicated by the `RequiresRecreation` field in a change's `Target` structure\. For example, if the `RequiresRecreation` field is `Never`, the `Replacement` field is `False`\. However, if there are multiple changes on a single resource and each change has a different value for the `RequiresRecreation` field, AWS CloudFormation updates the resource using the most intrusive behavior\. In other words, if only one of the many changes requires a replacement, AWS CloudFormation must replace the resource and, therefore, sets the `Replacement` field to `True`\.

The following change set was generated by changing the values for every parameter \(`Purpose`, `InstanceType`, and `KeyPairName`\), which are all used by the EC2 instance\. With these changes, AWS CloudFormation will be required to replace the instance because the `Replacement` field is equal to `True`\.

```
{
    "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
    "Status": "CREATE_COMPLETE",
    "ChangeSetName": "SampleChangeSet-multiple",
    "Parameters": [
        {
            "ParameterValue": "production",
            "ParameterKey": "Purpose"
        },
        {
            "ParameterValue": "MyNewKeyName",
            "ParameterKey": "KeyPairName"
        },
        {
            "ParameterValue": "t2.small",
            "ParameterKey": "InstanceType"
        }
    ],
    "Changes": [
        {
            "ResourceChange": {
                "ResourceType": "AWS::EC2::Instance",
                "PhysicalResourceId": "i-7bef86f8",
                "Details": [
                    {
                        "ChangeSource": "DirectModification",
                        "Evaluation": "Dynamic",
                        "Target": {
                            "Attribute": "Properties",
                            "Name": "KeyName",
                            "RequiresRecreation": "Always"
                        }
                    },
                    {
                        "ChangeSource": "DirectModification",
                        "Evaluation": "Dynamic",
                        "Target": {
                            "Attribute": "Properties",
                            "Name": "InstanceType",
                            "RequiresRecreation": "Conditionally"
                        }
                    },
                    {
                        "ChangeSource": "DirectModification",
                        "Evaluation": "Dynamic",
                        "Target": {
                            "Attribute": "Tags",
                            "RequiresRecreation": "Never"
                        }
                    },
                    {
                        "CausingEntity": "KeyPairName",
                        "ChangeSource": "ParameterReference",
                        "Evaluation": "Static",
                        "Target": {
                            "Attribute": "Properties",
                            "Name": "KeyName",
                            "RequiresRecreation": "Always"
                        }
                    },
                    {
                        "CausingEntity": "InstanceType",
                        "ChangeSource": "ParameterReference",
                        "Evaluation": "Static",
                        "Target": {
                            "Attribute": "Properties",
                            "Name": "InstanceType",
                            "RequiresRecreation": "Conditionally"
                        }
                    },
                    {
                        "CausingEntity": "Purpose",
                        "ChangeSource": "ParameterReference",
                        "Evaluation": "Static",
                        "Target": {
                            "Attribute": "Tags",
                            "RequiresRecreation": "Never"
                        }
                    }
                ],
                "Action": "Modify",
                "Scope": [
                    "Tags",
                    "Properties"
                ],
                "LogicalResourceId": "MyEC2Instance",
                "Replacement": "True"
            },
            "Type": "Resource"
        }
    ],
    "CreationTime": "2020-11-18T00:39:35.974Z",
    "Capabilities": [],
    "StackName": "SampleStack",
    "NotificationARNs": [],
    "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet-multiple/1a2345b6-0000-00a0-a123-00abc0abc000"
}
```

Identify the change that requires the resource to be replaced by viewing each change \(the static evaluations in the `Details` structure\)\. In this example, each change has a different value for the `RequireRecreation` field, but the change to the `KeyName` property has the most intrusive update behavior, always requiring a recreation\. AWS CloudFormation will replace the instance because the key name was changed\.

If the key name were unchanged, the change to the `InstanceType` property would have the most intrusive update behavior \(`Conditionally`\), so the `Replacement` field would be `Conditionally`\. To find the conditions in which AWS CloudFormation replaces the instance, view the update behavior for the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html#cfn-ec2-instance-instancetype](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html#cfn-ec2-instance-instancetype) property\.

## Adding and removing resources<a name="using-cfn-updating-stacks-changesets-samples-adding-and-removing-resources"></a>

The following example was generated by submitting a modified template that removes the EC2 instance and adds an Auto Scaling group and launch configuration\.

```
{
    "StackId": "arn:aws:cloudformation:us-east-1:123456789012:stack/SampleStack/1a2345b6-0000-00a0-a123-00abc0abc000",
    "Status": "CREATE_COMPLETE",
    "ChangeSetName": "SampleChangeSet-addremove",
    "Parameters": [
        {
            "ParameterValue": "testing",
            "ParameterKey": "Purpose"
        },
        {
            "ParameterValue": "MyKeyName",
            "ParameterKey": "KeyPairName"
        },
        {
            "ParameterValue": "t2.micro",
            "ParameterKey": "InstanceType"
        }
    ],
    "Changes": [
        {
            "ResourceChange": {
                "Action": "Add",
                "ResourceType": "AWS::AutoScaling::AutoScalingGroup",
                "Scope": [],
                "Details": [],
                "LogicalResourceId": "AutoScalingGroup"
            },
            "Type": "Resource"
        },
        {
            "ResourceChange": {
                "Action": "Add",
                "ResourceType": "AWS::AutoScaling::LaunchConfiguration",
                "Scope": [],
                "Details": [],
                "LogicalResourceId": "LaunchConfig"
            },
            "Type": "Resource"
        },
        {
            "ResourceChange": {
                "ResourceType": "AWS::EC2::Instance",
                "PhysicalResourceId": "i-1abc23d4",
                "Details": [],
                "Action": "Remove",
                "Scope": [],
                "LogicalResourceId": "MyEC2Instance"
            },
            "Type": "Resource"
        }
    ],
    "CreationTime": "2020-11-18T01:44:08.444Z",
    "Capabilities": [],
    "StackName": "SampleStack",
    "NotificationARNs": [],
    "ChangeSetId": "arn:aws:cloudformation:us-east-1:123456789012:changeSet/SampleChangeSet-addremove/1a2345b6-0000-00a0-a123-00abc0abc000"
}
```

In the `Changes` structure, there are three `ResourceChange` structures, one for each resource\. For each resource, the `Action` field indicates whether AWS CloudFormation adds or removes the resource\. The `Scope` and `Details` fields are empty because they apply only to modified resources\.

For new resources, AWS CloudFormation can't determine the value of some fields until you execute the change set\. For example, AWS CloudFormation doesn't provide the physical IDs of the Auto Scaling group and launch configuration because they don't exist yet\. AWS CloudFormation creates the new resources when you execute the change set\.