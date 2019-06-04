# AWS::AmazonMQ::Broker User<a name="aws-properties-amazonmq-broker-user"></a>

The list of ActiveMQ users \(persons or applications\) who can access queues and topics\. This value can contain only alphanumeric characters, dashes, periods, underscores, and tildes \(\- \. \_ \~\)\. This value must be 2\-100 characters long\.

## Syntax<a name="aws-properties-amazonmq-broker-user-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-amazonmq-broker-user-syntax.json"></a>

```
{
  "[ConsoleAccess](#cfn-amazonmq-broker-user-consoleaccess)" : Boolean,
  "[Groups](#cfn-amazonmq-broker-user-groups)" : [ String, ... ],
  "[Password](#cfn-amazonmq-broker-user-password)" : String,
  "[Username](#cfn-amazonmq-broker-user-username)" : String
}
```

### YAML<a name="aws-properties-amazonmq-broker-user-syntax.yaml"></a>

```
  [ConsoleAccess](#cfn-amazonmq-broker-user-consoleaccess): Boolean
  [Groups](#cfn-amazonmq-broker-user-groups): 
    - String
  [Password](#cfn-amazonmq-broker-user-password): String
  [Username](#cfn-amazonmq-broker-user-username): String
```

## Properties<a name="aws-properties-amazonmq-broker-user-properties"></a>

`ConsoleAccess`  <a name="cfn-amazonmq-broker-user-consoleaccess"></a>
Enables access to the the ActiveMQ Web Console for the ActiveMQ user\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Groups`  <a name="cfn-amazonmq-broker-user-groups"></a>
The list of groups \(20 maximum\) to which the ActiveMQ user belongs\. This value can contain only alphanumeric characters, dashes, periods, underscores, and tildes \(\- \. \_ \~\)\. This value must be 2\-100 characters long\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-amazonmq-broker-user-password"></a>
The password of the ActiveMQ user\. This value must be at least 12 characters long, must contain at least 4 unique characters, and must not contain commas\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-amazonmq-broker-user-username"></a>
The username of the ActiveMQ user\. This value can contain only alphanumeric characters, dashes, periods, underscores, and tildes \(\- \. \_ \~\)\. This value must be 2\-100 characters long\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)