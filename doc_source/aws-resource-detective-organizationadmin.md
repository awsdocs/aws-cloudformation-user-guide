# AWS::Detective::OrganizationAdmin<a name="aws-resource-detective-organizationadmin"></a>

The `AWS::Detective::OrganizationAdmin` resource is an Amazon Detective resource type that designates the Detective administrator account for the organization in the current region\. If the account does not have Detective enabled, then this resource enables Detective for that account and creates a new behavior graph\.

The `AWS::Detective::OrganizationAdmin` resource is currently not available in AWS GovCloud \(US\) PDT/OSU Regions\.

## Syntax<a name="aws-resource-detective-organizationadmin-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-detective-organizationadmin-syntax.json"></a>

```
{
  "Type" : "AWS::Detective::OrganizationAdmin",
  "Properties" : {
      "[AccountId](#cfn-detective-organizationadmin-accountid)" : String
    }
}
```

### YAML<a name="aws-resource-detective-organizationadmin-syntax.yaml"></a>

```
Type: AWS::Detective::OrganizationAdmin
Properties: 
  [AccountId](#cfn-detective-organizationadmin-accountid): String
```

## Properties<a name="aws-resource-detective-organizationadmin-properties"></a>

`AccountId`  <a name="cfn-detective-organizationadmin-accountid"></a>
The AWS account identifier of the account to designate as the Detective administrator account for the organization\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-detective-organizationadmin-return-values"></a>

### Ref<a name="aws-resource-detective-organizationadmin-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ARN of the behavior graph and the member account identifier, separated by a pipe character \('\|'\)\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-detective-organizationadmin-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-detective-organizationadmin-return-values-fn--getatt-fn--getatt"></a>

`GraphArn`  <a name="GraphArn-fn::getatt"></a>
The ARN of the behavior graph to invite the account to contribute data to\.

## Examples<a name="aws-resource-detective-organizationadmin--examples"></a>

### Designating a Detective administrator account for the organization in the current region<a name="aws-resource-detective-organizationadmin--examples--Designating_a__administrator_account_for_the_organization_in_the_current_region"></a>

This example shows how to declare a new `AWS::Detective::OrganizationAdmin` resource to designate a Detective administrator account for the organization in the current region\.

#### JSON<a name="aws-resource-detective-organizationadmin--examples--Designating_a__administrator_account_for_the_organization_in_the_current_region--json"></a>

```
"OrganizationAdmin": {
    "Type": "AWS::Detective::OrganizationAdmin",
    "Properties": {
        "AccountId" : "123456789101"
     }
}
```

#### YAML<a name="aws-resource-detective-organizationadmin--examples--Designating_a__administrator_account_for_the_organization_in_the_current_region--yaml"></a>

```
OrganizationAdmin:
    Type: AWS::Detective::OrganizationAdmin
    Properties:
      AccountId: 123456789101
```