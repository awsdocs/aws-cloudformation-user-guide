# Amazon Elastic Compute Cloud SpotFleet IamInstanceProfile<a name="aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile"></a>

`IamInstanceProfile` is a property of the [Amazon Elastic Compute Cloud SpotFleet LaunchSpecifications](aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications.md) property that specifies the IAM instance profile to associate with the instances\.

## Syntax<a name="w3ab2c21c14d790b5"></a>

### JSON<a name="aws-properties-aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile-syntax.json"></a>

```
{
  "[Arn](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile-arn)" : String
}
```

### YAML<a name="aws-properties-aws-properties-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile-syntax.yaml"></a>

```
[Arn](#cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile-arn): String
```

## Properties<a name="w3ab2c21c14d790b7"></a>

`Arn`  <a name="cfn-ec2-spotfleet-spotfleetrequestconfigdata-launchspecifications-iaminstanceprofile-arn"></a>
The Amazon Resource Name \(ARN\) of the instance profile to associate with the instances\. The instance profile contains the IAM role that is associated with the instances\.  
*Required*: No  
*Type*: String