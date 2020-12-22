# AWS::IoTSiteWise::AccessPolicy AccessPolicyIdentity<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyidentity"></a>

The identity \(AWS SSO user, AWS SSO group, or IAM user\) to which this access policy applies\.

## Syntax<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyidentity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyidentity-syntax.json"></a>

```
{
  "[User](#cfn-iotsitewise-accesspolicy-accesspolicyidentity-user)" : User
}
```

### YAML<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyidentity-syntax.yaml"></a>

```
  [User](#cfn-iotsitewise-accesspolicy-accesspolicyidentity-user): 
    User
```

## Properties<a name="aws-properties-iotsitewise-accesspolicy-accesspolicyidentity-properties"></a>

`User`  <a name="cfn-iotsitewise-accesspolicy-accesspolicyidentity-user"></a>
The AWS SSO user to which this access policy maps\.  
*Required*: No  
*Type*: [User](aws-properties-iotsitewise-accesspolicy-user.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)