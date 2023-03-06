# AWS::CloudFormation::StackSet DeploymentTargets<a name="aws-properties-cloudformation-stackset-deploymenttargets"></a>

The AWS OrganizationalUnitIds or Accounts for which to create stack instances in the specified Regions\.

## Syntax<a name="aws-properties-cloudformation-stackset-deploymenttargets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudformation-stackset-deploymenttargets-syntax.json"></a>

```
{
  "[AccountFilterType](#cfn-cloudformation-stackset-deploymenttargets-accountfiltertype)" : String,
  "[Accounts](#cfn-cloudformation-stackset-deploymenttargets-accounts)" : [ String, ... ],
  "[OrganizationalUnitIds](#cfn-cloudformation-stackset-deploymenttargets-organizationalunitids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudformation-stackset-deploymenttargets-syntax.yaml"></a>

```
  [AccountFilterType](#cfn-cloudformation-stackset-deploymenttargets-accountfiltertype): String
  [Accounts](#cfn-cloudformation-stackset-deploymenttargets-accounts): 
    - String
  [OrganizationalUnitIds](#cfn-cloudformation-stackset-deploymenttargets-organizationalunitids): 
    - String
```

## Properties<a name="aws-properties-cloudformation-stackset-deploymenttargets-properties"></a>

`AccountFilterType`  <a name="cfn-cloudformation-stackset-deploymenttargets-accountfiltertype"></a>
Limit deployment targets to individual accounts or include additional accounts with provided OUs\.  
The following is a list of possible values for the `AccountFilterType` operation\.  
+  `INTERSECTION`: StackSets deploys to the accounts specified in `Accounts` parameter\. 
+  `DIFFERENCE`: StackSets excludes the accounts specified in `Accounts` parameter\. This enables user to avoid certain accounts within an OU such as suspended accounts\.
+  `UNION`: StackSets includes additional accounts deployment targets\. 

  This is the default value if `AccountFilterType` is not provided\. This enables user to update an entire OU and individual accounts from a different OU in one request, which used to be two separate requests\.
+  `NONE`: Deploys to all the accounts in specified organizational units \(OU\)\.
*Required*: No  
*Type*: String  
*Allowed values*: `DIFFERENCE | INTERSECTION | NONE | UNION`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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