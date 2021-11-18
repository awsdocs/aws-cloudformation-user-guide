# AWS::Route53RecoveryReadiness::ResourceSet R53ResourceRecord<a name="aws-properties-route53recoveryreadiness-resourceset-r53resourcerecord"></a>

The Route 53 resource that a DNS target resource record points to\.

## Syntax<a name="aws-properties-route53recoveryreadiness-resourceset-r53resourcerecord-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53recoveryreadiness-resourceset-r53resourcerecord-syntax.json"></a>

```
{
  "[DomainName](#cfn-route53recoveryreadiness-resourceset-r53resourcerecord-domainname)" : String,
  "[RecordSetId](#cfn-route53recoveryreadiness-resourceset-r53resourcerecord-recordsetid)" : String
}
```

### YAML<a name="aws-properties-route53recoveryreadiness-resourceset-r53resourcerecord-syntax.yaml"></a>

```
  [DomainName](#cfn-route53recoveryreadiness-resourceset-r53resourcerecord-domainname): String
  [RecordSetId](#cfn-route53recoveryreadiness-resourceset-r53resourcerecord-recordsetid): String
```

## Properties<a name="aws-properties-route53recoveryreadiness-resourceset-r53resourcerecord-properties"></a>

`DomainName`  <a name="cfn-route53recoveryreadiness-resourceset-r53resourcerecord-domainname"></a>
The DNS target domain name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RecordSetId`  <a name="cfn-route53recoveryreadiness-resourceset-r53resourcerecord-recordsetid"></a>
The Route 53 Resource Record Set ID\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)