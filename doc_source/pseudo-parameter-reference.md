# Pseudo parameters reference<a name="pseudo-parameter-reference"></a>

Pseudo parameters are parameters that are predefined by AWS CloudFormation\. You do not declare them in your template\. Use them the same way as you would a parameter, as the argument for the `Ref` function\.

## Example<a name="w7739ab1c33c33b5"></a>

The following snippet assigns the value of the `AWS::Region` pseudo parameter to an output value:

### JSON<a name="pseudo-parameter-reference-example-1.json"></a>

```
"Outputs" : {
   "MyStacksRegion" : { "Value" : { "Ref" : "AWS::Region" } }
}
```

### YAML<a name="pseudo-parameter-reference-example-1.yaml"></a>

```
Outputs:
  MyStacksRegion:
    Value: !Ref "AWS::Region"
```

## AWS::AccountId<a name="cfn-pseudo-param-accountid"></a>

Returns the AWS account ID of the account in which the stack is being created, such as `123456789012`\.

## AWS::NotificationARNs<a name="cfn-pseudo-param-notificationarns"></a>

Returns the list of notification Amazon Resource Names \(ARNs\) for the current stack\.

To get a single ARN from the list, use [Fn::Select](intrinsic-function-reference-select.md)\.

### JSON<a name="pseudo-parameter-reference-example-2.json"></a>

```
"myASGrpOne" : {
   "Type" : "AWS::AutoScaling::AutoScalingGroup",
   "Version" : "2009-05-15",
   "Properties" : {
      "AvailabilityZones" : [ "us-east-1a" ],
      "LaunchConfigurationName" : { "Ref" : "MyLaunchConfiguration" },
      "MinSize" : "0",
      "MaxSize" : "0",
      "NotificationConfigurations" : [{
         "TopicARN" : { "Fn::Select" : [ "0", { "Ref" : "AWS::NotificationARNs" } ] },
         "NotificationTypes" : [ "autoscaling:EC2_INSTANCE_LAUNCH", "autoscaling:EC2_INSTANCE_LAUNCH_ERROR" ]
      }]
   }
}
```

### YAML<a name="pseudo-parameter-reference-example-2.yaml"></a>

```
myASGrpOne:
  Type: AWS::AutoScaling::AutoScalingGroup
  Version: '2009-05-15'
  Properties:
    AvailabilityZones:
    - "us-east-1a"
    LaunchConfigurationName:
      Ref: MyLaunchConfiguration
    MinSize: '0'
    MaxSize: '0'
    NotificationConfigurations:
    - TopicARN:
        Fn::Select:
        - '0'
        - Ref: AWS::NotificationARNs
      NotificationTypes:
      - autoscaling:EC2_INSTANCE_LAUNCH
      - autoscaling:EC2_INSTANCE_LAUNCH_ERROR
```

## AWS::NoValue<a name="cfn-pseudo-param-novalue"></a>

Removes the corresponding resource property when specified as a return value in the `Fn::If` intrinsic function\.

For example, you can use the `AWS::NoValue` parameter when you want to use a snapshot for an Amazon RDS DB instance only if a snapshot ID is provided\. If the `UseDBSnapshot` condition evaluates to true, AWS CloudFormation uses the `DBSnapshotName` parameter value for the `DBSnapshotIdentifier` property\. If the condition evaluates to false, AWS CloudFormation removes the `DBSnapshotIdentifier` property\.

### JSON<a name="pseudo-parameter-reference-example-3.json"></a>

```
"MyDB" : {
  "Type" : "AWS::RDS::DBInstance",
  "Properties" : {
    "AllocatedStorage" : "5",
    "DBInstanceClass" : "db.t2.small",
    "Engine" : "MySQL",
    "EngineVersion" : "5.5",
    "MasterUsername" : { "Ref" : "DBUser" },
    "MasterUserPassword" : { "Ref" : "DBPassword" },
    "DBParameterGroupName" : { "Ref" : "MyRDSParamGroup" },
    "DBSnapshotIdentifier" : {
      "Fn::If" : [
        "UseDBSnapshot",
        {"Ref" : "DBSnapshotName"},
        {"Ref" : "AWS::NoValue"}
      ]
    }
  }
}
```

### YAML<a name="pseudo-parameter-reference-example-3.yaml"></a>

```
MyDB:
  Type: AWS::RDS::DBInstance
  Properties:
    AllocatedStorage: '5'
    DBInstanceClass: db.t2.small
    Engine: MySQL
    EngineVersion: '5.5'
    MasterUsername:
      Ref: DBUser
    MasterUserPassword:
      Ref: DBPassword
    DBParameterGroupName:
      Ref: MyRDSParamGroup
    DBSnapshotIdentifier:
      Fn::If:
      - UseDBSnapshot
      - Ref: DBSnapshotName
      - Ref: AWS::NoValue
```

## AWS::Partition<a name="cfn-pseudo-param-partition"></a>

Returns the partition that the resource is in\. For standard AWS regions, the partition is `aws`\. For resources in other partitions, the partition is `aws-`*partitionname*\. For example, the partition for resources in the China \(Beijing and Ningxia\) region is `aws-cn` and the partition for resources in the AWS GovCloud \(US\-West\) region is `aws-us-gov`\.

## AWS::Region<a name="cfn-pseudo-param-region"></a>

Returns a string representing the AWS Region in which the encompassing resource is being created, such as `us-west-2`\.

## AWS::StackId<a name="cfn-pseudo-param-stackid"></a>

Returns the ID of the stack as specified with the `aws cloudformation create-stack` command, such as `arn:aws:cloudformation:us-west-2:123456789012:stack/teststack/51af3dc0-da77-11e4-872e-1234567db123`\.

## AWS::StackName<a name="cfn-pseudo-param-stackname"></a>

Returns the name of the stack as specified with the `aws cloudformation create-stack` command, such as `teststack`\.

## AWS::URLSuffix<a name="cfn-pseudo-param-urlsuffix"></a>

Returns the suffix for a domain\. The suffix is typically `amazonaws.com`, but might differ by region\. For example, the suffix for the China \(Beijing\) region is `amazonaws.com.cn`\.