# AWS::EKS::Nodegroup RemoteAccess<a name="aws-properties-eks-nodegroup-remoteaccess"></a>

An object representing the remote access configuration for the managed node group\.

## Syntax<a name="aws-properties-eks-nodegroup-remoteaccess-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-eks-nodegroup-remoteaccess-syntax.json"></a>

```
{
  "[Ec2SshKey](#cfn-eks-nodegroup-remoteaccess-ec2sshkey)" : String,
  "[SourceSecurityGroups](#cfn-eks-nodegroup-remoteaccess-sourcesecuritygroups)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-eks-nodegroup-remoteaccess-syntax.yaml"></a>

```
  [Ec2SshKey](#cfn-eks-nodegroup-remoteaccess-ec2sshkey): String
  [SourceSecurityGroups](#cfn-eks-nodegroup-remoteaccess-sourcesecuritygroups): 
    - String
```

## Properties<a name="aws-properties-eks-nodegroup-remoteaccess-properties"></a>

`Ec2SshKey`  <a name="cfn-eks-nodegroup-remoteaccess-ec2sshkey"></a>
The Amazon EC2 SSH key that provides access for SSH communication with the nodes in the managed node group\. For more information, see [Amazon EC2 Key Pairs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html) in the *Amazon Elastic Compute Cloud User Guide for Linux Instances*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceSecurityGroups`  <a name="cfn-eks-nodegroup-remoteaccess-sourcesecuritygroups"></a>
The security groups that are allowed SSH access \(port 22\) to the nodes\. If you specify an Amazon EC2 SSH key but do not specify a source security group when you create a managed node group, then port 22 on the nodes is opened to the internet \(0\.0\.0\.0/0\)\. For more information, see [Security Groups for Your VPC](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_SecurityGroups.html) in the *Amazon Virtual Private Cloud User Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)