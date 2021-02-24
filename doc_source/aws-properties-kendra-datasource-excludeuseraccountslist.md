# AWS::Kendra::DataSource ExcludeUserAccountsList<a name="aws-properties-kendra-datasource-excludeuseraccountslist"></a>

A list of user email addresses\. Documents owned by these users are excluded from the index\. 

## Syntax<a name="aws-properties-kendra-datasource-excludeuseraccountslist-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-excludeuseraccountslist-syntax.json"></a>

```
{
  "[ExcludeUserAccountsList](#cfn-kendra-datasource-excludeuseraccountslist-excludeuseraccountslist)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-excludeuseraccountslist-syntax.yaml"></a>

```
  [ExcludeUserAccountsList](#cfn-kendra-datasource-excludeuseraccountslist-excludeuseraccountslist): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-excludeuseraccountslist-properties"></a>

`ExcludeUserAccountsList`  <a name="cfn-kendra-datasource-excludeuseraccountslist-excludeuseraccountslist"></a>
A list of strings containing the email addresses of the accounts to exclude\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-excludeuseraccountslist) of [String](#aws-properties-kendra-datasource-excludeuseraccountslist)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)