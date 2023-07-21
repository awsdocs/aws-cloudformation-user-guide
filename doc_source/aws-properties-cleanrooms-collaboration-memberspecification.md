# AWS::CleanRooms::Collaboration MemberSpecification<a name="aws-properties-cleanrooms-collaboration-memberspecification"></a>

Basic metadata used to construct a new member\.

## Syntax<a name="aws-properties-cleanrooms-collaboration-memberspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-collaboration-memberspecification-syntax.json"></a>

```
{
  "[AccountId](#cfn-cleanrooms-collaboration-memberspecification-accountid)" : String,
  "[DisplayName](#cfn-cleanrooms-collaboration-memberspecification-displayname)" : String,
  "[MemberAbilities](#cfn-cleanrooms-collaboration-memberspecification-memberabilities)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cleanrooms-collaboration-memberspecification-syntax.yaml"></a>

```
  [AccountId](#cfn-cleanrooms-collaboration-memberspecification-accountid): String
  [DisplayName](#cfn-cleanrooms-collaboration-memberspecification-displayname): String
  [MemberAbilities](#cfn-cleanrooms-collaboration-memberspecification-memberabilities): 
    - String
```

## Properties<a name="aws-properties-cleanrooms-collaboration-memberspecification-properties"></a>

`AccountId`  <a name="cfn-cleanrooms-collaboration-memberspecification-accountid"></a>
The identifier used to reference members of the collaboration\. Currently only supports AWS account ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `12`  
*Maximum*: `12`  
*Pattern*: `\d+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DisplayName`  <a name="cfn-cleanrooms-collaboration-memberspecification-displayname"></a>
The member's display name\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `(?!\s*$)[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDBFF-\uDC00\uDFFF\t]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MemberAbilities`  <a name="cfn-cleanrooms-collaboration-memberspecification-memberabilities"></a>
The abilities granted to the collaboration member\.  
*Allowed Values*: `CAN_QUERY` \| `CAN_RECEIVE_RESULTS`  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)