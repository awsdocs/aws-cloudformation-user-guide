# AWS::Kendra::DataSource SalesforceChatterFeedIncludeFilterTypes<a name="aws-properties-kendra-datasource-salesforcechatterfeedincludefiltertypes"></a>

Specifies filters for a feed based on the status of the user\.

## Syntax<a name="aws-properties-kendra-datasource-salesforcechatterfeedincludefiltertypes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-salesforcechatterfeedincludefiltertypes-syntax.json"></a>

```
{
  "[SalesforceChatterFeedIncludeFilterTypes](#cfn-kendra-datasource-salesforcechatterfeedincludefiltertypes-salesforcechatterfeedincludefiltertypes)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-kendra-datasource-salesforcechatterfeedincludefiltertypes-syntax.yaml"></a>

```
  [SalesforceChatterFeedIncludeFilterTypes](#cfn-kendra-datasource-salesforcechatterfeedincludefiltertypes-salesforcechatterfeedincludefiltertypes): 
    - String
```

## Properties<a name="aws-properties-kendra-datasource-salesforcechatterfeedincludefiltertypes-properties"></a>

`SalesforceChatterFeedIncludeFilterTypes`  <a name="cfn-kendra-datasource-salesforcechatterfeedincludefiltertypes-salesforcechatterfeedincludefiltertypes"></a>
A filter that determines the type of user whose documents should be indexed\. When you specify `ACTIVE_USERS` only documents from users who have an active account are indexed\. When you specify `STANDARD_USER` only documents for Salesforce standard users are documented\. You can specify both\.  
*Required*: No  
*Type*: [List](#aws-properties-kendra-datasource-salesforcechatterfeedincludefiltertypes) of [String](#aws-properties-kendra-datasource-salesforcechatterfeedincludefiltertypes)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)