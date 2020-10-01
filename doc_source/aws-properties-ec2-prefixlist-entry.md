# AWS::EC2::PrefixList Entry<a name="aws-properties-ec2-prefixlist-entry"></a>

An entry for a prefix list\.

## Syntax<a name="aws-properties-ec2-prefixlist-entry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-prefixlist-entry-syntax.json"></a>

```
{
  "[Cidr](#cfn-ec2-prefixlist-entry-cidr)" : String,
  "[Description](#cfn-ec2-prefixlist-entry-description)" : String
}
```

### YAML<a name="aws-properties-ec2-prefixlist-entry-syntax.yaml"></a>

```
  [Cidr](#cfn-ec2-prefixlist-entry-cidr): String
  [Description](#cfn-ec2-prefixlist-entry-description): String
```

## Properties<a name="aws-properties-ec2-prefixlist-entry-properties"></a>

`Cidr`  <a name="cfn-ec2-prefixlist-entry-cidr"></a>
The CIDR block\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ec2-prefixlist-entry-description"></a>
A description for the entry\.  
Constraints: Up to 255 characters in length\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)