# AWS::Shield::Protection<a name="aws-resource-shield-protection"></a>

Enables AWS Shield Advanced for a specific AWS resource\. The resource can be an Amazon CloudFront distribution, Amazon Route 53 hosted zone, AWS Global Accelerator standard accelerator, Elastic IP Address, Application Load Balancer, or a Classic Load Balancer\. You can protect Amazon EC2 instances and Network Load Balancers by association with protected Amazon EC2 Elastic IP addresses\.

Use this to add protection to a single resource at a time\. You can add protection to multiple resources at once through the [Shield Advanced console](https://console.aws.amazon.com/wafv2/shieldv2#/)\. For more information see [Getting Started with AWS Shield Advanced](https://docs.aws.amazon.com/waf/latest/developerguide/getting-started-ddos.html) and [Managing resource protections in AWS Shield Advanced](https://docs.aws.amazon.com/waf/latest/developerguide/ddos-manage-protected-resources.html)\.

**Note**  
To configure this resource through AWS CloudFormation, you must be subscribed to AWS Shield Advanced\. You can subscribe through the [Shield Advanced console](https://console.aws.amazon.com/wafv2/shieldv2#/) and through the APIs\. For more information, see [Subscribe to AWS Shield Advanced](https://docs.aws.amazon.com/waf/latest/developerguide/enable-ddos-prem.html)\. 

## Syntax<a name="aws-resource-shield-protection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-shield-protection-syntax.json"></a>

```
{
  "Type" : "AWS::Shield::Protection",
  "Properties" : {
      "[ApplicationLayerAutomaticResponseConfiguration](#cfn-shield-protection-applicationlayerautomaticresponseconfiguration)" : ApplicationLayerAutomaticResponseConfiguration,
      "[HealthCheckArns](#cfn-shield-protection-healthcheckarns)" : [ String, ... ],
      "[Name](#cfn-shield-protection-name)" : String,
      "[ResourceArn](#cfn-shield-protection-resourcearn)" : String,
      "[Tags](#cfn-shield-protection-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-shield-protection-syntax.yaml"></a>

```
Type: AWS::Shield::Protection
Properties: 
  [ApplicationLayerAutomaticResponseConfiguration](#cfn-shield-protection-applicationlayerautomaticresponseconfiguration): 
    ApplicationLayerAutomaticResponseConfiguration
  [HealthCheckArns](#cfn-shield-protection-healthcheckarns): 
    - String
  [Name](#cfn-shield-protection-name): String
  [ResourceArn](#cfn-shield-protection-resourcearn): String
  [Tags](#cfn-shield-protection-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-shield-protection-properties"></a>

`ApplicationLayerAutomaticResponseConfiguration`  <a name="cfn-shield-protection-applicationlayerautomaticresponseconfiguration"></a>
The automatic application layer DDoS mitigation settings for the protection\. This configuration determines whether Shield Advanced automatically manages rules in the web ACL in order to respond to application layer events that Shield Advanced determines to be DDoS attacks\.   
*Required*: No  
*Type*: [ApplicationLayerAutomaticResponseConfiguration](aws-properties-shield-protection-applicationlayerautomaticresponseconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckArns`  <a name="cfn-shield-protection-healthcheckarns"></a>
The ARN \(Amazon Resource Name\) of the health check to associate with the protection\. Health\-based detection provides improved responsiveness and accuracy in attack detection and mitigation\.   
You can use this option with any resource type except for Route 53 hosted zones\.  
For more information, see [Configuring health\-based detection using health checks](https://docs.aws.amazon.com/waf/latest/developerguide/ddos-advanced-health-checks.html) in the *AWS Shield Advanced Developer Guide*\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-shield-protection-name"></a>
The name of the protection\. For example, `My CloudFront distributions`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[ a-zA-Z0-9_\\.\\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceArn`  <a name="cfn-shield-protection-resourcearn"></a>
The ARN \(Amazon Resource Name\) of the AWS resource that is protected\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^arn:aws.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-shield-protection-tags"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
To modify tags on existing resources, use the AWS Shield Advanced APIs or command line interface\. With AWS CloudFormation, you can only add tags to resources during resource creation\. 
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-shield-protection-return-values"></a>

### Ref<a name="aws-resource-shield-protection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the ARN \(Amazon Resource Name\) of the protection\. 

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-shield-protection-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-shield-protection-return-values-fn--getatt-fn--getatt"></a>

`ProtectionArn`  <a name="ProtectionArn-fn::getatt"></a>
The ARN \(Amazon Resource Name\) of the new protection\. 

`ProtectionId`  <a name="ProtectionId-fn::getatt"></a>
The ID of the new protection\. 

## Examples<a name="aws-resource-shield-protection--examples"></a>



### Create a network layer protection<a name="aws-resource-shield-protection--examples--Create_a_network_layer_protection"></a>

The following shows an example protection configuration for an Amazon EC2 Elastic IP address\. 

#### YAML<a name="aws-resource-shield-protection--examples--Create_a_network_layer_protection--yaml"></a>

```
Resources:
  EIP:
    Type: AWS::EC2::EIP
  Protection:
    Type: AWS::Shield::Protection
    Properties:
      Name: 'MyEIPProtection'
            ResourceArn: !Sub 'arn:${AWS::Partition}:ec2:${AWS::Region}:${AWS::AccountId}:eip-allocation/${EIP.AllocationId}'
```

#### JSON<a name="aws-resource-shield-protection--examples--Create_a_network_layer_protection--json"></a>

```
{
    "Resources": {
        "EIP": {
            "Type": "AWS::EC2::EIP"
        },
        "Protection": {
            "Type": "AWS::Shield::Protection",
            "Properties": {
                "Name": "MyEIPProtection",
                "ResourceArn": {
                    "Fn::Sub": "arn:${AWS::Partition}:ec2:${AWS::Region}:${AWS::AccountId}:eip-allocation/${EIP.AllocationId}"
                }
            }
        }
    }
}
```

### Create an application layer protection<a name="aws-resource-shield-protection--examples--Create_an_application_layer_protection"></a>

The following shows an example layer 7 protection configuration for an application load balancer\. The protection includes a health check and has application layer automatic response enabled\. The load balancer must be associated with an AWS WAF web ACL that has a rate\-based rule defined in it\. 

#### YAML<a name="aws-resource-shield-protection--examples--Create_an_application_layer_protection--yaml"></a>

```
Resources:
  # Create L7 Protection
  Protection:
    Type: AWS::Shield::Protection
    DependsOn:
    - WebACLAssociation
    Properties:
      Name: 'MyL7Protection'
      ResourceArn: !Ref ALB
      HealthCheckArns:
        - !Sub 'arn:${AWS::Partition}:route53:::healthcheck/${HealthCheck}'
      ApplicationLayerAutomaticResponseConfiguration:
        Status: ENABLED
        Action:
          Block: { }
```

#### JSON<a name="aws-resource-shield-protection--examples--Create_an_application_layer_protection--json"></a>

```
{
    "Resources": {
        "Protection": {
            "Type": "AWS::Shield::Protection",
            "DependsOn": [
                "WebACLAssociation"
            ],
            "Properties": {
                "Name": "MyL7Protection",
                "ResourceArn": {
                    "Ref": "ALB"
                },
                "HealthCheckArns": [
                    {
                        "Fn::Sub": "arn:${AWS::Partition}:route53:::healthcheck/${HealthCheck}"
                    }
                ],
                "ApplicationLayerAutomaticResponseConfiguration": {
                    "Status": "ENABLED",
                    "Action": {
                        "Block": {}
                    }
                }
            }
        }
    }
}
```