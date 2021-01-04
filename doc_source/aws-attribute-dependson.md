# DependsOn attribute<a name="aws-attribute-dependson"></a>

With the `DependsOn` attribute you can specify that the creation of a specific resource follows another\. When you add a `DependsOn` attribute to a resource, that resource is created only after the creation of the resource specified in the `DependsOn` attribute\.

**Important**  
Dependent stacks also have implicit dependencies in the form of target properties `!Ref` and `!GetAtt`\. For example, if the properties of resource A use a `!Ref` to resource B, the following rule apply:  
Resource B is created before resource A\.
Resource A is deleted before resource B\.
Resource B is updated before resource A\.

You can use the `DependsOn` attribute with any resource\. Here are some typical uses:
+ Determine when a wait condition goes into effect\. For more information, see [Creating wait conditions in a template](using-cfn-waitcondition.md)\.
+ Declare dependencies for resources that must be created or deleted in a specific order\. For example, you must explicitly declare dependencies on gateway attachments for some resources in a VPC\. For more information, see [When a DependsOn attribute is required](#gatewayattachment)\.
+ Override default parallelism when creating, updating, or deleting resources\. AWS CloudFormation creates, updates, and deletes resources in parallel to the extent possible\. It automatically determines which resources in a template can be parallelized and which have dependencies that require other operations to finish first\. You can use `DependsOn` to explicitly specify dependencies, which overrides the default parallelism and directs CloudFormation to operate on those resources in a specified order\.

**Note**  
During a stack update, resources that depend on updated resources are updated automatically\. AWS CloudFormation makes no changes to the automatically\-updated resources, but, if a stack policy is associated with these resources, your account must have the permissions to update them\.

## Syntax<a name="w7739ab1c33c23c15c13"></a>

The `DependsOn` attribute can take a single string or list of strings\.

```
"DependsOn" : [ String, ... ]
```

## Example<a name="w7739ab1c33c23c15c15"></a>

The following template contains an [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource with a `DependsOn` attribute that specifies myDB, an [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)\. When AWS CloudFormation creates this stack, it first creates myDB, then creates Ec2Instance\.

### JSON<a name="aws-attribute-dependson-example-1.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion" : "2010-09-09",
 3.     "Mappings" : {
 4.         "RegionMap" : {
 5.             "us-east-1" : { 
 6.                 "AMI" : "ami-0ff8a91507f77f867" 
 7.             },
 8.             "us-west-1" : { 
 9.                 "AMI" : "ami-0bdb828fd58c52235" 
10.             },
11.             "eu-west-1" : { 
12.                 "AMI" : "ami-047bb4163c506cd98" 
13.             },
14.             "ap-northeast-1" : { 
15.                 "AMI" : "ami-06cd52961ce9f0d85" 
16.             },
17.             "ap-southeast-1" : { 
18.                 "AMI" : "ami-08569b978cc4dfa10" 
19.             }
20.         }
21.     },
22.     "Resources" : {
23.         "Ec2Instance" : {
24.             "Type" : "AWS::EC2::Instance",
25.             "Properties" : {
26.                 "ImageId": {
27.                     "Fn::FindInMap": [
28.                         "RegionMap",
29.                         {
30.                             "Ref": "AWS::Region"
31.                         },
32.                         "AMI"
33.                     ]
34.                 }
35.             },
36.             "DependsOn" : "myDB"
37.         },
38.         "myDB" : {
39.             "Type" : "AWS::RDS::DBInstance",
40.             "Properties" : {
41.                "AllocatedStorage" : "5",
42.                "DBInstanceClass" : "db.t2.small",
43.                "Engine" : "MySQL",
44.                "EngineVersion" : "5.5",
45.                "MasterUsername" : "MyName",
46.                "MasterUserPassword" : "MyPassword"
47.             }
48.         }
49.     }
50. }
```

### YAML<a name="aws-attribute-dependson-example-1.yaml"></a>

```
 1. AWSTemplateFormatVersion: '2010-09-09'
 2. Mappings:
 3.   RegionMap:
 4.     us-east-1:
 5.       AMI: ami-0ff8a91507f77f867
 6.     us-west-1:
 7.       AMI: ami-0bdb828fd58c52235
 8.     eu-west-1:
 9.       AMI: ami-047bb4163c506cd98
10.     ap-northeast-1:
11.       AMI: ami-06cd52961ce9f0d85
12.     ap-southeast-1:
13.       AMI: ami-08569b978cc4dfa10
14. Resources:
15.   Ec2Instance:
16.     Type: AWS::EC2::Instance
17.     Properties:
18.       ImageId:
19.         Fn::FindInMap:
20.         - RegionMap
21.         - Ref: AWS::Region
22.         - AMI
23.     DependsOn: myDB
24.   myDB:
25.     Type: AWS::RDS::DBInstance
26.     Properties:
27.       AllocatedStorage: '5'
28.       DBInstanceClass: db.t2.small
29.       Engine: MySQL
30.       EngineVersion: '5.5'
31.       MasterUsername: MyName
32.       MasterUserPassword: MyPassword
```

## When a DependsOn attribute is required<a name="gatewayattachment"></a>

VPC\-gateway attachment

Some resources in a VPC require a gateway \(either an Internet or VPN gateway\)\. If your AWS CloudFormation template defines a VPC, a gateway, and a gateway attachment, any resources that require the gateway are dependent on the gateway attachment\. For example, an Amazon EC2 instance with a public IP address is dependent on the VPC\-gateway attachment if the `VPC` and `InternetGateway` resources are also declared in the same template\.

Currently, the following resources depend on a VPC\-gateway attachment when they have an associated public IP address and are in a VPC:
+ Auto Scaling groups
+ Amazon EC2 instances
+ Elastic Load Balancing load balancers
+ Elastic IP addresses
+ Amazon RDS database instances
+ Amazon VPC routes that include the Internet gateway

A VPN gateway route propagation depends on a VPC\-gateway attachment when you have a VPN gateway\.

The following snippet shows a sample gateway attachment and an Amazon EC2 instance that depends on a gateway attachment:

### JSON<a name="aws-attribute-dependson-example-2.json"></a>

```
"GatewayToInternet" : {
  "Type" : "AWS::EC2::VPCGatewayAttachment",
  "Properties" : {
    "VpcId" : { 
      "Ref" : "VPC" 
    },
    "InternetGatewayId" : { 
      "Ref" : "InternetGateway" 
    }
  }
},

"EC2Host" : {
  "Type" : "AWS::EC2::Instance",
  "DependsOn" : "GatewayToInternet",
  "Properties" : {
    "InstanceType" : { 
      "Ref" : "EC2InstanceType" 
    },
    "KeyName"  : { 
      "Ref" : "KeyName" 
    },
    "ImageId": {
      "Fn::FindInMap": [
        "AWSRegionArch2AMI",
        {
          "Ref": "AWS::Region"
        },
        {
          "Fn::FindInMap": [
            "AWSInstanceType2Arch",
            {
              "Ref": "EC2InstanceType"
            },
            "Arch"
          ]
        }
      ]
    },
    "NetworkInterfaces" : [
      {
        "GroupSet" : [
          { 
            "Ref" : "EC2SecurityGroup" 
          }
        ],
        "AssociatePublicIpAddress" : "true",
        "DeviceIndex" : "0",
        "DeleteOnTermination" : "true",
        "SubnetId" : { 
          "Ref" : "PublicSubnet" 
        }
      }
    ]
  }
}
```

### YAML<a name="aws-attribute-dependson-example-2.yaml"></a>

```
GatewayToInternet:
  Type: AWS::EC2::VPCGatewayAttachment
  Properties:
    VpcId:
      Ref: VPC
    InternetGatewayId:
      Ref: InternetGateway
EC2Host:
  Type: AWS::EC2::Instance
  DependsOn: GatewayToInternet
  Properties:
    InstanceType:
      Ref: EC2InstanceType
    KeyName:
      Ref: KeyName
    ImageId:
      Fn::FindInMap:
      - AWSRegionArch2AMI
      - Ref: AWS::Region
      - Fn::FindInMap:
        - AWSInstanceType2Arch
        - Ref: EC2InstanceType
        - Arch
    NetworkInterfaces:
    - GroupSet:
      - Ref: EC2SecurityGroup
      AssociatePublicIpAddress: 'true'
      DeviceIndex: '0'
      DeleteOnTermination: 'true'
      SubnetId:
        Ref: PublicSubnet
```

### Amazon ECS service and Auto Scaling group<a name="w7739ab1c33c23c15c17c18"></a>

When you use Auto Scaling or Amazon Elastic Compute Cloud \(Amazon EC2\) to create container instances for an Amazon ECS cluster, the Amazon ECS service resource must have a dependency on the Auto Scaling group or Amazon EC2 instances, as shown in the following snippet\. That way the container instances are available and associated with the Amazon ECS cluster before AWS CloudFormation creates the Amazon ECS service\.

#### JSON<a name="aws-attribute-dependson-example-3.json"></a>

```
"service": {
  "Type": "AWS::ECS::Service",
  "DependsOn": [
    "ECSAutoScalingGroup"
  ],
  "Properties" : {
    "Cluster": {
      "Ref": "ECSCluster"
    },
    "DesiredCount": "1",
    "LoadBalancers": [
      {
        "ContainerName": "simple-app",
        "ContainerPort": "80",
        "LoadBalancerName" : { 
          "Ref" : "EcsElasticLoadBalancer" 
        }
      }
    ],
    "Role" : {
      "Ref":"ECSServiceRole"
    },
    "TaskDefinition" : {
      "Ref":"taskdefinition"
    }
  }
}
```

#### YAML<a name="aws-attribute-dependson-example-3.yaml"></a>

```
service:
  Type: AWS::ECS::Service
  DependsOn:
  - ECSAutoScalingGroup
  Properties:
    Cluster:
      Ref: ECSCluster
    DesiredCount: 1
    LoadBalancers:
    - ContainerName: simple-app
      ContainerPort: 80
      LoadBalancerName:
        Ref: EcsElasticLoadBalancer
    Role:
      Ref: ECSServiceRole
    TaskDefinition:
      Ref: taskdefinition
```

### IAM role policy<a name="w7739ab1c33c23c15c17c20"></a>

Resources that make additional calls to AWS require a service role, which permits a service to make calls to AWS on your behalf\. For example, the `AWS::CodeDeploy::DeploymentGroup` resource requires a service role so that CodeDeploy has permissions to deploy applications to your instances\. When you have a single template that defines a service role, the role's policy \(by using the `AWS::IAM::Policy` or `AWS::IAM::ManagedPolicy` resource\), and a resource that uses the role, add a dependency so that the resource depends on the role's policy\. This dependency ensures that the policy is available throughout the resource's lifecycle\.

For example, imagine that you have a template with a deployment group resource, a service role, and the role's policy\. When you create a stack, AWS CloudFormation won't create the deployment group until it creates the role's policy\. Without the dependency, AWS CloudFormation can create the deployment group resource before it creates the role's policy\. If that happens, the deployment group will fail to create because of insufficient permissions\.

If the role has an embedded policy, don't specify a dependency\. AWS CloudFormation creates the role and its policy at the same time\.