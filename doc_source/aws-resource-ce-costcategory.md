# AWS::CE::CostCategory<a name="aws-resource-ce-costcategory"></a>

The `AWS::CE::CostCategory` resource creates groupings of cost that you can use across products in the AWS Billing and Cost Management console, such as Cost Explorer and AWS Budgets\. For more information, see [Managing Your Costs with Cost Categories](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/manage-cost-categories.html) in the *AWS Billing and Cost Management User Guide*\.

## Syntax<a name="aws-resource-ce-costcategory-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ce-costcategory-syntax.json"></a>

```
{
  "Type" : "AWS::CE::CostCategory",
  "Properties" : {
      "[Name](#cfn-ce-costcategory-name)" : String,
      "[Rules](#cfn-ce-costcategory-rules)" : String,
      "[RuleVersion](#cfn-ce-costcategory-ruleversion)" : String
    }
}
```

### YAML<a name="aws-resource-ce-costcategory-syntax.yaml"></a>

```
Type: AWS::CE::CostCategory
Properties: 
  [Name](#cfn-ce-costcategory-name): String
  [Rules](#cfn-ce-costcategory-rules): String
  [RuleVersion](#cfn-ce-costcategory-ruleversion): String
```

## Properties<a name="aws-resource-ce-costcategory-properties"></a>

`Name`  <a name="cfn-ce-costcategory-name"></a>
The unique name of the Cost Category\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rules`  <a name="cfn-ce-costcategory-rules"></a>
 The array of CostCategoryRule in JSON array format\.  
Rules are processed in order\. If there are multiple rules that match the line item, then the first rule to match is used to determine that Cost Category value\. 
*Required*: Yes  
*Type*: String  
*Maximum*: `500`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleVersion`  <a name="cfn-ce-costcategory-ruleversion"></a>
The rule schema version in this particular Cost Category\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ce-costcategory-return-values"></a>

### Ref<a name="aws-resource-ce-costcategory-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Arn of the Cost Category that is created by the template\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ce-costcategory-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ce-costcategory-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The unique identifier for your Cost Category\.

`EffectiveStart`  <a name="EffectiveStart-fn::getatt"></a>
The Cost Category's effective start date\.

## Examples<a name="aws-resource-ce-costcategory--examples"></a>



### Cost Category Department with two rules<a name="aws-resource-ce-costcategory--examples--Cost_Category_Department_with_two_rules"></a>

The following example creates a Cost Category "Department" with two rules\.

#### JSON<a name="aws-resource-ce-costcategory--examples--Cost_Category_Department_with_two_rules--json"></a>

```
{
  "CostCategoryDepartment": {
    "Type": "AWS::CE::CostCategory",
    "Properties": {
      "Name": "Department",
      "RuleVersion": "CostCategoryExpression.v1",
      "Rules": "[
        {
          \"Value\":\"Engineering\",
          \"Rule\": {
            \"Dimensions\": {
            \"Key\": \"LINKED_ACCOUNT\",
            \"Values\": [ \"111111111111\" ]
            }
          }
        },
        {
          \"Value\": \"Marketing\",
          \"Rule\": {
            \"Dimensions\": {
            \"Key\": \"LINKED_ACCOUNT\",
            \"Values\": [ \"222222222222\" ] 
            }
          } 
        } 
        ]"
      }
    }
  }
```

#### YAML<a name="aws-resource-ce-costcategory--examples--Cost_Category_Department_with_two_rules--yaml"></a>

```
  CostCategoryDepartment:
    Type: 'AWS::CE::CostCategory'
    Properties:
      Name: Department
      RuleVersion: CostCategoryExpression.v1
      Rules: '
        [
          {
            "Value":"Engineering",
            "Rule": {
              "Dimensions": {
                "Key": "LINKED_ACCOUNT",
                "Values": [ "111111111111" ]
          }
        }
      },
      {
        "Value":"Marketing",
        "Rule": {
          "Dimensions": {
          "Key": "LINKED_ACCOUNT",
          "Values": [ "222222222222" ]
          }
        }

    ]'
```

## See also<a name="aws-resource-ce-costcategory--seealso"></a>
+  [CostCategory](https://docs.aws.amazon.com/aws-cost-management/latest/APIReference/API_CostCategory.html) in the *AWS Billing and Cost Management API Reference*\. 

