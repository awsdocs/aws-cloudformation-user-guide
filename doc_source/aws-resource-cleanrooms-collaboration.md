# AWS::CleanRooms::Collaboration<a name="aws-resource-cleanrooms-collaboration"></a>

Creates a new collaboration\.

## Syntax<a name="aws-resource-cleanrooms-collaboration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cleanrooms-collaboration-syntax.json"></a>

```
{
  "Type" : "AWS::CleanRooms::Collaboration",
  "Properties" : {
      "[CreatorDisplayName](#cfn-cleanrooms-collaboration-creatordisplayname)" : String,
      "[CreatorMemberAbilities](#cfn-cleanrooms-collaboration-creatormemberabilities)" : [ String, ... ],
      "[DataEncryptionMetadata](#cfn-cleanrooms-collaboration-dataencryptionmetadata)" : DataEncryptionMetadata,
      "[Description](#cfn-cleanrooms-collaboration-description)" : String,
      "[Members](#cfn-cleanrooms-collaboration-members)" : [ MemberSpecification, ... ],
      "[Name](#cfn-cleanrooms-collaboration-name)" : String,
      "[QueryLogStatus](#cfn-cleanrooms-collaboration-querylogstatus)" : String,
      "[Tags](#cfn-cleanrooms-collaboration-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cleanrooms-collaboration-syntax.yaml"></a>

```
Type: AWS::CleanRooms::Collaboration
Properties: 
  [CreatorDisplayName](#cfn-cleanrooms-collaboration-creatordisplayname): String
  [CreatorMemberAbilities](#cfn-cleanrooms-collaboration-creatormemberabilities): 
    - String
  [DataEncryptionMetadata](#cfn-cleanrooms-collaboration-dataencryptionmetadata): 
    DataEncryptionMetadata
  [Description](#cfn-cleanrooms-collaboration-description): String
  [Members](#cfn-cleanrooms-collaboration-members): 
    - MemberSpecification
  [Name](#cfn-cleanrooms-collaboration-name): String
  [QueryLogStatus](#cfn-cleanrooms-collaboration-querylogstatus): String
  [Tags](#cfn-cleanrooms-collaboration-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cleanrooms-collaboration-properties"></a>

`CreatorDisplayName`  <a name="cfn-cleanrooms-collaboration-creatordisplayname"></a>
A display name of the collaboration creator\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `(?!\s*$)[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDBFF-\uDC00\uDFFF\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CreatorMemberAbilities`  <a name="cfn-cleanrooms-collaboration-creatormemberabilities"></a>
The abilities granted to the collaboration creator\.  
*Allowed values* `CAN_QUERY` \| `CAN_RECEIVE_RESULTS`  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DataEncryptionMetadata`  <a name="cfn-cleanrooms-collaboration-dataencryptionmetadata"></a>
The settings for client\-side encryption for cryptographic computing\.  
*Required*: No  
*Type*: [DataEncryptionMetadata](aws-properties-cleanrooms-collaboration-dataencryptionmetadata.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-cleanrooms-collaboration-description"></a>
A description of the collaboration provided by the collaboration owner\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `(?!\s*$)[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDBFF-\uDC00\uDFFF\t\r\n]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Members`  <a name="cfn-cleanrooms-collaboration-members"></a>
A list of initial members, not including the creator\. This list is immutable\.  
*Required*: Yes  
*Type*: List of [MemberSpecification](aws-properties-cleanrooms-collaboration-memberspecification.md)  
*Maximum*: `9`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-cleanrooms-collaboration-name"></a>
A human\-readable identifier provided by the collaboration owner\. Display names are not unique\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `(?!\s*$)[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDBFF-\uDC00\uDFFF\t]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`QueryLogStatus`  <a name="cfn-cleanrooms-collaboration-querylogstatus"></a>
An indicator as to whether query logging has been enabled or disabled for the collaboration\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-cleanrooms-collaboration-tags"></a>
An optional label that you can assign to a resource when you create it\. Each tag consists of a key and an optional value, both of which you define\. When you use tagging, you can also use tag\-based access control in IAM policies to control access to this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cleanrooms-collaboration-return-values"></a>

### Ref<a name="aws-resource-cleanrooms-collaboration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the `CollaborationIdentifier`, such as `a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`\. For example: 

`{ "Ref": "MyCollaboration" }`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cleanrooms-collaboration-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cleanrooms-collaboration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the specified collaboration\.  
Example: `arn:aws:cleanrooms:us-east-1:111122223333:collaboration/a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`

`CollaborationIdentifier`  <a name="CollaborationIdentifier-fn::getatt"></a>
Returns the unique identifier of the specified collaboration\.  
Example: `a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`

## Examples<a name="aws-resource-cleanrooms-collaboration--examples"></a>



### Create a collaboration<a name="aws-resource-cleanrooms-collaboration--examples--Create_a_collaboration"></a>

The following example creates a collaboration with the collaboration creator\.

#### JSON<a name="aws-resource-cleanrooms-collaboration--examples--Create_a_collaboration--json"></a>

```
"ExampleCollaboration": {
  {
    "Type": "AWS::CleanRooms::Collaboration",
    "Properties": {
      "Name": "Example Collaboration",
      "Description": "Example AWS Clean Rooms collaboration",
      "CreatorDisplayName": "Member 1",
      "CreatorMemberAbilities": ["CAN_QUERY", "CAN_RECEIVE_RESULTS"],
      "Members": [
        {
          "AccountId": "111122223333",
          "DisplayName": "Member 2",
          "MemberAbilities": []
        },
        {
          "AccountId": "444455556666",
          "DisplayName": "Member 3",
          "MemberAbilities": []
        }
      ],
      "QueryLogStatus": "ENABLED"
    }
  }
}
```

#### YAML<a name="aws-resource-cleanrooms-collaboration--examples--Create_a_collaboration--yaml"></a>

```
ExampleCollaboration:
  Type: AWS::CleanRooms::Collaboration
  Properties:
    Name: Example Collaboration
    Description: Example AWS Clean Rooms collaboration
    CreatorDisplayName: Member 1
    CreatorMemberAbilities:
      - CAN_QUERY
      - CAN_RECEIVE_RESULTS
    Members:
      - AccountId: 111122223333
        DisplayName: Member 2
        MemberAbilities: []
      - AccountId: 444455556666
        DisplayName: Member 3
        MemberAbilities: []
    QueryLogStatus: ENABLED
```