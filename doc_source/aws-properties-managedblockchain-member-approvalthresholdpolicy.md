# AWS::ManagedBlockchain::Member ApprovalThresholdPolicy<a name="aws-properties-managedblockchain-member-approvalthresholdpolicy"></a>

A policy type that defines the voting rules for the network\. The rules decide if a proposal is approved\. Approval may be based on criteria such as the percentage of `YES` votes and the duration of the proposal\. The policy applies to all proposals and is specified when the network is created\.

Applies only to Hyperledger Fabric\.

## Syntax<a name="aws-properties-managedblockchain-member-approvalthresholdpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-managedblockchain-member-approvalthresholdpolicy-syntax.json"></a>

```
{
  "[ProposalDurationInHours](#cfn-managedblockchain-member-approvalthresholdpolicy-proposaldurationinhours)" : Integer,
  "[ThresholdComparator](#cfn-managedblockchain-member-approvalthresholdpolicy-thresholdcomparator)" : String,
  "[ThresholdPercentage](#cfn-managedblockchain-member-approvalthresholdpolicy-thresholdpercentage)" : Integer
}
```

### YAML<a name="aws-properties-managedblockchain-member-approvalthresholdpolicy-syntax.yaml"></a>

```
  [ProposalDurationInHours](#cfn-managedblockchain-member-approvalthresholdpolicy-proposaldurationinhours): Integer
  [ThresholdComparator](#cfn-managedblockchain-member-approvalthresholdpolicy-thresholdcomparator): String
  [ThresholdPercentage](#cfn-managedblockchain-member-approvalthresholdpolicy-thresholdpercentage): Integer
```

## Properties<a name="aws-properties-managedblockchain-member-approvalthresholdpolicy-properties"></a>

`ProposalDurationInHours`  <a name="cfn-managedblockchain-member-approvalthresholdpolicy-proposaldurationinhours"></a>
The duration from the time that a proposal is created until it expires\. If members cast neither the required number of `YES` votes to approve the proposal nor the number of `NO` votes required to reject it before the duration expires, the proposal is `EXPIRED` and `ProposalActions` are not carried out\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `168`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThresholdComparator`  <a name="cfn-managedblockchain-member-approvalthresholdpolicy-thresholdcomparator"></a>
Determines whether the vote percentage must be greater than the `ThresholdPercentage` or must be greater than or equal to the `ThreholdPercentage` to be approved\.  
*Required*: No  
*Type*: String  
*Allowed values*: `GREATER_THAN | GREATER_THAN_OR_EQUAL_TO`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ThresholdPercentage`  <a name="cfn-managedblockchain-member-approvalthresholdpolicy-thresholdpercentage"></a>
The percentage of votes among all members that must be `YES` for a proposal to be approved\. For example, a `ThresholdPercentage` value of `50` indicates 50%\. The `ThresholdComparator` determines the precise comparison\. If a `ThresholdPercentage` value of `50` is specified on a network with 10 members, along with a `ThresholdComparator` value of `GREATER_THAN`, this indicates that 6 `YES` votes are required for the proposal to be approved\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)