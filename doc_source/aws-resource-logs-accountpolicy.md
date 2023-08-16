# AWS::Logs::AccountPolicy<a name="aws-resource-logs-accountpolicy"></a>

Creates or updates an account\-level data protection policy that applies to all log groups in the account\. A data protection policy can help safeguard sensitive data that's ingested by your log groups by auditing and masking the sensitive log data\. Each account can have only one account\-level policy\.

**Important**  
Sensitive data is detected and masked when it is ingested into a log group\. When you set a data protection policy, log events ingested into the log groups before that time are not masked\.

If you create a data protection policy for your whole account, it applies to both existing log groups and all log groups that are created later in this account\. The account policy is applied to existing log groups with eventual consistency\. It might take up to 5 minutes before sensitive data in existing log groups begins to be masked\.

By default, when a user views a log event that includes masked data, the sensitive data is replaced by asterisks\. A user who has the `logs:Unmask` permission can use a [GetLogEvents](https://docs.aws.amazon.com/AmazonCloudWatchLogs/latest/APIReference/API_GetLogEvents.html) or [FilterLogEvents](https://docs.aws.amazon.com/AmazonCloudWatchLogs/latest/APIReference/API_FilterLogEvents.html) operation with the `unmask` parameter set to `true` to view the unmasked log events\. Users with the `logs:Unmask` can also view unmasked data in the CloudWatch Logs console by running a CloudWatch Logs Insights query with the `unmask` query command\.

For more information, including a list of types of data that can be audited and masked, see [Protect sensitive log data with masking](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/mask-sensitive-log-data.html)\.

To create an account\-level policy, you must be signed on with the `logs:PutDataProtectionPolicy` and `logs:PutAccountPolicy` permissions\.

An account\-level policy applies to all log groups in the account\. You can also create a data protection policy that applies to just one log group\. If a log group has its own data protection policy and the account also has an account\-level data protection policy, then the two policies are cumulative\. Any sensitive term specified in either policy is masked\.

## Syntax<a name="aws-resource-logs-accountpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-logs-accountpolicy-syntax.json"></a>

```
{
  "Type" : "AWS::Logs::AccountPolicy",
  "Properties" : {
      "[PolicyDocument](#cfn-logs-accountpolicy-policydocument)" : String,
      "[PolicyName](#cfn-logs-accountpolicy-policyname)" : String,
      "[PolicyType](#cfn-logs-accountpolicy-policytype)" : String,
      "[Scope](#cfn-logs-accountpolicy-scope)" : String
    }
}
```

### YAML<a name="aws-resource-logs-accountpolicy-syntax.yaml"></a>

```
Type: AWS::Logs::AccountPolicy
Properties: 
  [PolicyDocument](#cfn-logs-accountpolicy-policydocument): String
  [PolicyName](#cfn-logs-accountpolicy-policyname): String
  [PolicyType](#cfn-logs-accountpolicy-policytype): String
  [Scope](#cfn-logs-accountpolicy-scope): String
```

## Properties<a name="aws-resource-logs-accountpolicy-properties"></a>

`PolicyDocument`  <a name="cfn-logs-accountpolicy-policydocument"></a>
Specify the data protection policy, in JSON\.  
This policy must include two JSON blocks:  
+ The first block must include both a `DataIdentifer` array and an `Operation` property with an `Audit` action\. The `DataIdentifer` array lists the types of sensitive data that you want to mask\. For more information about the available options, see [Types of data that you can mask](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/mask-sensitive-log-data-types.html)\.

  The `Operation` property with an `Audit` action is required to find the sensitive data terms\. This `Audit` action must contain a `FindingsDestination` object\. You can optionally use that `FindingsDestination` object to list one or more destinations to send audit findings to\. If you specify destinations such as log groups, Kinesis Data Firehose streams, and S3 buckets, they must already exist\.
+ The second block must include both a `DataIdentifer` array and an `Operation` property with an `Deidentify` action\. The `DataIdentifer` array must exactly match the `DataIdentifer` array in the first block of the policy\.

  The `Operation` property with the `Deidentify` action is what actually masks the data, and it must contain the ` "MaskConfig": {}` object\. The ` "MaskConfig": {}` object must be empty\.
The contents of the two `DataIdentifer` arrays must match exactly\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyName`  <a name="cfn-logs-accountpolicy-policyname"></a>
A name for the policy\. This must be unique within the account\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PolicyType`  <a name="cfn-logs-accountpolicy-policytype"></a>
Currently the only valid value for this parameter is `DATA_PROTECTION_POLICY`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Scope`  <a name="cfn-logs-accountpolicy-scope"></a>
Currently the only valid value for this parameter is `ALL`, which specifies that the data protection policy applies to all log groups in the account\. If you omit this parameter, the default of `ALL` is used\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-logs-accountpolicy-return-values"></a>

### Fn::GetAtt<a name="aws-resource-logs-accountpolicy-return-values-fn--getatt"></a>

#### <a name="aws-resource-logs-accountpolicy-return-values-fn--getatt-fn--getatt"></a>

`AccountId`  <a name="AccountId-fn::getatt"></a>
The account ID of the account where this policy was created\. For example, `123456789012`\.

## Examples<a name="aws-resource-logs-accountpolicy--examples"></a>



### Create an account policy<a name="aws-resource-logs-accountpolicy--examples--Create_an_account_policy"></a>

The following example creates an account policy that finds and masks email addresses in log events\. It also sends audit findings to the `EXISTING_LOG_GROUP_NAME` log group in CloudWatch Logs\.

#### JSON<a name="aws-resource-logs-accountpolicy--examples--Create_an_account_policy--json"></a>

```
{
    "Resources": {
        "AccountPolicy": {
            "Type": "AWS::Logs::AccountPolicy",
            "Properties": {
                "PolicyName": "TestPolicy",
                "PolicyDocument": "{ \"Name\": \"data-protection-policy\", \"Description\": \"\", \"Version\": \"2021-06-01\", \"Statement\": [ { \"Sid\": \"audit-policy\", \"DataIdentifier\": [ \"arn:aws:dataprotection::aws:data-identifier/EmailAddress\" ], \"Operation\": { \"Audit\": { \"FindingsDestination\": { \"CloudWatchLogs\": { \"LogGroup\": \"EXISTING_LOG_GROUP_NAME\" } } } } }, { \"Sid\": \"redact-policy\", \"DataIdentifier\": [ \"arn:aws:dataprotection::aws:data-identifier/EmailAddress\" ], \"Operation\": { \"Deidentify\": { \"MaskConfig\": {} } } } ] }",
                "PolicyType": "DATA_PROTECTION_POLICY",
                "Scope": "ALL"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-logs-accountpolicy--examples--Create_an_account_policy--yaml"></a>

```
Resources:
  AccountPolicy:
    Type: AWS::Logs::AccountPolicy
    Properties:
      PolicyName: "TestPolicy"
      PolicyDocument: '{
        "Name": "data-protection-policy",
        "Description": "",
        "Version": "2021-06-01",
        "Statement": [
          {
            "Sid": "audit-policy",
            "DataIdentifier": [
              "arn:aws:dataprotection::aws:data-identifier/EmailAddress"
            ],
            "Operation": {
              "Audit": {
                "FindingsDestination": {
                  "CloudWatchLogs": {
                    "LogGroup": "EXISTING_LOG_GROUP_NAME"
                  }
                }
              }
            }
          },
          {
            "Sid": "redact-policy",
            "DataIdentifier": [
              "arn:aws:dataprotection::aws:data-identifier/EmailAddress"
            ],
            "Operation": {
              "Deidentify": {
                "MaskConfig": {}
              }
            }
          }
        ]
      }'
      PolicyType: "DATA_PROTECTION_POLICY"
      Scope: "ALL"
```