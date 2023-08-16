# Account level targets for service\-managed Stack Sets<a name="account-level-targets"></a>

The `AccountFilterType` allows you to limit deployment targets to individual accounts or include additional accounts with provided AWS Organizations units \(OUs\) with your Create, Update, or Delete operations\.

Service\-managed Stack Sets, can deploy to individual accounts with the accounts parameter, to all the accounts in specified OU, or a subset of accounts in the specified OU\. For more information about deployment targets, see [https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DeploymentTargets.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DeploymentTargets.html) in the AWS CLI Command Reference\.

```
{
  "Accounts": ["string", ...],
  "AccountsUrl": "string", 
  "OrganizationalUnitIds": ["string", ...] 
  "AccountFilterType": "string"
}
```

`Accounts`  <a name="accounts"></a>
The names of one or more AWS accounts for which you want to deploy a StackSets updates to\.

`AccountsUrl`  <a name="accountsurl"></a>
An Amazon S3 URL for a list of accounts\.

`OrganizationalUnitIds`  <a name="org.unit"></a>
The organization root ID or organizational unit \(OU\) IDs to which StackSets deploys to\.

`AccountFilterType`  <a name="accountfiltertype"></a>
*Valid values*: `INTERSECTION` \| `DIFFERENCE` \| `UNION`  
The following is a list of possible values for the `AccountFilterType` operation\.  
+ `INTERSECTION`: StackSets deploys to the accounts specified in `Accounts` parameter\.
+ `DIFFERENCE`: StackSets excludes the accounts specified in `Accounts` parameter\. This enables user to avoid certain accounts within an OU such as suspended accounts\.
+ `UNION`: \(default value\) StackSets includes additional accounts deployment targets\.

  The default value if `AccountFilterType` isn't provided\. This enables user to update an entire OU and individual accounts from a different OU in one request, which used to be two separate requests\.
+ `NONE`: Deploys to all the accounts in specified organizational units \(OU\)\.

## AWS CLI examples<a name="account-level-cli-examples"></a>

The following examples show how to use `AccountFilterType` in the AWS CLI\.

### Target individual accounts within an OU<a name="target-accounts-within-ou"></a>

The following example filters the deployment targets in the OU\. In this example, A1, A2, and A3 accounts are all in the OU1 Organization\. The AWS CLI command deploys to the A1 and A2 target accounts\.

![\[Target individual accounts within an OU.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/target-accounts-within-ou.png)

```
aws cloudformation create-stack-instances --deployment-targets OrganizationalUnitIds=OU1,Accounts=A1,A2,AccountFilterType=INTERSECTION
```

*Results*: You've created stack instances for accounts 1 and 2\.

### Target an OU and filter individual accounts<a name="target-ou-except-account"></a>

The following example creates a stack instance in all accounts in the OU besides account 1 and 2\.

![\[Target individual accounts within an OU.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/target-ou-except-account.png)

```
aws cloudformation create-stack-instances --deployment-targets OrganizationalUnitIds=OU1,Accounts=A1,A2,AccountFilterType=DIFFERENCE
```

*Results*: You avoided deploying to specific accounts in your OU\.

### Target an OU and an additional individual account<a name="target-out-with-account"></a>

The following example updates stack instances\.

![\[Target individual accounts within an OU.\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/images/target-out-with-account.png)

```
aws cloudformation update-stack-instances --deployment-targets OrganizationalUnitIds=OU1,Accounts=A4,AccountFilterType=UNION
```

*Results*: You updated stack instances for accounts 1, 2, and 4 in your OU\. By filtering accounts, you didn't update stack instances on account A5\.