# AWS::VpcLattice::TargetGroup Target<a name="aws-properties-vpclattice-targetgroup-target"></a>

Describes a target\.

## Syntax<a name="aws-properties-vpclattice-targetgroup-target-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-targetgroup-target-syntax.json"></a>

```
{
  "[Id](#cfn-vpclattice-targetgroup-target-id)" : String,
  "[Port](#cfn-vpclattice-targetgroup-target-port)" : Integer
}
```

### YAML<a name="aws-properties-vpclattice-targetgroup-target-syntax.yaml"></a>

```
  [Id](#cfn-vpclattice-targetgroup-target-id): String
  [Port](#cfn-vpclattice-targetgroup-target-port): Integer
```

## Properties<a name="aws-properties-vpclattice-targetgroup-target-properties"></a>

`Id`  <a name="cfn-vpclattice-targetgroup-target-id"></a>
The ID of the target\. If the target group type is `INSTANCE`, this is an instance ID\. If the target group type is `IP`, this is an IP address\. If the target group type is `LAMBDA`, this is the ARN of a Lambda function\. If the target group type is `ALB`, this is the ARN of an Application Load Balancer\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-vpclattice-targetgroup-target-port"></a>
The port on which the target is listening\. For HTTP, the default is 80\. For HTTPS, the default is 443\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)