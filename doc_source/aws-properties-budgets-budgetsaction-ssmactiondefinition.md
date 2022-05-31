# AWS::Budgets::BudgetsAction SsmActionDefinition<a name="aws-properties-budgets-budgetsaction-ssmactiondefinition"></a>

The Amazon EC2 Systems Manager \(SSM\) action definition details\.

## Syntax<a name="aws-properties-budgets-budgetsaction-ssmactiondefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-budgets-budgetsaction-ssmactiondefinition-syntax.json"></a>

```
{
  "[InstanceIds](#cfn-budgets-budgetsaction-ssmactiondefinition-instanceids)" : [ String, ... ],
  "[Region](#cfn-budgets-budgetsaction-ssmactiondefinition-region)" : String,
  "[Subtype](#cfn-budgets-budgetsaction-ssmactiondefinition-subtype)" : String
}
```

### YAML<a name="aws-properties-budgets-budgetsaction-ssmactiondefinition-syntax.yaml"></a>

```
  [InstanceIds](#cfn-budgets-budgetsaction-ssmactiondefinition-instanceids): 
    - String
  [Region](#cfn-budgets-budgetsaction-ssmactiondefinition-region): String
  [Subtype](#cfn-budgets-budgetsaction-ssmactiondefinition-subtype): String
```

## Properties<a name="aws-properties-budgets-budgetsaction-ssmactiondefinition-properties"></a>

`InstanceIds`  <a name="cfn-budgets-budgetsaction-ssmactiondefinition-instanceids"></a>
The EC2 and RDS instance IDs\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-budgets-budgetsaction-ssmactiondefinition-region"></a>
The Region to run the \(SSM\) document\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `9`  
*Maximum*: `20`  
*Pattern*: `^\w{2}-\w+(-\w+)?-\d$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subtype`  <a name="cfn-budgets-budgetsaction-ssmactiondefinition-subtype"></a>
The action subType\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `STOP_EC2_INSTANCES | STOP_RDS_INSTANCES`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)