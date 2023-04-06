# AWS::RolesAnywhere::Profile<a name="aws-resource-rolesanywhere-profile"></a>

 Creates a Profile\. 

## Syntax<a name="aws-resource-rolesanywhere-profile-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rolesanywhere-profile-syntax.json"></a>

```
{
  "Type" : "AWS::RolesAnywhere::Profile",
  "Properties" : {
      "[DurationSeconds](#cfn-rolesanywhere-profile-durationseconds)" : Double,
      "[Enabled](#cfn-rolesanywhere-profile-enabled)" : Boolean,
      "[ManagedPolicyArns](#cfn-rolesanywhere-profile-managedpolicyarns)" : [ String, ... ],
      "[Name](#cfn-rolesanywhere-profile-name)" : String,
      "[RequireInstanceProperties](#cfn-rolesanywhere-profile-requireinstanceproperties)" : Boolean,
      "[RoleArns](#cfn-rolesanywhere-profile-rolearns)" : [ String, ... ],
      "[SessionPolicy](#cfn-rolesanywhere-profile-sessionpolicy)" : String,
      "[Tags](#cfn-rolesanywhere-profile-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-rolesanywhere-profile-syntax.yaml"></a>

```
Type: AWS::RolesAnywhere::Profile
Properties: 
  [DurationSeconds](#cfn-rolesanywhere-profile-durationseconds): Double
  [Enabled](#cfn-rolesanywhere-profile-enabled): Boolean
  [ManagedPolicyArns](#cfn-rolesanywhere-profile-managedpolicyarns): 
    - String
  [Name](#cfn-rolesanywhere-profile-name): String
  [RequireInstanceProperties](#cfn-rolesanywhere-profile-requireinstanceproperties): Boolean
  [RoleArns](#cfn-rolesanywhere-profile-rolearns): 
    - String
  [SessionPolicy](#cfn-rolesanywhere-profile-sessionpolicy): String
  [Tags](#cfn-rolesanywhere-profile-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-rolesanywhere-profile-properties"></a>

`DurationSeconds`  <a name="cfn-rolesanywhere-profile-durationseconds"></a>
 The number of seconds vended session credentials will be valid for   
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-rolesanywhere-profile-enabled"></a>
 The enabled status of the resource\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedPolicyArns`  <a name="cfn-rolesanywhere-profile-managedpolicyarns"></a>
 A list of managed policy ARNs\. Managed policies identified by this list will be applied to the vended session credentials\.   
*Required*: No  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-rolesanywhere-profile-name"></a>
 The customer specified name of the resource\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[ a-zA-Z0-9-_]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireInstanceProperties`  <a name="cfn-rolesanywhere-profile-requireinstanceproperties"></a>
 Specifies whether instance properties are required in CreateSession requests with this profile\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArns`  <a name="cfn-rolesanywhere-profile-rolearns"></a>
 A list of IAM role ARNs that can be assumed when this profile is specified in a CreateSession request\.   
*Required*: Yes  
*Type*: List of String  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SessionPolicy`  <a name="cfn-rolesanywhere-profile-sessionpolicy"></a>
 A session policy that will applied to the trust boundary of the vended session credentials\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rolesanywhere-profile-tags"></a>
 A list of Tags\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rolesanywhere-profile-return-values"></a>

### Ref<a name="aws-resource-rolesanywhere-profile-return-values-ref"></a>

 The name of the Profile

### Fn::GetAtt<a name="aws-resource-rolesanywhere-profile-return-values-fn--getatt"></a>

 

#### <a name="aws-resource-rolesanywhere-profile-return-values-fn--getatt-fn--getatt"></a>

`ProfileArn`  <a name="ProfileArn-fn::getatt"></a>
The ARN of the profile\.

`ProfileId`  <a name="ProfileId-fn::getatt"></a>
 The unique primary identifier of the Profile 