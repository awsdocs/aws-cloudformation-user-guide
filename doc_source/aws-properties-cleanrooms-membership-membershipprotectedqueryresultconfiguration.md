# AWS::CleanRooms::Membership MembershipProtectedQueryResultConfiguration<a name="aws-properties-cleanrooms-membership-membershipprotectedqueryresultconfiguration"></a>

Contains configurations for protected query results\.

## Syntax<a name="aws-properties-cleanrooms-membership-membershipprotectedqueryresultconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-membership-membershipprotectedqueryresultconfiguration-syntax.json"></a>

```
{
  "[OutputConfiguration](#cfn-cleanrooms-membership-membershipprotectedqueryresultconfiguration-outputconfiguration)" : MembershipProtectedQueryOutputConfiguration,
  "[RoleArn](#cfn-cleanrooms-membership-membershipprotectedqueryresultconfiguration-rolearn)" : String
}
```

### YAML<a name="aws-properties-cleanrooms-membership-membershipprotectedqueryresultconfiguration-syntax.yaml"></a>

```
  [OutputConfiguration](#cfn-cleanrooms-membership-membershipprotectedqueryresultconfiguration-outputconfiguration): 
    MembershipProtectedQueryOutputConfiguration
  [RoleArn](#cfn-cleanrooms-membership-membershipprotectedqueryresultconfiguration-rolearn): String
```

## Properties<a name="aws-properties-cleanrooms-membership-membershipprotectedqueryresultconfiguration-properties"></a>

`OutputConfiguration`  <a name="cfn-cleanrooms-membership-membershipprotectedqueryresultconfiguration-outputconfiguration"></a>
Configuration for protected query results\.  
*Required*: Yes  
*Type*: [MembershipProtectedQueryOutputConfiguration](aws-properties-cleanrooms-membership-membershipprotectedqueryoutputconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-cleanrooms-membership-membershipprotectedqueryresultconfiguration-rolearn"></a>
The unique ARN for an IAM role that is used by AWS Clean Rooms to write protected query results to the result location, given by the member who can receive results\.  
*Required*: No  
*Type*: String  
*Minimum*: `32`  
*Maximum*: `512`  
*Pattern*: `arn:aws:iam::[\w]+:role/[\w+=,./@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)