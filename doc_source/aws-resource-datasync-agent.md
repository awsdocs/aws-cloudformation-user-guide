# AWS::DataSync::Agent<a name="aws-resource-datasync-agent"></a>

The `AWS::DataSync::Agent` resource activates an AWS DataSync agent that you've deployed for storage discovery or data transfers\. The activation process associates the agent with your AWS account\.

For more information, see the following topics in the *AWS DataSync User Guide*:
+ [DataSync agent requirements](https://docs.aws.amazon.com/datasync/latest/userguide/agent-requirements.html)
+ [DataSync network requirements](https://docs.aws.amazon.com/datasync/latest/userguide/datasync-network.html)
+ [Create a DataSync agent](https://docs.aws.amazon.com/datasync/latest/userguide/configure-agent.html)

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
Specifies your DataSync agent's activation key\. If you don't have an activation key, see [Activate your agent](https://docs.aws.amazon.com/datasync/latest/userguide/activate-agent.html)\.  
*Required*: No  
*Type*: String  
*Maximum*: `29`  
*Pattern*: `[A-Z0-9]{5}(-[A-Z0-9]{5}){4}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AgentName`  <a name="cfn-datasync-agent-agentname"></a>
Specifies a name for your agent\. You can see this name in the DataSync console\.  
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
Specifies the ARN of the subnet where you want to run your DataSync task when using a VPC endpoint\. This is the subnet where DataSync creates and manages the [network interfaces](https://docs.aws.amazon.com/datasync/latest/userguide/datasync-network.html#required-network-interfaces) for your transfer\. You can only specify one ARN\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-datasync-agent-tags"></a>
Specifies labels that help you categorize, filter, and search for your AWS resources\. We recommend creating at least one tag for your agent\.  
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