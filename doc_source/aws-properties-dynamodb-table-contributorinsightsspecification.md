# AWS::DynamoDB::Table ContributorInsightsSpecification<a name="aws-properties-dynamodb-table-contributorinsightsspecification"></a>

The settings used to enable or disable CloudWatch Contributor Insights\.

## Syntax<a name="aws-properties-dynamodb-table-contributorinsightsspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-contributorinsightsspecification-syntax.json"></a>

```
{
  "[Enabled](#cfn-dynamodb-table-contributorinsightsspecification-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-dynamodb-table-contributorinsightsspecification-syntax.yaml"></a>

```
  [Enabled](#cfn-dynamodb-table-contributorinsightsspecification-enabled): Boolean
```

## Properties<a name="aws-properties-dynamodb-table-contributorinsightsspecification-properties"></a>

`Enabled`  <a name="cfn-dynamodb-table-contributorinsightsspecification-enabled"></a>
Indicates whether CloudWatch Contributor Insights are to be enabled \(true\) or disabled \(false\)\.  
*Required*: Yes  
*Type*: Boolean  
*Allowed values*: `DISABLE | ENABLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)