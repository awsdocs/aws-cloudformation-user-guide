# AWS::CloudFormation::Interface<a name="aws-resource-cloudformation-interface"></a>

`AWS::CloudFormation::Interface` is a metadata key that defines how parameters are grouped and sorted in the AWS CloudFormation console\. When you create or update stacks in the console, the console lists input parameters in alphabetical order by their logical IDs\. By using this key, you can define your own parameter grouping and ordering so that users can efficiently specify parameter values\. For example, you could group all EC2\-related parameters in one group and all VPC\-related parameters in another group\.

In addition to grouping and ordering parameters, you can define labels for parameters\. A label is a friendly name or description that the console displays instead of a parameter's logical ID\. Labels are useful for helping users understand the values to specify for each parameter\. For example, you could label a `KeyPair` parameter `Select an EC2 key pair`\.

**Note**  
Only the AWS CloudFormation console uses the `AWS::CloudFormation::Interface` metadata key\. AWS CloudFormation CLI and API calls do not use this key\.

## Syntax<a name="aws-resource-cloudformation-interface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudformation-interface-syntax.json"></a>

```
"Metadata" : {
  "AWS::CloudFormation::Interface" : {
    "ParameterGroups" : [ ParameterGroup, ... ],
    "ParameterLabels" : ParameterLabel
  }
}
```

### YAML<a name="aws-resource-cloudformation-interface-syntax.yaml"></a>

```
Metadata:
  AWS::CloudFormation::Interface:
    ParameterGroups:
      - ParameterGroup
    ParameterLabels:
      ParameterLabel
```

## Properties<a name="w7739ab1c27c15c15c27c13"></a>

`ParameterGroups`  <a name="cfn-cloudformation-interface-parametergroups"></a>
A list of parameter group types, where you specify group names, the parameters in each group, and the order in which the parameters are shown\.  
*Required*: No  
*Type*: [AWS::CloudFormation::Interface ParameterGroup](aws-properties-cloudformation-interface-parametergroup.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ParameterLabels`  <a name="cfn-cloudformation-interface-parameterlabels"></a>
A mapping of parameters and their friendly names that the AWS CloudFormation console shows when a stack is created or updated\.  
*Required*: No  
*Type*: [AWS::CloudFormation::Interface ParameterLabel](aws-properties-cloudformation-interface-parameterlabel.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Example<a name="w7739ab1c27c15c15c27c15"></a>

The following example defines two parameter groups: `Network Configuration` and `Amazon EC2 Configuration`\. The `Network Configuration` group includes the `VPCID`, `SubnetId`, and `SecurityGroupID` parameters, which are defined in the `Parameters` section of the template \(not shown\)\. The order in which the console shows these parameters is defined by the order in which the parameters are listed, starting with the `VPCID` parameter\. The example similarly groups and orders the `Amazon EC2 Configuration` parameters\.

The example also defines a label for the `VPCID` parameter\. The console will show **Which VPC should this be deployed to?** instead of the parameter's logical ID \(`VPCID`\)\.

### JSON<a name="aws-resource-cloudformation-interface-example.json"></a>

```
"Metadata" : {
  "AWS::CloudFormation::Interface" : {
    "ParameterGroups" : [
      {
        "Label" : { "default" : "Network Configuration" },
        "Parameters" : [ "VPCID", "SubnetId", "SecurityGroupID" ]
      },
      {
        "Label" : { "default":"Amazon EC2 Configuration" },
        "Parameters" : [ "InstanceType", "KeyName" ]
      }
    ],
    "ParameterLabels" : {
      "VPCID" : { "default" : "Which VPC should this be deployed to?" }
    }
  }
}
```

### YAML<a name="aws-resource-cloudformation-interface-example.yaml"></a>

```
Metadata: 
  AWS::CloudFormation::Interface: 
    ParameterGroups: 
      - 
        Label: 
          default: "Network Configuration"
        Parameters: 
          - VPCID
          - SubnetId
          - SecurityGroupID
      - 
        Label: 
          default: "Amazon EC2 Configuration"
        Parameters: 
          - InstanceType
          - KeyName
    ParameterLabels: 
      VPCID: 
        default: "Which VPC should this be deployed to?"
```

### Parameter groups in the console<a name="w7739ab1c27c15c15c27c15c10"></a>

Using the metadata key from this example, the following figure shows how the console displays parameter groups when a stack is created or updated: **Parameter groups in the console** 

![\[Console showing parameter groups for this example.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/console-create-stack-parameter-groups.png)