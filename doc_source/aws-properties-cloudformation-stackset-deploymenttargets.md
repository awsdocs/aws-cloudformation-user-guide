# AWS::CloudFormation::StackSet DeploymentTargets<a name="aws-properties-cloudformation-stackset-deploymenttargets"></a>

The AWS OrganizationalUnitIds or Accounts for which to create stack instances in the specified Regions\.

## Syntax<a name="aws-properties-cloudformation-stackset-deploymenttargets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudformation-stackset-deploymenttargets-syntax.json"></a>

```
{
  "[Accounts](#cfn-cloudformation-stackset-deploymenttargets-accounts)" : [ String, ... ],
  "[OrganizationalUnitIds](#cfn-cloudformation-stackset-deploymenttargets-organizationalunitids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudformation-stackset-deploymenttargets-syntax.yaml"></a>

```
  [Accounts](#cfn-cloudformation-stackset-deploymenttargets-accounts): 
    - String
  [OrganizationalUnitIds](#cfn-cloudformation-stackset-deploymenttargets-organizationalunitids): 
    - String
```

## Properties<a name="aws-properties-cloudformation-stackset-deploymenttargets-properties"></a>

`Accounts`  <a name="cfn-cloudformation-stackset-deploymenttargets-accounts"></a>
The names of one or more AWS accounts for which you want to deploy stack set updates\.  
*Pattern*: `^[0-9]{12}$`  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationalUnitIds`  <a name="cfn-cloudformation-stackset-deploymenttargets-organizationalunitids"></a>
The organization root ID or organizational unit \(OU\) IDs to which StackSets deploys\.  
*Pattern*: `^(ou-[a-z0-9]{4,32}-[a-z0-9]{8,32}|r-[a-z0-9]{4,32})$`  
*Required*: Conditional  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)