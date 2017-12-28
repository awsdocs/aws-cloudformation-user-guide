# AWS::Redshift::ClusterSecurityGroupIngress<a name="aws-resource-redshift-clustersecuritygroupingress"></a>

Specifies inbound \(ingress\) rules for an Amazon Redshift security group\.


+ [Syntax](#aws-resource-redshift-clustersecuritygroupingress-syntax)
+ [Properties](#w3ab2c21c10d932b9)
+ [Template Snippet](#w3ab2c21c10d932c11)
+ [See Also](#w3ab2c21c10d932c13)

## Syntax<a name="aws-resource-redshift-clustersecuritygroupingress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-clustersecuritygroupingress-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::ClusterSecurityGroupIngress",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-clustersecuritygroupingress-clustersecuritygroupname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-clustersecuritygroupingress-cidrip)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupname)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupownerid)" : String
  }
}
```

### YAML<a name="aws-resource-redshift-clustersecuritygroupingress-syntax.yaml"></a>

```
Type: "AWS::Redshift::ClusterSecurityGroupIngress"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-clustersecuritygroupingress-clustersecuritygroupname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-clustersecuritygroupingress-cidrip): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupname): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupownerid): String
```

## Properties<a name="w3ab2c21c10d932b9"></a>

`ClusterSecurityGroupName`  
The name of the Amazon Redshift security group that will be associated with the ingress rule\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`CIDRIP`  
The IP address range that has inbound access to the Amazon Redshift security group\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`EC2SecurityGroupName`  
The Amazon EC2 security group that will be added the Amazon Redshift security group\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`EC2SecurityGroupOwnerId`  
The 12\-digit AWS account number of the owner of the Amazon EC2 security group that is specified by the `EC2SecurityGroupName` parameter\.  
*Required: *Conditional\. If you specify the `EC2SecurityGroupName` property, you must specify this property\.  
*Type*: String  
*Update requires*: Replacement

## Template Snippet<a name="w3ab2c21c10d932c11"></a>

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

## See Also<a name="w3ab2c21c10d932c13"></a>

+ [AWS::Redshift::ClusterSecurityGroup](aws-resource-redshift-clustersecuritygroup.md)