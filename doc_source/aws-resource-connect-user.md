# AWS::Connect::User<a name="aws-resource-connect-user"></a>

Specifies a user account for an Amazon Connect instance\.

For information about how to create user accounts using the Amazon Connect console, see [Add Users](https://docs.aws.amazon.com/connect/latest/adminguide/user-management.html) in the *Amazon Connect Administrator Guide*\.

## Syntax<a name="aws-resource-connect-user-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-connect-user-syntax.json"></a>

```
{
  "Type" : "AWS::Connect::User",
  "Properties" : {
      "[DirectoryUserId](#cfn-connect-user-directoryuserid)" : String,
      "[HierarchyGroupArn](#cfn-connect-user-hierarchygrouparn)" : String,
      "[IdentityInfo](#cfn-connect-user-identityinfo)" : UserIdentityInfo,
      "[InstanceArn](#cfn-connect-user-instancearn)" : String,
      "[Password](#cfn-connect-user-password)" : String,
      "[PhoneConfig](#cfn-connect-user-phoneconfig)" : UserPhoneConfig,
      "[RoutingProfileArn](#cfn-connect-user-routingprofilearn)" : String,
      "[SecurityProfileArns](#cfn-connect-user-securityprofilearns)" : [ String, ... ],
      "[Tags](#cfn-connect-user-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Username](#cfn-connect-user-username)" : String
    }
}
```

### YAML<a name="aws-resource-connect-user-syntax.yaml"></a>

```
Type: AWS::Connect::User
Properties: 
  [DirectoryUserId](#cfn-connect-user-directoryuserid): String
  [HierarchyGroupArn](#cfn-connect-user-hierarchygrouparn): String
  [IdentityInfo](#cfn-connect-user-identityinfo): 
    UserIdentityInfo
  [InstanceArn](#cfn-connect-user-instancearn): String
  [Password](#cfn-connect-user-password): String
  [PhoneConfig](#cfn-connect-user-phoneconfig): 
    UserPhoneConfig
  [RoutingProfileArn](#cfn-connect-user-routingprofilearn): String
  [SecurityProfileArns](#cfn-connect-user-securityprofilearns): 
    - String
  [Tags](#cfn-connect-user-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Username](#cfn-connect-user-username): String
```

## Properties<a name="aws-resource-connect-user-properties"></a>

`DirectoryUserId`  <a name="cfn-connect-user-directoryuserid"></a>
The identifier of the user account in the directory used for identity management\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HierarchyGroupArn`  <a name="cfn-connect-user-hierarchygrouparn"></a>
The Amazon Resource Name \(ARN\) of the user's hierarchy group\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityInfo`  <a name="cfn-connect-user-identityinfo"></a>
Information about the user identity\.  
*Required*: No  
*Type*: [UserIdentityInfo](aws-properties-connect-user-useridentityinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceArn`  <a name="cfn-connect-user-instancearn"></a>
The Amazon Resource Name \(ARN\) of the instance\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-connect-user-password"></a>
The user's password\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PhoneConfig`  <a name="cfn-connect-user-phoneconfig"></a>
Information about the phone configuration for the user\.  
*Required*: Yes  
*Type*: [UserPhoneConfig](aws-properties-connect-user-userphoneconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoutingProfileArn`  <a name="cfn-connect-user-routingprofilearn"></a>
The Amazon Resource Name \(ARN\) of the user's routing profile\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityProfileArns`  <a name="cfn-connect-user-securityprofilearns"></a>
The Amazon Resource Name \(ARN\) of the user's security profile\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-connect-user-tags"></a>
The tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-connect-user-username"></a>
The user name assigned to the user account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-connect-user-return-values"></a>

### Ref<a name="aws-resource-connect-user-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the user\. For example:

`{ "Ref": "myUser" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-connect-user-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-connect-user-return-values-fn--getatt-fn--getatt"></a>

`UserArn`  <a name="UserArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the user\.

## Examples<a name="aws-resource-connect-user--examples"></a>



### Specify a user resource<a name="aws-resource-connect-user--examples--Specify_a_user_resource"></a>

The following example specifies a user resource for an Amazon Connect instance\. This example specifies a user under an Amazon Connect instance\. We recommend using a [dynamic reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/security-best-practices.html#creds) to specify a password value or mask the parameter with `NoEcho`\.

#### YAML<a name="aws-resource-connect-user--examples--Specify_a_user_resource--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a user for an Amazon Connect instance
Resources:
    User:
      Type: 'AWS::Connect::User'
      Properties:
        IdentityInfo:
          FirstName: 'firstname'
          LastName: 'lastname'
          Email: 'example@email.com'
        PhoneConfig:
          PhoneType: 'DESK_PHONE'
          AutoAccept: true
          DeskPhoneNumber: '+12345678902'
          AfterContactWorkTimeLimit: 10
        Username: 'exampleuser'
        InstanceArn: 'arn:aws:connect:region-name:aws-account-id:instance/instance-arn'
        RoutingProfileArn: 'arn:aws:connect:region-name:aws-account-id:instance/instance-arn/routing-profile/routing-arn'
        SecurityProfileArns: [arn:aws:connect:region-name:aws-account-id:instance/instance-arn/security-profile/security-arn]
        Password: !Ref password
        Tags:
          - Key: 'tagKey'
            Value: 'tagValue'
```