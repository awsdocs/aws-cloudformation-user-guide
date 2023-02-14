# AWS::SES::ContactList Topic<a name="aws-properties-ses-contactlist-topic"></a>

An interest group, theme, or label within a list\. Lists can have multiple topics\.

## Syntax<a name="aws-properties-ses-contactlist-topic-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ses-contactlist-topic-syntax.json"></a>

```
{
  "[DefaultSubscriptionStatus](#cfn-ses-contactlist-topic-defaultsubscriptionstatus)" : String,
  "[Description](#cfn-ses-contactlist-topic-description)" : String,
  "[DisplayName](#cfn-ses-contactlist-topic-displayname)" : String,
  "[TopicName](#cfn-ses-contactlist-topic-topicname)" : String
}
```

### YAML<a name="aws-properties-ses-contactlist-topic-syntax.yaml"></a>

```
  [DefaultSubscriptionStatus](#cfn-ses-contactlist-topic-defaultsubscriptionstatus): String
  [Description](#cfn-ses-contactlist-topic-description): String
  [DisplayName](#cfn-ses-contactlist-topic-displayname): String
  [TopicName](#cfn-ses-contactlist-topic-topicname): String
```

## Properties<a name="aws-properties-ses-contactlist-topic-properties"></a>

`DefaultSubscriptionStatus`  <a name="cfn-ses-contactlist-topic-defaultsubscriptionstatus"></a>
The default subscription status to be applied to a contact if the contact has not noted their preference for subscribing to a topic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ses-contactlist-topic-description"></a>
A description of what the topic is about, which the contact will see\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-ses-contactlist-topic-displayname"></a>
The name of the topic the contact will see\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TopicName`  <a name="cfn-ses-contactlist-topic-topicname"></a>
The name of the topic\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)