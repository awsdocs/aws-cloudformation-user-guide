# AWS::Redshift::ClusterSecurityGroupIngress<a name="aws-resource-redshift-clustersecuritygroupingress"></a>

Specifies inbound \(ingress\) rules for an Amazon Redshift security group\.

**Topics**
+ [Syntax](#aws-resource-redshift-clustersecuritygroupingress-syntax)
+ [Properties](#w3ab2c21c10e1005b9)
+ [Template Snippet](#w3ab2c21c10e1005c11)
+ [See Also](#w3ab2c21c10e1005c13)

## Syntax<a name="aws-resource-redshift-clustersecuritygroupingress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-clustersecuritygroupingress-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::ClusterSecurityGroupIngress",
  "Properties" : {
    "[ClusterSecurityGroupName](#cfn-redshift-clustersecuritygroupingress-clustersecuritygroupname)" : String,
    "[CIDRIP](#cfn-redshift-clustersecuritygroupingress-cidrip)" : String,
    "[EC2SecurityGroupName](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupname)" : String,
    "[EC2SecurityGroupOwnerId](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupownerid)" : String
  }
}
```

### YAML<a name="aws-resource-redshift-clustersecuritygroupingress-syntax.yaml"></a>

```
Type: "AWS::Redshift::ClusterSecurityGroupIngress"
Properties: 
  [ClusterSecurityGroupName](#cfn-redshift-clustersecuritygroupingress-clustersecuritygroupname): String
  [CIDRIP](#cfn-redshift-clustersecuritygroupingress-cidrip): String
  [EC2SecurityGroupName](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupname): String
  [EC2SecurityGroupOwnerId](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupownerid): String
```

## Properties<a name="w3ab2c21c10e1005b9"></a>

`ClusterSecurityGroupName`  <a name="cfn-redshift-clustersecuritygroupingress-clustersecuritygroupname"></a>
The name of the Amazon Redshift security group that will be associated with the ingress rule\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`CIDRIP`  <a name="cfn-redshift-clustersecuritygroupingress-cidrip"></a>
The IP address range that has inbound access to the Amazon Redshift security group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EC2SecurityGroupName`  <a name="cfn-redshift-clustersecuritygroupingress-ec2securitygroupname"></a>
The Amazon EC2 security group that will be added the Amazon Redshift security group\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`EC2SecurityGroupOwnerId`  <a name="cfn-redshift-clustersecuritygroupingress-ec2securitygroupownerid"></a>
The 12\-digit AWS account number of the owner of the Amazon EC2 security group that is specified by the `EC2SecurityGroupName` parameter\.  
*Required*: Conditional\. If you specify the `EC2SecurityGroupName` property, you must specify this property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Template Snippet<a name="w3ab2c21c10e1005c11"></a>

The following snippet describes a ingress rules for an Amazon Redshift cluster security group:

### JSON<a name="aws-resource-redshift-clustersecuritygroupingress-example.json"></a>

```
"myClusterSecurityGroupIngressIP" : {
  "Type": "AWS::Redshift::ClusterSecurityGroupIngress",
  "Properties": {
    "ClusterSecurityGroupName" : {"Ref":"myClusterSecurityGroup"},
    "CIDRIP" : "10.0.0.0/16"
  }
}
```

### YAML<a name="aws-resource-redshift-clustersecuritygroupingress-example.yaml"></a>

```
myClusterSecurityGroupIngressIP: 
  Type: "AWS::Redshift::ClusterSecurityGroupIngress"
  Properties: 
    ClusterSecurityGroupName: 
      Ref: "myClusterSecurityGroup"
    CIDRIP: "10.0.0.0/16"
```

## See Also<a name="w3ab2c21c10e1005c13"></a>
+ [AWS::Redshift::ClusterSecurityGroup](aws-resource-redshift-clustersecuritygroup.md)