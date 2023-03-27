# AWS::Organizations::OrganizationalUnit<a name="aws-resource-organizations-organizationalunit"></a>

Creates an organizational unit \(OU\) within a root or parent OU\. An OU is a container for accounts that enables you to organize your accounts to apply policies according to your business requirements\. The number of levels deep that you can nest OUs is dependent upon the policy types enabled for that root\. For service control policies, the limit is five\.

For more information about OUs, see [Managing Organizational Units](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_ous.html) in the * AWS Organizations User Guide\.* 

If the request includes tags, then the requester must have the `organizations:TagResource` permission\.

This operation can be called only from the organization's management account\.

## Syntax<a name="aws-resource-organizations-organizationalunit-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-organizations-organizationalunit-syntax.json"></a>

```
{
  "Type" : "AWS::Organizations::OrganizationalUnit",
  "Properties" : {
      "[Name](#cfn-organizations-organizationalunit-name)" : String,
      "[ParentId](#cfn-organizations-organizationalunit-parentid)" : String,
      "[Tags](#cfn-organizations-organizationalunit-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-organizations-organizationalunit-syntax.yaml"></a>

```
Type: AWS::Organizations::OrganizationalUnit
Properties: 
  [Name](#cfn-organizations-organizationalunit-name): String
  [ParentId](#cfn-organizations-organizationalunit-parentid): String
  [Tags](#cfn-organizations-organizationalunit-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-organizations-organizationalunit-properties"></a>

`Name`  <a name="cfn-organizations-organizationalunit-name"></a>
The friendly name of this OU\.  
The [regex pattern](http://wikipedia.org/wiki/regex) that is used to validate this parameter is a string of any of the characters in the ASCII character range\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\s\S]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParentId`  <a name="cfn-organizations-organizationalunit-parentid"></a>
The unique identifier \(ID\) of the parent root or OU that you want to create the new OU in\.  
To update the `ParentId` parameter value, you must first remove all accounts attached to the organizational unit \(OU\)\. OUs can't be moved within the organization with accounts still attached\.
The [regex pattern](http://wikipedia.org/wiki/regex) for a parent ID string requires one of the following:  
+  **Root** \- A string that begins with "r\-" followed by from 4 to 32 lowercase letters or digits\.
+  **Organizational unit \(OU\)** \- A string that begins with "ou\-" followed by from 4 to 32 lowercase letters or digits \(the ID of the root that the OU is in\)\. This string is followed by a second "\-" dash and from 8 to 32 additional lowercase letters or digits\.
*Required*: Yes  
*Type*: String  
*Maximum*: `100`  
*Pattern*: `^(r-[0-9a-z]{4,32})|(ou-[0-9a-z]{4,32}-[a-z0-9]{8,32})$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-organizations-organizationalunit-tags"></a>
A list of tags that you want to attach to the newly created OU\. For each tag in the list, you must specify both a tag key and a value\. You can set the value to an empty string, but you can't set it to `null`\. For more information about tagging, see [Tagging AWS Organizations resources](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_tagging.html) in the AWS Organizations User Guide\.  
If any one of the tags is not valid or if you exceed the allowed number of tags for an OU, then the entire request fails and the OU is not created\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-organizations-organizationalunit-return-values"></a>

### Ref<a name="aws-resource-organizations-organizationalunit-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `Id`\. For example: `ou-examplerootid111-exampleouid111`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-organizations-organizationalunit-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-organizations-organizationalunit-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of this OU\. For example: `arn:aws:organizations::111111111111:ou/o-exampleorgid/ou-examplerootid111-exampleouid111`\.

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier \(ID\) associated with this OU\. For example: `ou-examplerootid111-exampleouid111`\.