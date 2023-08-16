# AWS::EC2::VerifiedAccessInstance KinesisDataFirehose<a name="aws-properties-ec2-verifiedaccessinstance-kinesisdatafirehose"></a>

Options for Kinesis as a logging destination\.

## Syntax<a name="aws-properties-ec2-verifiedaccessinstance-kinesisdatafirehose-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-verifiedaccessinstance-kinesisdatafirehose-syntax.json"></a>

```
{
  "[DeliveryStream](#cfn-ec2-verifiedaccessinstance-kinesisdatafirehose-deliverystream)" : String,
  "[Enabled](#cfn-ec2-verifiedaccessinstance-kinesisdatafirehose-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-ec2-verifiedaccessinstance-kinesisdatafirehose-syntax.yaml"></a>

```
  [DeliveryStream](#cfn-ec2-verifiedaccessinstance-kinesisdatafirehose-deliverystream): String
  [Enabled](#cfn-ec2-verifiedaccessinstance-kinesisdatafirehose-enabled): Boolean
```

## Properties<a name="aws-properties-ec2-verifiedaccessinstance-kinesisdatafirehose-properties"></a>

`DeliveryStream`  <a name="cfn-ec2-verifiedaccessinstance-kinesisdatafirehose-deliverystream"></a>
The ID of the delivery stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-ec2-verifiedaccessinstance-kinesisdatafirehose-enabled"></a>
Indicates whether logging is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)