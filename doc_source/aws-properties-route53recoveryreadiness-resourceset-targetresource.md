# AWS::Route53RecoveryReadiness::ResourceSet TargetResource<a name="aws-properties-route53recoveryreadiness-resourceset-targetresource"></a>

The target resource that the Route 53 record points to\.

## Syntax<a name="aws-properties-route53recoveryreadiness-resourceset-targetresource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53recoveryreadiness-resourceset-targetresource-syntax.json"></a>

```
{
  "[NLBResource](#cfn-route53recoveryreadiness-resourceset-targetresource-nlbresource)" : NLBResource,
  "[R53Resource](#cfn-route53recoveryreadiness-resourceset-targetresource-r53resource)" : R53ResourceRecord
}
```

### YAML<a name="aws-properties-route53recoveryreadiness-resourceset-targetresource-syntax.yaml"></a>

```
  [NLBResource](#cfn-route53recoveryreadiness-resourceset-targetresource-nlbresource): 
    NLBResource
  [R53Resource](#cfn-route53recoveryreadiness-resourceset-targetresource-r53resource): 
    R53ResourceRecord
```

## Properties<a name="aws-properties-route53recoveryreadiness-resourceset-targetresource-properties"></a>

`NLBResource`  <a name="cfn-route53recoveryreadiness-resourceset-targetresource-nlbresource"></a>
The Network Load Balancer resource that a DNS target resource points to\.  
*Required*: No  
*Type*: [NLBResource](aws-properties-route53recoveryreadiness-resourceset-nlbresource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`R53Resource`  <a name="cfn-route53recoveryreadiness-resourceset-targetresource-r53resource"></a>
The Route 53 resource that a DNS target resource record points to\.  
*Required*: No  
*Type*: [R53ResourceRecord](aws-properties-route53recoveryreadiness-resourceset-r53resourcerecord.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)