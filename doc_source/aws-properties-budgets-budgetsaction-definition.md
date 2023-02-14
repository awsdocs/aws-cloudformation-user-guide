# AWS::Budgets::BudgetsAction Definition<a name="aws-properties-budgets-budgetsaction-definition"></a>

The definition is where you specify all of the type\-specific parameters\.

## Syntax<a name="aws-properties-budgets-budgetsaction-definition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budgetsaction-definition-syntax.json"></a>

```
{
  "[IamActionDefinition](#cfn-budgets-budgetsaction-definition-iamactiondefinition)" : IamActionDefinition,
  "[ScpActionDefinition](#cfn-budgets-budgetsaction-definition-scpactiondefinition)" : ScpActionDefinition,
  "[SsmActionDefinition](#cfn-budgets-budgetsaction-definition-ssmactiondefinition)" : SsmActionDefinition
}
```

### YAML<a name="aws-properties-budgets-budgetsaction-definition-syntax.yaml"></a>

```
  [IamActionDefinition](#cfn-budgets-budgetsaction-definition-iamactiondefinition): 
    IamActionDefinition
  [ScpActionDefinition](#cfn-budgets-budgetsaction-definition-scpactiondefinition): 
    ScpActionDefinition
  [SsmActionDefinition](#cfn-budgets-budgetsaction-definition-ssmactiondefinition): 
    SsmActionDefinition
```

## Properties<a name="aws-properties-budgets-budgetsaction-definition-properties"></a>

`IamActionDefinition`  <a name="cfn-budgets-budgetsaction-definition-iamactiondefinition"></a>
The AWS Identity and Access Management \(IAM\) action definition details\.  
*Required*: No  
*Type*: [IamActionDefinition](aws-properties-budgets-budgetsaction-iamactiondefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScpActionDefinition`  <a name="cfn-budgets-budgetsaction-definition-scpactiondefinition"></a>
The service control policies \(SCP\) action definition details\.  
*Required*: No  
*Type*: [ScpActionDefinition](aws-properties-budgets-budgetsaction-scpactiondefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SsmActionDefinition`  <a name="cfn-budgets-budgetsaction-definition-ssmactiondefinition"></a>
The Amazon EC2 Systems Manager \(SSM\) action definition details\.  
*Required*: No  
*Type*: [SsmActionDefinition](aws-properties-budgets-budgetsaction-ssmactiondefinition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)