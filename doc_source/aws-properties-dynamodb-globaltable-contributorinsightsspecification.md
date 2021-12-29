# AWS::DynamoDB::GlobalTable ContributorInsightsSpecification<a name="aws-properties-dynamodb-globaltable-contributorinsightsspecification"></a>

Configures contributor insights settings for a replica or one of its indexes\.

## Syntax<a name="aws-properties-dynamodb-globaltable-contributorinsightsspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-globaltable-contributorinsightsspecification-syntax.json"></a>

```
{
  "[Enabled](#cfn-dynamodb-globaltable-contributorinsightsspecification-enabled)" : Boolean
}
```

### YAML<a name="aws-properties-dynamodb-globaltable-contributorinsightsspecification-syntax.yaml"></a>

```
  [Enabled](#cfn-dynamodb-globaltable-contributorinsightsspecification-enabled): Boolean
```

## Properties<a name="aws-properties-dynamodb-globaltable-contributorinsightsspecification-properties"></a>

`Enabled`  <a name="cfn-dynamodb-globaltable-contributorinsightsspecification-enabled"></a>
Indicates whether CloudWatch Contributor Insights are to be enabled \(true\) or disabled \(false\)\.  
*Required*: Yes  
*Type*: Boolean  
*Allowed values*: `DISABLE | ENABLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)