# AWS::ElasticLoadBalancingV2::ListenerRule<a name="aws-resource-elasticloadbalancingv2-listenerrule"></a>

Specifies a listener rule\. The listener must be associated with an Application Load Balancer\. Each rule consists of a priority, one or more actions, and one or more conditions\.

## Syntax<a name="aws-resource-elasticloadbalancingv2-listenerrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-listenerrule-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::ListenerRule",
  "Properties" : {
      "[Actions](#cfn-elasticloadbalancingv2-listenerrule-actions)" : [ Action, ... ],
      "[Conditions](#cfn-elasticloadbalancingv2-listenerrule-conditions)" : [ RuleCondition, ... ],
      "[ListenerArn](#cfn-elasticloadbalancingv2-listenerrule-listenerarn)" : String,
      "[Priority](#cfn-elasticloadbalancingv2-listenerrule-priority)" : Integer
    }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-listenerrule-syntax.yaml"></a>

```
Type: AWS::ElasticLoadBalancingV2::ListenerRule
Properties: 
  [Actions](#cfn-elasticloadbalancingv2-listenerrule-actions): 
    - Action
  [Conditions](#cfn-elasticloadbalancingv2-listenerrule-conditions): 
    - RuleCondition
  [ListenerArn](#cfn-elasticloadbalancingv2-listenerrule-listenerarn): String
  [Priority](#cfn-elasticloadbalancingv2-listenerrule-priority): Integer
```

## Properties<a name="aws-resource-elasticloadbalancingv2-listenerrule-properties"></a>

`Actions`  <a name="cfn-elasticloadbalancingv2-listenerrule-actions"></a>
The actions\.  
The rule must include exactly one of the following types of actions: `forward`, `fixed-response`, or `redirect`, and it must be the last action to be performed\. If the rule is for an HTTPS listener, it can also optionally include an authentication action\.  
*Required*: Yes  
*Type*: List of [Action](aws-properties-elasticloadbalancingv2-listenerrule-actions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Conditions`  <a name="cfn-elasticloadbalancingv2-listenerrule-conditions"></a>
The conditions\.  
The rule can optionally include up to one of each of the following conditions: `http-request-method`, `host-header`, `path-pattern`, and `source-ip`\. A rule can also optionally include one or more of each of the following conditions: `http-header` and `query-string`\.  
*Required*: Yes  
*Type*: List of [RuleCondition](aws-properties-elasticloadbalancingv2-listenerrule-conditions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ListenerArn`  <a name="cfn-elasticloadbalancingv2-listenerrule-listenerarn"></a>
The Amazon Resource Name \(ARN\) of the listener\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Priority`  <a name="cfn-elasticloadbalancingv2-listenerrule-priority"></a>
The rule priority\. A listener can't have multiple rules with the same priority\.  
If you try to reorder rules by updating their priorities, do not specify a new priority if an existing rule already uses this priority, as this can cause an error\. If you need to reuse a priority with a different rule, you must remove it as a priority first, and then specify it in a subsequent update\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `50000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-elasticloadbalancingv2-listenerrule-return-values"></a>

### Ref<a name="aws-resource-elasticloadbalancingv2-listenerrule-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the listener rule\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples"></a>



### HTTP Header Rule Example<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--HTTP_Header_Rule_Example"></a>



#### YAML<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--HTTP_Header_Rule_Example--yaml"></a>

```
Parameters:
  CidrBlockForVPC:
    Default: 187.0.0.0/24
    Description: CidrBlockForVPC
    Type: String
  CidrBlockForSubnet1:
    Default: 187.0.0.0/25
    Description: Cidr Block For Subnet1
    Type: String
  CidrBlockForSubnet2:
    Default: 187.0.0.128/25
    Description: Cidr Block For Subnet2
    Type: String
  AvailabilityZoneForSubnet1:
    Default: us-east-1c
    Description: AvailabilityZone For Subnet1
    Type: String
  AvailabilityZoneForSubnet2:
    Default: us-east-1b
    Description: AvailabilityZone For Subnet2
    Type: String
Resources:
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: !Ref CidrBlockForVPC
  Subnet1:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
      AvailabilityZone: !Ref AvailabilityZoneForSubnet1
      CidrBlock: !Ref CidrBlockForSubnet1
  Subnet2:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
      AvailabilityZone: !Ref AvailabilityZoneForSubnet2
      CidrBlock: !Ref CidrBlockForSubnet2
  LoadBalancer:
    Type: 'AWS::ElasticLoadBalancingV2::LoadBalancer'
    Properties:
      Scheme: internal
      Subnets:
        - !Ref Subnet1
        - !Ref Subnet2
  TargetGroup1:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      Port: 1000
      Protocol: HTTP
      VpcId: !Ref VPC
  TargetGroup2:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      Port: 2000
      Protocol: HTTP
      VpcId: !Ref VPC
  ListenerRule1:
    Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
    Properties:
      Actions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup1
      Conditions:
        - Field: http-header
          HttpHeaderConfig:
            HttpHeaderName: User-Agent
            Values:
              - Mozilla
        - Field: http-header
          HttpHeaderConfig:
            HttpHeaderName: Referer
            Values:
              - 'https://www.amazon.com/'
      ListenerArn: !Ref Listener
      Priority: 1
  ListenerRule2:
    Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
    Properties:
      Actions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup2
      Conditions:
        - Field: http-header
          HttpHeaderConfig:
            HttpHeaderName: User-Agent
            Values:
              - Chrome
      ListenerArn: !Ref Listener
      Priority: 2
  Listener:
    Type: 'AWS::ElasticLoadBalancingV2::Listener'
    Properties:
      DefaultActions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup1
      LoadBalancerArn: !Ref LoadBalancer
      Port: '8000'
      Protocol: HTTP
  LoadBalancerAlarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      Namespace: AWS/ApplicationELB
      Dimensions:
        - Name: LoadBalancer
          Value: !GetAtt 
            - LoadBalancer
            - LoadBalancerFullName
        - Name: TargetGroup
          Value: !GetAtt 
            - TargetGroup1
            - TargetGroupFullName
      MetricName: UnHealthyHostCount
      Period: 60
      Statistic: Average
      ComparisonOperator: GreaterThanThreshold
      Threshold: 0
      EvaluationPeriods: 1
Outputs:
  LoadBalancer:
    Value: !Ref LoadBalancer
  TargetGroup1:
    Value: !Ref TargetGroup1
  TargetGroup2:
    Value: !Ref TargetGroup2
  ListenerArn:
    Value: !Ref Listener
  ListenerRule1Arn:
    Value: !Ref ListenerRule1
  ListenerRule2Arn:
    Value: !Ref ListenerRule2
  LoadBalancersAssociatedWithTargetGroup1:
    Description: LoadBalancers associated with TargetGroup
    Value: !Select 
      - '0'
      - !GetAtt 
        - TargetGroup1
        - LoadBalancerArns
  LoadBalancersAssociatedWithTargetGroup2:
    Description: LoadBalancers associated with TargetGroup
    Value: !Select 
      - '0'
      - !GetAtt 
        - TargetGroup2
        - LoadBalancerArns
  TargetGroupFullName1:
    Description: FullName of TargetGroup1
    Value: !GetAtt 
      - TargetGroup1
      - TargetGroupFullName
  TargetGroupFullName2:
    Description: FullName of TargetGroup2
    Value: !GetAtt 
      - TargetGroup2
      - TargetGroupFullName
```

#### JSON<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--HTTP_Header_Rule_Example--json"></a>

```
{
  "Parameters": {
    "CidrBlockForVPC" : {
      "Default" : "187.0.0.0/24",
      "Description" : "CidrBlockForVPC",
      "Type" : "String"
    },
    "CidrBlockForSubnet1" : {
      "Default" : "187.0.0.0/25",
      "Description" : "Cidr Block For Subnet1",
      "Type" : "String"
    },
    "CidrBlockForSubnet2" : {
      "Default" : "187.0.0.128/25",
      "Description" : "Cidr Block For Subnet2",
      "Type" : "String"
    },
    "AvailabilityZoneForSubnet1" : {
      "Default" : "us-east-1c",
      "Description" : "AvailabilityZone For Subnet1",
      "Type" : "String"
    },
    "AvailabilityZoneForSubnet2" : {
      "Default" : "us-east-1b",
      "Description" : "AvailabilityZone For Subnet2",
      "Type" : "String"
    }
  },
  "Resources": {
    "VPC": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": {"Ref" : "CidrBlockForVPC"}
      }
    },
    "Subnet1": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId" : { "Ref" : "VPC" },
        "AvailabilityZone": { "Ref": "AvailabilityZoneForSubnet1" },
        "CidrBlock": {"Ref" : "CidrBlockForSubnet1"}
      }
    },
    "Subnet2": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId" : { "Ref" : "VPC" },
        "AvailabilityZone": { "Ref": "AvailabilityZoneForSubnet2" },
        "CidrBlock": {"Ref" : "CidrBlockForSubnet2"}
      }
    },
    "LoadBalancer" : {
      "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
      "Properties": {
        "Scheme" : "internal",
        "Subnets" : [ {"Ref": "Subnet1"}, {"Ref" : "Subnet2"} ]
      }
    },
    "TargetGroup1" : {
      "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties" : {
        "Port": 1000,
        "Protocol": "HTTP",
        "VpcId": { "Ref" : "VPC" }
      }
    },
    "TargetGroup2" : {
      "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties" : {
        "Port": 2000,
        "Protocol": "HTTP",
        "VpcId": { "Ref" : "VPC" }
      }
    },
    "ListenerRule1": {
      "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
      "Properties": {
        "Actions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup1" }
        }],
        "Conditions": [{
          "Field": "http-header",
          "HttpHeaderConfig": {
              "HttpHeaderName": "User-Agent",
              "Values": ["Mozilla"]
          }
        },
        {
          "Field": "http-header",
          "HttpHeaderConfig": {
              "HttpHeaderName": "Referer",
              "Values": ["https://www.amazon.com/"]
          }
         }],
        "ListenerArn": { "Ref": "Listener" },
        "Priority": 1
      }
    },
    "ListenerRule2": {
      "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
      "Properties": {
        "Actions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup2" }
        }],
        "Conditions": [{
          "Field": "http-header",
          "HttpHeaderConfig": {
              "HttpHeaderName": "User-Agent",
              "Values": ["Chrome"]
          }
        }],
        "ListenerArn": { "Ref": "Listener" },
        "Priority": 2
      }
    },
    "Listener": {
      "Type": "AWS::ElasticLoadBalancingV2::Listener",
      "Properties": {
        "DefaultActions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup1" }
        }],
        "LoadBalancerArn": { "Ref": "LoadBalancer" },
        "Port": "8000",
        "Protocol": "HTTP"
      }
    },
    "LoadBalancerAlarm": {
      "Type": "AWS::CloudWatch::Alarm",
      "Properties": {
        "Namespace": "AWS/ApplicationELB",
        "Dimensions": [
          {
            "Name": "LoadBalancer",
            "Value": {"Fn::GetAtt" : ["LoadBalancer", "LoadBalancerFullName"]}
          },
          {
            "Name": "TargetGroup",
            "Value": {"Fn::GetAtt" : ["TargetGroup1", "TargetGroupFullName"]}
          }
        ],
        "MetricName": "UnHealthyHostCount",
        "Period": 60,
        "Statistic": "Average",
        "ComparisonOperator": "GreaterThanThreshold",
        "Threshold": 0,
        "EvaluationPeriods": 1
      }
    }
  },
  "Outputs": {
    "LoadBalancer": {
      "Value": {
        "Ref": "LoadBalancer"
      }
    },
    "TargetGroup1": {
      "Value": {
        "Ref": "TargetGroup1"
      }
    },
    "TargetGroup2": {
      "Value": {
        "Ref": "TargetGroup2"
      }
    },
    "ListenerArn": {
      "Value": {
        "Ref": "Listener"
      }
    },
    "ListenerRule1Arn": {
      "Value": {
        "Ref": "ListenerRule1"
      }
    },
    "ListenerRule2Arn": {
      "Value": {
        "Ref": "ListenerRule2"
      }
    },
    "LoadBalancersAssociatedWithTargetGroup1" : {
      "Description" : "LoadBalancers associated with TargetGroup",
      "Value" : { "Fn::Select" : [ "0",
          { "Fn::GetAtt" : ["TargetGroup1", "LoadBalancerArns"] }
        ]
      }
    },
    "LoadBalancersAssociatedWithTargetGroup2" : {
      "Description" : "LoadBalancers associated with TargetGroup",
      "Value" : { "Fn::Select" : [ "0",
          { "Fn::GetAtt" : ["TargetGroup2", "LoadBalancerArns"] }
        ]
      }
    },
    "TargetGroupFullName1" : {
      "Description" : "FullName of TargetGroup1",
      "Value" : {"Fn::GetAtt" : ["TargetGroup1", "TargetGroupFullName"]}
    },
    "TargetGroupFullName2" : {
      "Description" : "FullName of TargetGroup2",
      "Value" : {"Fn::GetAtt" : ["TargetGroup2", "TargetGroupFullName"]}
    }
  }
}
```

### HTTP Request Method Rule Example<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--HTTP_Request_Method_Rule_Example"></a>



#### YAML<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--HTTP_Request_Method_Rule_Example--yaml"></a>

```
Parameters:
  CidrBlockForVPC:
    Default: 187.0.0.0/24
    Description: CidrBlockForVPC
    Type: String
  CidrBlockForSubnet1:
    Default: 187.0.0.0/25
    Description: Cidr Block For Subnet1
    Type: String
  CidrBlockForSubnet2:
    Default: 187.0.0.128/25
    Description: Cidr Block For Subnet2
    Type: String
  AvailabilityZoneForSubnet1:
    Default: us-east-1c
    Description: AvailabilityZone For Subnet1
    Type: String
  AvailabilityZoneForSubnet2:
    Default: us-east-1b
    Description: AvailabilityZone For Subnet2
    Type: String
Resources:
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: !Ref CidrBlockForVPC
  Subnet1:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
      AvailabilityZone: !Ref AvailabilityZoneForSubnet1
      CidrBlock: !Ref CidrBlockForSubnet1
  Subnet2:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
      AvailabilityZone: !Ref AvailabilityZoneForSubnet2
      CidrBlock: !Ref CidrBlockForSubnet2
  LoadBalancer:
    Type: 'AWS::ElasticLoadBalancingV2::LoadBalancer'
    Properties:
      Scheme: internal
      Subnets:
        - !Ref Subnet1
        - !Ref Subnet2
  TargetGroup1:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      Port: 1000
      Protocol: HTTP
      VpcId: !Ref VPC
  TargetGroup2:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      Port: 2000
      Protocol: HTTP
      VpcId: !Ref VPC
  ListenerRule1:
    Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
    Properties:
      Actions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup1
      Conditions:
        - Field: http-request-method
          HttpRequestMethodConfig:
            Values:
              - GET_OR_HEAD
      ListenerArn: !Ref Listener
      Priority: 1
  ListenerRule2:
    Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
    Properties:
      Actions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup2
      Conditions:
        - Field: http-request-method
          HttpRequestMethodConfig:
            Values:
              - POST
      ListenerArn: !Ref Listener
      Priority: 2
  Listener:
    Type: 'AWS::ElasticLoadBalancingV2::Listener'
    Properties:
      DefaultActions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup1
      LoadBalancerArn: !Ref LoadBalancer
      Port: '8000'
      Protocol: HTTP
  LoadBalancerAlarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      Namespace: AWS/ApplicationELB
      Dimensions:
        - Name: LoadBalancer
          Value: !GetAtt 
            - LoadBalancer
            - LoadBalancerFullName
        - Name: TargetGroup
          Value: !GetAtt 
            - TargetGroup1
            - TargetGroupFullName
      MetricName: UnHealthyHostCount
      Period: 60
      Statistic: Average
      ComparisonOperator: GreaterThanThreshold
      Threshold: 0
      EvaluationPeriods: 1
Outputs:
  LoadBalancer:
    Value: !Ref LoadBalancer
  TargetGroup1:
    Value: !Ref TargetGroup1
  TargetGroup2:
    Value: !Ref TargetGroup2
  ListenerArn:
    Value: !Ref Listener
  ListenerRule1Arn:
    Value: !Ref ListenerRule1
  ListenerRule2Arn:
    Value: !Ref ListenerRule2
  LoadBalancersAssociatedWithTargetGroup1:
    Description: LoadBalancers associated with TargetGroup
    Value: !Select 
      - '0'
      - !GetAtt 
        - TargetGroup1
        - LoadBalancerArns
  LoadBalancersAssociatedWithTargetGroup2:
    Description: LoadBalancers associated with TargetGroup
    Value: !Select 
      - '0'
      - !GetAtt 
        - TargetGroup2
        - LoadBalancerArns
  TargetGroupFullName1:
    Description: FullName of TargetGroup1
    Value: !GetAtt 
      - TargetGroup1
      - TargetGroupFullName
  TargetGroupFullName2:
    Description: FullName of TargetGroup2
    Value: !GetAtt 
      - TargetGroup2
      - TargetGroupFullName
```

#### JSON<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--HTTP_Request_Method_Rule_Example--json"></a>

```
{
  "Parameters": {
    "CidrBlockForVPC" : {
      "Default" : "187.0.0.0/24",
      "Description" : "CidrBlockForVPC",
      "Type" : "String"
    },
    "CidrBlockForSubnet1" : {
      "Default" : "187.0.0.0/25",
      "Description" : "Cidr Block For Subnet1",
      "Type" : "String"
    },
    "CidrBlockForSubnet2" : {
      "Default" : "187.0.0.128/25",
      "Description" : "Cidr Block For Subnet2",
      "Type" : "String"
    },
    "AvailabilityZoneForSubnet1" : {
      "Default" : "us-east-1c",
      "Description" : "AvailabilityZone For Subnet1",
      "Type" : "String"
    },
    "AvailabilityZoneForSubnet2" : {
      "Default" : "us-east-1b",
      "Description" : "AvailabilityZone For Subnet2",
      "Type" : "String"
    }
  },
  "Resources": {
    "VPC": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": {"Ref" : "CidrBlockForVPC"}
      }
    },
    "Subnet1": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId" : { "Ref" : "VPC" },
        "AvailabilityZone": { "Ref": "AvailabilityZoneForSubnet1" },
        "CidrBlock": {"Ref" : "CidrBlockForSubnet1"}
      }
    },
    "Subnet2": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId" : { "Ref" : "VPC" },
        "AvailabilityZone": { "Ref": "AvailabilityZoneForSubnet2" },
        "CidrBlock": {"Ref" : "CidrBlockForSubnet2"}
      }
    },
    "LoadBalancer" : {
      "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
      "Properties": {
        "Scheme" : "internal",
        "Subnets" : [ {"Ref": "Subnet1"}, {"Ref" : "Subnet2"} ]
      }
    },
    "TargetGroup1" : {
      "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties" : {
        "Port": 1000,
        "Protocol": "HTTP",
        "VpcId": { "Ref" : "VPC" }
      }
    },
    "TargetGroup2" : {
      "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties" : {
        "Port": 2000,
        "Protocol": "HTTP",
        "VpcId": { "Ref" : "VPC" }
      }
    },
    "ListenerRule1": {
      "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
      "Properties": {
        "Actions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup1" }
        }],
        "Conditions": [{
          "Field": "http-request-method",
          "HttpRequestMethodConfig": {
              "Values": ["GET_OR_HEAD"]
          }
        }],
        "ListenerArn": { "Ref": "Listener" },
        "Priority": 1
      }
    },
    "ListenerRule2": {
      "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
      "Properties": {
        "Actions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup2" }
        }],
        "Conditions": [{
          "Field": "http-request-method",
          "HttpRequestMethodConfig": {
              "Values": ["POST"]
          }
        }],
        "ListenerArn": { "Ref": "Listener" },
        "Priority": 2
      }
    },
    "Listener": {
      "Type": "AWS::ElasticLoadBalancingV2::Listener",
      "Properties": {
        "DefaultActions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup1" }
        }],
        "LoadBalancerArn": { "Ref": "LoadBalancer" },
        "Port": "8000",
        "Protocol": "HTTP"
      }
    },
    "LoadBalancerAlarm": {
      "Type": "AWS::CloudWatch::Alarm",
      "Properties": {
        "Namespace": "AWS/ApplicationELB",
        "Dimensions": [
          {
            "Name": "LoadBalancer",
            "Value": {"Fn::GetAtt" : ["LoadBalancer", "LoadBalancerFullName"]}
          },
          {
            "Name": "TargetGroup",
            "Value": {"Fn::GetAtt" : ["TargetGroup1", "TargetGroupFullName"]}
          }
        ],
        "MetricName": "UnHealthyHostCount",
        "Period": 60,
        "Statistic": "Average",
        "ComparisonOperator": "GreaterThanThreshold",
        "Threshold": 0,
        "EvaluationPeriods": 1
      }
    }
  },
  "Outputs": {
    "LoadBalancer": {
      "Value": {
        "Ref": "LoadBalancer"
      }
    },
    "TargetGroup1": {
      "Value": {
        "Ref": "TargetGroup1"
      }
    },
    "TargetGroup2": {
      "Value": {
        "Ref": "TargetGroup2"
      }
    },
    "ListenerArn": {
      "Value": {
        "Ref": "Listener"
      }
    },
    "ListenerRule1Arn": {
      "Value": {
        "Ref": "ListenerRule1"
      }
    },
    "ListenerRule2Arn": {
      "Value": {
        "Ref": "ListenerRule2"
      }
    },
    "LoadBalancersAssociatedWithTargetGroup1" : {
      "Description" : "LoadBalancers associated with TargetGroup",
      "Value" : { "Fn::Select" : [ "0",
          { "Fn::GetAtt" : ["TargetGroup1", "LoadBalancerArns"] }
        ]
      }
    },
    "LoadBalancersAssociatedWithTargetGroup2" : {
      "Description" : "LoadBalancers associated with TargetGroup",
      "Value" : { "Fn::Select" : [ "0",
          { "Fn::GetAtt" : ["TargetGroup2", "LoadBalancerArns"] }
        ]
      }
    },
    "TargetGroupFullName1" : {
      "Description" : "FullName of TargetGroup1",
      "Value" : {"Fn::GetAtt" : ["TargetGroup1", "TargetGroupFullName"]}
    },
    "TargetGroupFullName2" : {
      "Description" : "FullName of TargetGroup2",
      "Value" : {"Fn::GetAtt" : ["TargetGroup2", "TargetGroupFullName"]}
    }
  }
}
```

### Query String Rule Example<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--Query_String_Rule_Example"></a>



#### YAML<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--Query_String_Rule_Example--yaml"></a>

```
Parameters:
  CidrBlockForVPC:
    Default: 187.0.0.0/24
    Description: CidrBlockForVPC
    Type: String
  CidrBlockForSubnet1:
    Default: 187.0.0.0/25
    Description: Cidr Block For Subnet1
    Type: String
  CidrBlockForSubnet2:
    Default: 187.0.0.128/25
    Description: Cidr Block For Subnet2
    Type: String
  AvailabilityZoneForSubnet1:
    Default: us-east-1c
    Description: AvailabilityZone For Subnet1
    Type: String
  AvailabilityZoneForSubnet2:
    Default: us-east-1b
    Description: AvailabilityZone For Subnet2
    Type: String
Resources:
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: !Ref CidrBlockForVPC
  Subnet1:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
      AvailabilityZone: !Ref AvailabilityZoneForSubnet1
      CidrBlock: !Ref CidrBlockForSubnet1
  Subnet2:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
      AvailabilityZone: !Ref AvailabilityZoneForSubnet2
      CidrBlock: !Ref CidrBlockForSubnet2
  LoadBalancer:
    Type: 'AWS::ElasticLoadBalancingV2::LoadBalancer'
    Properties:
      Scheme: internal
      Subnets:
        - !Ref Subnet1
        - !Ref Subnet2
  TargetGroup1:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      Port: 1000
      Protocol: HTTP
      VpcId: !Ref VPC
  TargetGroup2:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      Port: 2000
      Protocol: HTTP
      VpcId: !Ref VPC
  ListenerRule1:
    Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
    Properties:
      Actions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup1
      Conditions:
        - Field: query-string
          QueryStringConfig:
            Values:
              - Key: Foo
                Value: Bar
        - Field: query-string
          QueryStringConfig:
            Values:
              - Key: Bar
                Value: Xyz
      ListenerArn: !Ref Listener
      Priority: 1
  ListenerRule2:
    Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
    Properties:
      Actions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup2
      Conditions:
        - Field: query-string
          QueryStringConfig:
            Values:
              - Key: Foo
                Value: Baz
      ListenerArn: !Ref Listener
      Priority: 2
  Listener:
    Type: 'AWS::ElasticLoadBalancingV2::Listener'
    Properties:
      DefaultActions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup1
      LoadBalancerArn: !Ref LoadBalancer
      Port: '8000'
      Protocol: HTTP
  LoadBalancerAlarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      Namespace: AWS/ApplicationELB
      Dimensions:
        - Name: LoadBalancer
          Value: !GetAtt 
            - LoadBalancer
            - LoadBalancerFullName
        - Name: TargetGroup
          Value: !GetAtt 
            - TargetGroup1
            - TargetGroupFullName
      MetricName: UnHealthyHostCount
      Period: 60
      Statistic: Average
      ComparisonOperator: GreaterThanThreshold
      Threshold: 0
      EvaluationPeriods: 1
Outputs:
  LoadBalancer:
    Value: !Ref LoadBalancer
  TargetGroup1:
    Value: !Ref TargetGroup1
  TargetGroup2:
    Value: !Ref TargetGroup2
  ListenerArn:
    Value: !Ref Listener
  ListenerRule1Arn:
    Value: !Ref ListenerRule1
  ListenerRule2Arn:
    Value: !Ref ListenerRule2
  LoadBalancersAssociatedWithTargetGroup1:
    Description: LoadBalancers associated with TargetGroup
    Value: !Select 
      - '0'
      - !GetAtt 
        - TargetGroup1
        - LoadBalancerArns
  LoadBalancersAssociatedWithTargetGroup2:
    Description: LoadBalancers associated with TargetGroup
    Value: !Select 
      - '0'
      - !GetAtt 
        - TargetGroup2
        - LoadBalancerArns
  TargetGroupFullName1:
    Description: FullName of TargetGroup1
    Value: !GetAtt 
      - TargetGroup1
      - TargetGroupFullName
  TargetGroupFullName2:
    Description: FullName of TargetGroup2
    Value: !GetAtt 
      - TargetGroup2
      - TargetGroupFullName
```

#### JSON<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--Query_String_Rule_Example--json"></a>

```
{
  "Parameters": {
    "CidrBlockForVPC" : {
      "Default" : "187.0.0.0/24",
      "Description" : "CidrBlockForVPC",
      "Type" : "String"
    },
    "CidrBlockForSubnet1" : {
      "Default" : "187.0.0.0/25",
      "Description" : "Cidr Block For Subnet1",
      "Type" : "String"
    },
    "CidrBlockForSubnet2" : {
      "Default" : "187.0.0.128/25",
      "Description" : "Cidr Block For Subnet2",
      "Type" : "String"
    },
    "AvailabilityZoneForSubnet1" : {
      "Default" : "us-east-1c",
      "Description" : "AvailabilityZone For Subnet1",
      "Type" : "String"
    },
    "AvailabilityZoneForSubnet2" : {
      "Default" : "us-east-1b",
      "Description" : "AvailabilityZone For Subnet2",
      "Type" : "String"
    }
  },
  "Resources": {
    "VPC": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": {"Ref" : "CidrBlockForVPC"}
      }
    },
    "Subnet1": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId" : { "Ref" : "VPC" },
        "AvailabilityZone": { "Ref": "AvailabilityZoneForSubnet1" },
        "CidrBlock": {"Ref" : "CidrBlockForSubnet1"}
      }
    },
    "Subnet2": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId" : { "Ref" : "VPC" },
        "AvailabilityZone": { "Ref": "AvailabilityZoneForSubnet2" },
        "CidrBlock": {"Ref" : "CidrBlockForSubnet2"}
      }
    },
    "LoadBalancer" : {
      "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
      "Properties": {
        "Scheme" : "internal",
        "Subnets" : [ {"Ref": "Subnet1"}, {"Ref" : "Subnet2"} ]
      }
    },
    "TargetGroup1" : {
      "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties" : {
        "Port": 1000,
        "Protocol": "HTTP",
        "VpcId": { "Ref" : "VPC" }
      }
    },
    "TargetGroup2" : {
      "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties" : {
        "Port": 2000,
        "Protocol": "HTTP",
        "VpcId": { "Ref" : "VPC" }
      }
    },
    "ListenerRule1": {
      "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
      "Properties": {
        "Actions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup1" }
        }],
        "Conditions": [{
          "Field": "query-string",
          "QueryStringConfig": {
              "Values": [{
                    "Key": "Foo",
                    "Value": "Bar"
              }]
          }
        },
        {
          "Field": "query-string",
          "QueryStringConfig": {
              "Values": [{
                    "Key": "Bar",
                    "Value": "Xyz"
              }]
          }
        }],
        "ListenerArn": { "Ref": "Listener" },
        "Priority": 1
      }
    },
    "ListenerRule2": {
      "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
      "Properties": {
        "Actions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup2" }
        }],
        "Conditions": [{
          "Field": "query-string",
          "QueryStringConfig": {
              "Values": [{
                  "Key": "Foo",
                  "Value": "Baz"
              }]
          }
        }],
        "ListenerArn": { "Ref": "Listener" },
        "Priority": 2
      }
    },
    "Listener": {
      "Type": "AWS::ElasticLoadBalancingV2::Listener",
      "Properties": {
        "DefaultActions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup1" }
        }],
        "LoadBalancerArn": { "Ref": "LoadBalancer" },
        "Port": "8000",
        "Protocol": "HTTP"
      }
    },
    "LoadBalancerAlarm": {
      "Type": "AWS::CloudWatch::Alarm",
      "Properties": {
        "Namespace": "AWS/ApplicationELB",
        "Dimensions": [
          {
            "Name": "LoadBalancer",
            "Value": {"Fn::GetAtt" : ["LoadBalancer", "LoadBalancerFullName"]}
          },
          {
            "Name": "TargetGroup",
            "Value": {"Fn::GetAtt" : ["TargetGroup1", "TargetGroupFullName"]}
          }
        ],
        "MetricName": "UnHealthyHostCount",
        "Period": 60,
        "Statistic": "Average",
        "ComparisonOperator": "GreaterThanThreshold",
        "Threshold": 0,
        "EvaluationPeriods": 1
      }
    }
  },
  "Outputs": {
    "LoadBalancer": {
      "Value": {
        "Ref": "LoadBalancer"
      }
    },
    "TargetGroup1": {
      "Value": {
        "Ref": "TargetGroup1"
      }
    },
    "TargetGroup2": {
      "Value": {
        "Ref": "TargetGroup2"
      }
    },
    "ListenerArn": {
      "Value": {
        "Ref": "Listener"
      }
    },
    "ListenerRule1Arn": {
      "Value": {
        "Ref": "ListenerRule1"
      }
    },
    "ListenerRule2Arn": {
      "Value": {
        "Ref": "ListenerRule2"
      }
    },
    "LoadBalancersAssociatedWithTargetGroup1" : {
      "Description" : "LoadBalancers associated with TargetGroup",
      "Value" : { "Fn::Select" : [ "0",
          { "Fn::GetAtt" : ["TargetGroup1", "LoadBalancerArns"] }
        ]
      }
    },
    "LoadBalancersAssociatedWithTargetGroup2" : {
      "Description" : "LoadBalancers associated with TargetGroup",
      "Value" : { "Fn::Select" : [ "0",
          { "Fn::GetAtt" : ["TargetGroup2", "LoadBalancerArns"] }
        ]
      }
    },
    "TargetGroupFullName1" : {
      "Description" : "FullName of TargetGroup1",
      "Value" : {"Fn::GetAtt" : ["TargetGroup1", "TargetGroupFullName"]}
    },
    "TargetGroupFullName2" : {
      "Description" : "FullName of TargetGroup2",
      "Value" : {"Fn::GetAtt" : ["TargetGroup2", "TargetGroupFullName"]}
    }
  }
}
```

### Source IP Rule Example<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--Source_IP_Rule_Example"></a>



#### YAML<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--Source_IP_Rule_Example--yaml"></a>

```
Parameters:
  CidrBlockForVPC:
    Default: 187.0.0.0/24
    Description: CidrBlockForVPC
    Type: String
  CidrBlockForSubnet1:
    Default: 187.0.0.0/25
    Description: Cidr Block For Subnet1
    Type: String
  CidrBlockForSubnet2:
    Default: 187.0.0.128/25
    Description: Cidr Block For Subnet2
    Type: String
  AvailabilityZoneForSubnet1:
    Default: us-east-1c
    Description: AvailabilityZone For Subnet1
    Type: String
  AvailabilityZoneForSubnet2:
    Default: us-east-1b
    Description: AvailabilityZone For Subnet2
    Type: String
Resources:
  VPC:
    Type: 'AWS::EC2::VPC'
    Properties:
      CidrBlock: !Ref CidrBlockForVPC
  Subnet1:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
      AvailabilityZone: !Ref AvailabilityZoneForSubnet1
      CidrBlock: !Ref CidrBlockForSubnet1
  Subnet2:
    Type: 'AWS::EC2::Subnet'
    Properties:
      VpcId: !Ref VPC
      AvailabilityZone: !Ref AvailabilityZoneForSubnet2
      CidrBlock: !Ref CidrBlockForSubnet2
  LoadBalancer:
    Type: 'AWS::ElasticLoadBalancingV2::LoadBalancer'
    Properties:
      Scheme: internal
      Subnets:
        - !Ref Subnet1
        - !Ref Subnet2
  TargetGroup1:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      Port: 1000
      Protocol: HTTP
      VpcId: !Ref VPC
  TargetGroup2:
    Type: 'AWS::ElasticLoadBalancingV2::TargetGroup'
    Properties:
      Port: 2000
      Protocol: HTTP
      VpcId: !Ref VPC
  ListenerRule1:
    Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
    Properties:
      Actions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup1
      Conditions:
        - Field: source-ip
          SourceIpConfig:
            Values:
              - 172.0.0.0/8
      ListenerArn: !Ref Listener
      Priority: 1
  ListenerRule2:
    Type: 'AWS::ElasticLoadBalancingV2::ListenerRule'
    Properties:
      Actions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup2
      Conditions:
        - Field: source-ip
          SourceIpConfig:
            Values:
              - 192.168.0.0/16
      ListenerArn: !Ref Listener
      Priority: 2
  Listener:
    Type: 'AWS::ElasticLoadBalancingV2::Listener'
    Properties:
      DefaultActions:
        - Type: forward
          TargetGroupArn: !Ref TargetGroup1
      LoadBalancerArn: !Ref LoadBalancer
      Port: '8000'
      Protocol: HTTP
  LoadBalancerAlarm:
    Type: 'AWS::CloudWatch::Alarm'
    Properties:
      Namespace: AWS/ApplicationELB
      Dimensions:
        - Name: LoadBalancer
          Value: !GetAtt 
            - LoadBalancer
            - LoadBalancerFullName
        - Name: TargetGroup
          Value: !GetAtt 
            - TargetGroup1
            - TargetGroupFullName
      MetricName: UnHealthyHostCount
      Period: 60
      Statistic: Average
      ComparisonOperator: GreaterThanThreshold
      Threshold: 0
      EvaluationPeriods: 1
Outputs:
  LoadBalancer:
    Value: !Ref LoadBalancer
  TargetGroup1:
    Value: !Ref TargetGroup1
  TargetGroup2:
    Value: !Ref TargetGroup2
  ListenerArn:
    Value: !Ref Listener
  ListenerRule1Arn:
    Value: !Ref ListenerRule1
  ListenerRule2Arn:
    Value: !Ref ListenerRule2
  LoadBalancersAssociatedWithTargetGroup1:
    Description: LoadBalancers associated with TargetGroup
    Value: !Select 
      - '0'
      - !GetAtt 
        - TargetGroup1
        - LoadBalancerArns
  LoadBalancersAssociatedWithTargetGroup2:
    Description: LoadBalancers associated with TargetGroup
    Value: !Select 
      - '0'
      - !GetAtt 
        - TargetGroup2
        - LoadBalancerArns
  TargetGroupFullName1:
    Description: FullName of TargetGroup1
    Value: !GetAtt 
      - TargetGroup1
      - TargetGroupFullName
  TargetGroupFullName2:
    Description: FullName of TargetGroup2
    Value: !GetAtt 
      - TargetGroup2
      - TargetGroupFullName
```

#### JSON<a name="aws-resource-elasticloadbalancingv2-listenerrule--examples--Source_IP_Rule_Example--json"></a>

```
{
  "Parameters": {
    "CidrBlockForVPC" : {
      "Default" : "187.0.0.0/24",
      "Description" : "CidrBlockForVPC",
      "Type" : "String"
    },
    "CidrBlockForSubnet1" : {
      "Default" : "187.0.0.0/25",
      "Description" : "Cidr Block For Subnet1",
      "Type" : "String"
    },
    "CidrBlockForSubnet2" : {
      "Default" : "187.0.0.128/25",
      "Description" : "Cidr Block For Subnet2",
      "Type" : "String"
    },
    "AvailabilityZoneForSubnet1" : {
      "Default" : "us-east-1c",
      "Description" : "AvailabilityZone For Subnet1",
      "Type" : "String"
    },
    "AvailabilityZoneForSubnet2" : {
      "Default" : "us-east-1b",
      "Description" : "AvailabilityZone For Subnet2",
      "Type" : "String"
    }
  },
  "Resources": {
    "VPC": {
      "Type": "AWS::EC2::VPC",
      "Properties": {
        "CidrBlock": {"Ref" : "CidrBlockForVPC"}
      }
    },
    "Subnet1": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId" : { "Ref" : "VPC" },
        "AvailabilityZone": { "Ref": "AvailabilityZoneForSubnet1" },
        "CidrBlock": {"Ref" : "CidrBlockForSubnet1"}
      }
    },
    "Subnet2": {
      "Type": "AWS::EC2::Subnet",
      "Properties": {
        "VpcId" : { "Ref" : "VPC" },
        "AvailabilityZone": { "Ref": "AvailabilityZoneForSubnet2" },
        "CidrBlock": {"Ref" : "CidrBlockForSubnet2"}
      }
    },
    "LoadBalancer" : {
      "Type": "AWS::ElasticLoadBalancingV2::LoadBalancer",
      "Properties": {
        "Scheme" : "internal",
        "Subnets" : [ {"Ref": "Subnet1"}, {"Ref" : "Subnet2"} ]
      }
    },
    "TargetGroup1" : {
      "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties" : {
        "Port": 1000,
        "Protocol": "HTTP",
        "VpcId": { "Ref" : "VPC" }
      }
    },
    "TargetGroup2" : {
      "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
      "Properties" : {
        "Port": 2000,
        "Protocol": "HTTP",
        "VpcId": { "Ref" : "VPC" }
      }
    },
    "ListenerRule1": {
      "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
      "Properties": {
        "Actions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup1" }
        }],
        "Conditions": [{
          "Field": "source-ip",
          "SourceIpConfig": {
              "Values": ["172.0.0.0/8"]
          }
        }],
        "ListenerArn": { "Ref": "Listener" },
        "Priority": 1
      }
    },
    "ListenerRule2": {
      "Type": "AWS::ElasticLoadBalancingV2::ListenerRule",
      "Properties": {
        "Actions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup2" }
        }],
        "Conditions": [{
          "Field": "source-ip",
          "SourceIpConfig": {
              "Values": ["192.168.0.0/16"]
          }
        }],
        "ListenerArn": { "Ref": "Listener" },
        "Priority": 2
      }
    },
    "Listener": {
      "Type": "AWS::ElasticLoadBalancingV2::Listener",
      "Properties": {
        "DefaultActions": [{
          "Type": "forward",
          "TargetGroupArn": { "Ref": "TargetGroup1" }
        }],
        "LoadBalancerArn": { "Ref": "LoadBalancer" },
        "Port": "8000",
        "Protocol": "HTTP"
      }
    },
    "LoadBalancerAlarm": {
      "Type": "AWS::CloudWatch::Alarm",
      "Properties": {
        "Namespace": "AWS/ApplicationELB",
        "Dimensions": [
          {
            "Name": "LoadBalancer",
            "Value": {"Fn::GetAtt" : ["LoadBalancer", "LoadBalancerFullName"]}
          },
          {
            "Name": "TargetGroup",
            "Value": {"Fn::GetAtt" : ["TargetGroup1", "TargetGroupFullName"]}
          }
        ],
        "MetricName": "UnHealthyHostCount",
        "Period": 60,
        "Statistic": "Average",
        "ComparisonOperator": "GreaterThanThreshold",
        "Threshold": 0,
        "EvaluationPeriods": 1
      }
    }
  },
  "Outputs": {
    "LoadBalancer": {
      "Value": {
        "Ref": "LoadBalancer"
      }
    },
    "TargetGroup1": {
      "Value": {
        "Ref": "TargetGroup1"
      }
    },
    "TargetGroup2": {
      "Value": {
        "Ref": "TargetGroup2"
      }
    },
    "ListenerArn": {
      "Value": {
        "Ref": "Listener"
      }
    },
    "ListenerRule1Arn": {
      "Value": {
        "Ref": "ListenerRule1"
      }
    },
    "ListenerRule2Arn": {
      "Value": {
        "Ref": "ListenerRule2"
      }
    },
    "LoadBalancersAssociatedWithTargetGroup1" : {
      "Description" : "LoadBalancers associated with TargetGroup",
      "Value" : { "Fn::Select" : [ "0",
          { "Fn::GetAtt" : ["TargetGroup1", "LoadBalancerArns"] }
        ]
      }
    },
    "LoadBalancersAssociatedWithTargetGroup2" : {
      "Description" : "LoadBalancers associated with TargetGroup",
      "Value" : { "Fn::Select" : [ "0",
          { "Fn::GetAtt" : ["TargetGroup2", "LoadBalancerArns"] }
        ]
      }
    },
    "TargetGroupFullName1" : {
      "Description" : "FullName of TargetGroup1",
      "Value" : {"Fn::GetAtt" : ["TargetGroup1", "TargetGroupFullName"]}
    },
    "TargetGroupFullName2" : {
      "Description" : "FullName of TargetGroup2",
      "Value" : {"Fn::GetAtt" : ["TargetGroup2", "TargetGroupFullName"]}
    }
  }
}
```

## See also<a name="aws-resource-elasticloadbalancingv2-listenerrule--seealso"></a>
+  [CreateRule](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateRule.html) in the *Elastic Load Balancing API Reference \(version 2015\-12\-01\)* 
+  [Listener Rules](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-listeners.html#listener-rules) in the *User Guide for Application Load Balancers* 

