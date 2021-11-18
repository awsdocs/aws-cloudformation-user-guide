# AWS::Redshift::EndpointAccess VpcSecurityGroup<a name="aws-properties-redshift-endpointaccess-vpcsecuritygroup"></a>

The security groups associated with the endpoint\.

## Syntax<a name="aws-properties-redshift-endpointaccess-vpcsecuritygroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-redshift-endpointaccess-vpcsecuritygroup-syntax.json"></a>

```
{
  "[Status](#cfn-redshift-endpointaccess-vpcsecuritygroup-status)" : String,
  "[VpcSecurityGroupId](#cfn-redshift-endpointaccess-vpcsecuritygroup-vpcsecuritygroupid)" : String
}
```

### YAML<a name="aws-properties-redshift-endpointaccess-vpcsecuritygroup-syntax.yaml"></a>

```
  [Status](#cfn-redshift-endpointaccess-vpcsecuritygroup-status): String
  [VpcSecurityGroupId](#cfn-redshift-endpointaccess-vpcsecuritygroup-vpcsecuritygroupid): String
```

## Properties<a name="aws-properties-redshift-endpointaccess-vpcsecuritygroup-properties"></a>

`Status`  <a name="cfn-redshift-endpointaccess-vpcsecuritygroup-status"></a>
The status of the endpoint\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupId`  <a name="cfn-redshift-endpointaccess-vpcsecuritygroup-vpcsecuritygroupid"></a>
The identifier of the VPC security group\.  
*Required*: No  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)