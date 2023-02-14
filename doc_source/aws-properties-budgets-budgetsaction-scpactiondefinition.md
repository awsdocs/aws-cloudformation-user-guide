# AWS::Budgets::BudgetsAction ScpActionDefinition<a name="aws-properties-budgets-budgetsaction-scpactiondefinition"></a>

The service control policies \(SCP\) action definition details\.

## Syntax<a name="aws-properties-budgets-budgetsaction-scpactiondefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budgetsaction-scpactiondefinition-syntax.json"></a>

```
{
  "[PolicyId](#cfn-budgets-budgetsaction-scpactiondefinition-policyid)" : String,
  "[TargetIds](#cfn-budgets-budgetsaction-scpactiondefinition-targetids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-budgets-budgetsaction-scpactiondefinition-syntax.yaml"></a>

```
  [PolicyId](#cfn-budgets-budgetsaction-scpactiondefinition-policyid): String
  [TargetIds](#cfn-budgets-budgetsaction-scpactiondefinition-targetids): 
    - String
```

## Properties<a name="aws-properties-budgets-budgetsaction-scpactiondefinition-properties"></a>

`PolicyId`  <a name="cfn-budgets-budgetsaction-scpactiondefinition-policyid"></a>
The policy ID attached\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `10`  
*Maximum*: `130`  
*Pattern*: `^p-[0-9a-zA-Z_]{8,128}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetIds`  <a name="cfn-budgets-budgetsaction-scpactiondefinition-targetids"></a>
A list of target IDs\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)