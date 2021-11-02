# AWS::EC2::LaunchTemplate TotalLocalStorageGB<a name="aws-properties-ec2-launchtemplate-totallocalstoragegb"></a>

The minimum and maximum amount of total local storage, in GB\.

## Syntax<a name="aws-properties-ec2-launchtemplate-totallocalstoragegb-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-launchtemplate-totallocalstoragegb-syntax.json"></a>

```
{
  "[Max](#cfn-ec2-launchtemplate-totallocalstoragegb-max)" : Double,
  "[Min](#cfn-ec2-launchtemplate-totallocalstoragegb-min)" : Double
}
```

### YAML<a name="aws-properties-ec2-launchtemplate-totallocalstoragegb-syntax.yaml"></a>

```
  [Max](#cfn-ec2-launchtemplate-totallocalstoragegb-max): Double
  [Min](#cfn-ec2-launchtemplate-totallocalstoragegb-min): Double
```

## Properties<a name="aws-properties-ec2-launchtemplate-totallocalstoragegb-properties"></a>

`Max`  <a name="cfn-ec2-launchtemplate-totallocalstoragegb-max"></a>
The maximum amount of total local storage, in GB\. To specify no maximum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Min`  <a name="cfn-ec2-launchtemplate-totallocalstoragegb-min"></a>
The minimum amount of total local storage, in GB\. To specify no minimum limit, omit this parameter\.  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)