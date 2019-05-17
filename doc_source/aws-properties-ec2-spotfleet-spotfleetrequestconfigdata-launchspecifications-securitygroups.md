# AWS::EC2::SpotFleet GroupIdentifier<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups"></a>

Describes a security group\.

## Syntax<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups-syntax.json"></a>

```
{
  "[GroupId](#cfn-ec2-spotfleet-groupidentifier-groupid)" : String
}
```

### YAML<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups-syntax.yaml"></a>

```
  [GroupId](#cfn-ec2-spotfleet-groupidentifier-groupid): String
```

## Properties<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-securitygroups-properties"></a>

`GroupId`  <a name="cfn-ec2-spotfleet-groupidentifier-groupid"></a>
The ID of the security group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)