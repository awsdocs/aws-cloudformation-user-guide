# AWS::ManagedBlockchain::Member VotingPolicy<a name="aws-properties-managedblockchain-member-votingpolicy"></a>

 The voting rules for the network to decide if a proposal is accepted 

Applies only to Hyperledger Fabric\.

## Syntax<a name="aws-properties-managedblockchain-member-votingpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-managedblockchain-member-votingpolicy-syntax.json"></a>

```
{
  "[ApprovalThresholdPolicy](#cfn-managedblockchain-member-votingpolicy-approvalthresholdpolicy)" : ApprovalThresholdPolicy
}
```

### YAML<a name="aws-properties-managedblockchain-member-votingpolicy-syntax.yaml"></a>

```
  [ApprovalThresholdPolicy](#cfn-managedblockchain-member-votingpolicy-approvalthresholdpolicy): 
    ApprovalThresholdPolicy
```

## Properties<a name="aws-properties-managedblockchain-member-votingpolicy-properties"></a>

`ApprovalThresholdPolicy`  <a name="cfn-managedblockchain-member-votingpolicy-approvalthresholdpolicy"></a>
Defines the rules for the network for voting on proposals, such as the percentage of `YES` votes required for the proposal to be approved and the duration of the proposal\. The policy applies to all proposals and is specified when the network is created\.  
*Required*: No  
*Type*: [ApprovalThresholdPolicy](aws-properties-managedblockchain-member-approvalthresholdpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)