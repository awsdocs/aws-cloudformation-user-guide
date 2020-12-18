# AWS::Redshift::ClusterSecurityGroupIngress<a name="aws-resource-redshift-clustersecuritygroupingress"></a>

Adds an inbound \(ingress\) rule to an Amazon Redshift security group\. Depending on whether the application accessing your cluster is running on the Internet or an Amazon EC2 instance, you can authorize inbound access to either a Classless Interdomain Routing \(CIDR\)/Internet Protocol \(IP\) range or to an Amazon EC2 security group\. You can add as many as 20 ingress rules to an Amazon Redshift security group\.

If you authorize access to an Amazon EC2 security group, specify *EC2SecurityGroupName* and *EC2SecurityGroupOwnerId*\. The Amazon EC2 security group and Amazon Redshift cluster must be in the same AWS Region\. 

If you authorize access to a CIDR/IP address range, specify *CIDRIP*\. For an overview of CIDR blocks, see the Wikipedia article on [Classless Inter\-Domain Routing](http://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)\. 

You must also associate the security group with a cluster so that clients running on these IP addresses or the EC2 instance are authorized to connect to the cluster\. For information about managing security groups, go to [Working with Security Groups](https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-security-groups.html) in the *Amazon Redshift Cluster Management Guide*\.

## Syntax<a name="aws-resource-redshift-clustersecuritygroupingress-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-clustersecuritygroupingress-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::ClusterSecurityGroupIngress",
  "Properties" : {
      "[CIDRIP](#cfn-redshift-clustersecuritygroupingress-cidrip)" : String,
      "[ClusterSecurityGroupName](#cfn-redshift-clustersecuritygroupingress-clustersecuritygroupname)" : String,
      "[EC2SecurityGroupName](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupname)" : String,
      "[EC2SecurityGroupOwnerId](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupownerid)" : String
    }
}
```

### YAML<a name="aws-resource-redshift-clustersecuritygroupingress-syntax.yaml"></a>

```
Type: AWS::Redshift::ClusterSecurityGroupIngress
Properties: 
  [CIDRIP](#cfn-redshift-clustersecuritygroupingress-cidrip): String
  [ClusterSecurityGroupName](#cfn-redshift-clustersecuritygroupingress-clustersecuritygroupname): String
  [EC2SecurityGroupName](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupname): String
  [EC2SecurityGroupOwnerId](#cfn-redshift-clustersecuritygroupingress-ec2securitygroupownerid): String
```

## Properties<a name="aws-resource-redshift-clustersecuritygroupingress-properties"></a>

`CIDRIP`  <a name="cfn-redshift-clustersecuritygroupingress-cidrip"></a>
The IP range to be added the Amazon Redshift security group\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterSecurityGroupName`  <a name="cfn-redshift-clustersecuritygroupingress-clustersecuritygroupname"></a>
The name of the security group to which the ingress rule is added\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EC2SecurityGroupName`  <a name="cfn-redshift-clustersecuritygroupingress-ec2securitygroupname"></a>
The EC2 security group to be added the Amazon Redshift security group\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EC2SecurityGroupOwnerId`  <a name="cfn-redshift-clustersecuritygroupingress-ec2securitygroupownerid"></a>
The AWS account number of the owner of the security group specified by the *EC2SecurityGroupName* parameter\. The AWS Access Key ID is not an acceptable value\.   
Example: `111122223333`   
Conditional\. If you specify the `EC2SecurityGroupName` property, you must specify this property\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-redshift-clustersecuritygroupingress--examples"></a>



### Ingress Rules<a name="aws-resource-redshift-clustersecuritygroupingress--examples--Ingress_Rules"></a>

The following snippet describes a ingress rules for an Amazon Redshift cluster security group\.

#### JSON<a name="aws-resource-redshift-clustersecuritygroupingress--examples--Ingress_Rules--json"></a>

```
"myClusterSecurityGroupIngressIP" : {
  "Type": "AWS::Redshift::ClusterSecurityGroupIngress",
  "Properties": {
    "ClusterSecurityGroupName" : {"Ref":"myClusterSecurityGroup"},
    "CIDRIP" : "10.0.0.0/16"
  }
}
```

#### YAML<a name="aws-resource-redshift-clustersecuritygroupingress--examples--Ingress_Rules--yaml"></a>

```
myClusterSecurityGroupIngressIP: 
  Type: "AWS::Redshift::ClusterSecurityGroupIngress"
  Properties: 
    ClusterSecurityGroupName: 
    Ref: "myClusterSecurityGroup"
    CIDRIP: "10.0.0.0/16"
```