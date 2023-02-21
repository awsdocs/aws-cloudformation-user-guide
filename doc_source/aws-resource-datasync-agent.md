# AWS::DataSync::Agent<a name="aws-resource-datasync-agent"></a>

The `AWS::DataSync::Agent` resource specifies an AWS DataSync agent to be deployed and activated on your host\. The activation process associates your agent with your account\. In the activation process, you specify information such as the AWS Region that you want to activate the agent in\. You activate the agent in the AWS Region where your target locations \(in Amazon S3, Amazon EFS, or Amazon FSx for Windows File Server\) reside\. Your tasks are created in this AWS Region\.

You can activate the agent in a virtual private cloud \(VPC\) or provide the agent access to a VPC endpoint so that you can run tasks without sending them over the public internet\.

You can specify an agent to be used for more than one location\. If a task uses multiple agents, all of them must have a status of AVAILABLE for the task to run\. If you use multiple agents for a source location, the status of all the agents must be AVAILABLE for the task to run\. 

For more information, see [Activating an Agent](https://docs.aws.amazon.com/datasync/latest/userguide/activating-agent.html) in the *AWS DataSync User Guide*\.

Agents are automatically updated by AWS on a regular basis, using a mechanism that ensures minimal interruption to your tasks\.



## Syntax<a name="aws-resource-datasync-agent-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-datasync-agent-syntax.json"></a>

```
{
  "Type" : "AWS::DataSync::Agent",
  "Properties" : {
      "[ActivationKey](#cfn-datasync-agent-activationkey)" : String,
      "[AgentName](#cfn-datasync-agent-agentname)" : String,
      "[SecurityGroupArns](#cfn-datasync-agent-securitygrouparns)" : [ String, ... ],
      "[SubnetArns](#cfn-datasync-agent-subnetarns)" : [ String, ... ],
      "[Tags](#cfn-datasync-agent-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcEndpointId](#cfn-datasync-agent-vpcendpointid)" : String
    }
}
```

### YAML<a name="aws-resource-datasync-agent-syntax.yaml"></a>

```
Type: AWS::DataSync::Agent
Properties: 
  [ActivationKey](#cfn-datasync-agent-activationkey): String
  [AgentName](#cfn-datasync-agent-agentname): String
  [SecurityGroupArns](#cfn-datasync-agent-securitygrouparns): 
    - String
  [SubnetArns](#cfn-datasync-agent-subnetarns): 
    - String
  [Tags](#cfn-datasync-agent-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcEndpointId](#cfn-datasync-agent-vpcendpointid): String
```

## Properties<a name="aws-resource-datasync-agent-properties"></a>

`ActivationKey`  <a name="cfn-datasync-agent-activationkey"></a>
Your agent activation key\. You can get the activation key either by sending an HTTP GET request with redirects that enable you to get the agent IP address \(port 80\)\. Alternatively, you can get it from the DataSync console\.  
The redirect URL returned in the response provides you the activation key for your agent in the query string parameter `activationKey`\. It might also include other activation\-related parameters; however, these are merely defaults\. The arguments you pass to this API call determine the actual configuration of your agent\.  
For more information, see [Creating and activating an agent](https://docs.aws.amazon.com/datasync/latest/userguide/activating-agent.html) in the * AWS DataSync User Guide\.*   
*Required*: No  
*Type*: String  
*Maximum*: `29`  
*Pattern*: `[A-Z0-9]{5}(-[A-Z0-9]{5}){4}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AgentName`  <a name="cfn-datasync-agent-agentname"></a>
The name you configured for your agent\. This value is a text reference that is used to identify the agent in the console\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[a-zA-Z0-9\s+=._:@/-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupArns`  <a name="cfn-datasync-agent-securitygrouparns"></a>
The Amazon Resource Names \(ARNs\) of the security groups used to protect your data transfer task subnets\. See [SecurityGroupArns](https://docs.aws.amazon.com/datasync/latest/userguide/API_Ec2Config.html#DataSync-Type-Ec2Config-SecurityGroupArns)\.  
*Pattern*: `^arn:(aws|aws-cn|aws-us-gov|aws-iso|aws-iso-b):ec2:[a-z\-0-9]*:[0-9]{12}:security-group/.*$`  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetArns`  <a name="cfn-datasync-agent-subnetarns"></a>
The Amazon Resource Names \(ARNs\) of the subnets in which DataSync will create elastic network interfaces for each data transfer task\. The agent that runs a task must be private\. When you start a task that is associated with an agent created in a VPC, or one that has access to an IP address in a VPC, then the task is also private\. In this case, DataSync creates four network interfaces for each task in your subnet\. For a data transfer to work, the agent must be able to route to all these four network interfaces\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-datasync-agent-tags"></a>
The key\-value pair that represents the tag that you want to associate with the agent\. The value can be an empty string\. This value helps you manage, filter, and search for your agents\.  
Valid characters for key and value are letters, spaces, and numbers representable in UTF\-8 format, and the following special characters: \+ \- = \. \_ : / @\. 
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcEndpointId`  <a name="cfn-datasync-agent-vpcendpointid"></a>
The ID of the virtual private cloud \(VPC\) endpoint that the agent has access to\. This is the client\-side VPC endpoint, powered by AWS PrivateLink\. If you don't have an AWS PrivateLink VPC endpoint, see [AWS PrivateLink and VPC endpoints](https://docs.aws.amazon.com/vpc/latest/userguide/endpoint-services-overview.html) in the *Amazon VPC User Guide*\.  
For more information about activating your agent in a private network based on a VPC, see [Using AWS DataSync in a Virtual Private Cloud](https://docs.aws.amazon.com/datasync/latest/userguide/datasync-in-vpc.html) in the *AWS DataSync User Guide\.*  
A VPC endpoint ID looks like this: `vpce-01234d5aff67890e1`\.  
*Required*: No  
*Type*: String  
*Pattern*: `^vpce-[0-9a-f]{17}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-datasync-agent-return-values"></a>

### Ref<a name="aws-resource-datasync-agent-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the agent Amazon Resource Name \(ARN\)\. For example:

`arn:aws:datasync:us-east-2:111222333444:agent/agent-0b0addbeef44baca3`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-datasync-agent-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-datasync-agent-return-values-fn--getatt-fn--getatt"></a>

`AgentArn`  <a name="AgentArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the agent\. Use the `ListAgents` operation to return a list of agents for your account and AWS Region\.

`EndpointType`  <a name="EndpointType-fn::getatt"></a>
The type of endpoint that your agent is connected to\. If the endpoint is a VPC endpoint, the agent is not accessible over the public internet\.

## Examples<a name="aws-resource-datasync-agent--examples"></a>



### DataSync Agent<a name="aws-resource-datasync-agent--examples--DataSync_Agent"></a>

The following example specifies a DataSync agent named `MyAgent`\. The agent activation key is included in the template\.

#### JSON<a name="aws-resource-datasync-agent--examples--DataSync_Agent--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "Specifies a DataSync agent",
  "Resources": 
    {
      "Agent": {
        "Type": "AWS::DataSync::Agent",
        "Properties": {
          "ActivationKey": "AAAAA-7AAAA-GG7MC-3I9R3-27COD",
          "AgentName": "MyAgent"
          }
      }
    }
}
```

#### YAML<a name="aws-resource-datasync-agent--examples--DataSync_Agent--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: Specifies a DataSync agent
Resources:
  Agent:
    Type: AWS::DataSync::Agent
    Properties:
      ActivationKey: AAAAA-7AAAA-GG7MC-3I9R3-27COD
      AgentName: MyAgent
```