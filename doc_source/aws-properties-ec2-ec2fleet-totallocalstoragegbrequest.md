# AWS::EC2::EC2Fleet TotalLocalStorageGBRequest<a name="aws-properties-ec2-ec2fleet-totallocalstoragegbrequest"></a>

The minimum and maximum amount of total local storage, in GB\.

## Syntax<a name="aws-properties-ec2-ec2fleet-totallocalstoragegbrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-ec2fleet-totallocalstoragegbrequest-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-ec2fleet-totallocalstoragegbrequest-max)" : Double,
  "[Min](#cfn-ec2-ec2fleet-totallocalstoragegbrequest-min)" : Double
}
```

### YAML<a name="aws-properties-ec2-ec2fleet-totallocalstoragegbrequest-syntax.yaml"></a>

```
  [Max](#cfn-ec2-ec2fleet-totallocalstoragegbrequest-max): Double
  [Min](#cfn-ec2-ec2fleet-totallocalstoragegbrequest-min): Double
```

## Properties<a name="aws-properties-ec2-ec2fleet-totallocalstoragegbrequest-properties"></a>

`Max`  <a name="cfn-ec2-ec2fleet-totallocalstoragegbrequest-max"></a>
The maximum amount of total local storage, in GB\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Min`  <a name="cfn-ec2-ec2fleet-totallocalstoragegbrequest-min"></a>
The minimum amount of total local storage, in GB\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)