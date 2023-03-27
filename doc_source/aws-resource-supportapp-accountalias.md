# AWS::SupportApp::AccountAlias<a name="aws-resource-supportapp-accountalias"></a>

You can use the `AWS::SupportApp::AccountAlias` resource to specify your AWS account when you configure the AWS Support App in Slack\. Your alias name appears on the AWS Support App page in the Support Center Console and in messages from the AWS Support App\. You can use this alias to identify the account you've configured with the AWS Support App\.

For more information, see [AWS Support App in Slack](https://docs.aws.amazon.com/awssupport/latest/user/aws-support-app-for-slack.html) in the *AWS Support User Guide*\.

## Syntax<a name="aws-resource-supportapp-accountalias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-supportapp-accountalias-syntax.json"></a>

```
{
  "Type" : "AWS::SupportApp::AccountAlias",
  "Properties" : {
      "[AccountAlias](#cfn-supportapp-accountalias-accountalias)" : String
    }
}
```

### YAML<a name="aws-resource-supportapp-accountalias-syntax.yaml"></a>

```
Type: AWS::SupportApp::AccountAlias
Properties: 
  [AccountAlias](#cfn-supportapp-accountalias-accountalias): String
```

## Properties<a name="aws-resource-supportapp-accountalias-properties"></a>

`AccountAlias`  <a name="cfn-supportapp-accountalias-accountalias"></a>
An alias or short name for an AWS account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-supportapp-accountalias-return-values"></a>

### Fn::GetAtt<a name="aws-resource-supportapp-accountalias-return-values-fn--getatt"></a>

#### <a name="aws-resource-supportapp-accountalias-return-values-fn--getatt-fn--getatt"></a>

`AccountAliasResourceId`  <a name="AccountAliasResourceId-fn::getatt"></a>
The `AccountAlias` resource type has an attribute `AccountAliasResourceId`\. You can use this attribute to identify the resource\.  
The `AccountAliasResourceId` will be `AccountAlias_for_accountId`\. In this example, `AccountAlias_for_` is the prefix and `accountId` is your AWS account number, such as `AccountAlias_for_123456789012`\.