# UpdatePolicy attribute<a name="aws-attribute-updatepolicy"></a>

Use the `UpdatePolicy` attribute to specify how AWS CloudFormation handles updates to the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup), [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html), or [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-alias.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-alias.html) resources\.
+ For `AWS::AutoScaling::AutoScalingGroup` resources, AWS CloudFormation invokes one of three update policies depending on the type of change you make or whether a scheduled action is associated with the Auto Scaling group\.
  + The `AutoScalingReplacingUpdate` and `AutoScalingRollingUpdate` policies apply *only* when you do one or more of the following:
    + Change the Auto Scaling group's `[AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html)`\.
    + Change the Auto Scaling group's `VPCZoneIdentifier` property
    + Change the Auto Scaling group's `LaunchTemplate` property
    + Update an Auto Scaling group that contains instances that don't match the current `LaunchConfiguration`\.

    If both the `AutoScalingReplacingUpdate` and `AutoScalingRollingUpdate` policies are specified, setting the `WillReplace` property to `true` gives `AutoScalingReplacingUpdate` precedence\.
  + The `AutoScalingScheduledAction` policy applies when you update a stack that includes an Auto Scaling group with an associated scheduled action\.
+ For `AWS::ElastiCache::ReplicationGroup` resources, AWS CloudFormation can modify a replication group's shards by adding or removing shards, rather than replacing the entire resource\. For more information, see [UseOnlineResharding policy](#cfn-attributes-updatepolicy-useonlineresharding)\. 
+ For `AWS::Elasticsearch::Domain` resources, AWS CloudFormation can upgrade an Amazon ES domain to a new version of Elasticsearch without replacing the entire resource\. For more information, see [EnableVersionUpgrade policy](#cfn-attributes-updatepolicy-upgradeelasticsearchdomain)\.
+ For `AWS::Lambda::Alias` resources, AWS CloudFormation performs an CodeDeploy deployment when the version changes on the alias\. For more information, see [CodeDeployLambdaAliasUpdate policy](#cfn-attributes-updatepolicy-codedeploylambdaaliasupdate)\.

## AutoScalingReplacingUpdate policy<a name="cfn-attributes-updatepolicy-replacingupdate"></a>

To specify how AWS CloudFormation handles replacement updates for an Auto Scaling group, use the `AutoScalingReplacingUpdate` policy\. This policy enables you to specify whether AWS CloudFormation replaces an Auto Scaling group with a new one or replaces only the instances in the Auto Scaling group\.

**Important**  
Before attempting an update, ensure that you have sufficient Amazon EC2 capacity for both your old and new Auto Scaling groups\.

### Syntax<a name="cfn-attributes-updatepolicy-replacingupdate-syntax"></a>

#### JSON<a name="aws-attribute-updatepolicy-replacingupdate-syntax.json"></a>

```
"UpdatePolicy" : {
  "AutoScalingReplacingUpdate" : {
    "WillReplace" : Boolean
  }
}
```

#### YAML<a name="aws-attribute-updatepolicy-replacingupdate-syntax.yaml"></a>

```
UpdatePolicy:
  AutoScalingReplacingUpdate:
    WillReplace: Boolean
```

### Properties<a name="cfn-attributes-updatepolicy-replacingupdate-properties"></a>

`WillReplace`  <a name="cfn-attributes-updatepolicy-replacingupdate-willreplace"></a>
Specifies whether an Auto Scaling group and the instances it contains are replaced during an update\. During replacement, AWS CloudFormation retains the old group until it finishes creating the new one\. If the update fails, AWS CloudFormation can roll back to the old Auto Scaling group and delete the new Auto Scaling group\.  
While AWS CloudFormation creates the new group, it doesn't detach or attach any instances\. After successfully creating the new Auto Scaling group, AWS CloudFormation deletes the old Auto Scaling group during the cleanup process\.  
When you set the `WillReplace` parameter, remember to specify a matching `[CreationPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-creationpolicy.html)`\. If the minimum number of instances \(specified by the `MinSuccessfulInstancesPercent` property\) don't signal success within the `Timeout` period \(specified in the `CreationPolicy` policy\), the replacement update fails and AWS CloudFormation rolls back to the old Auto Scaling group\.  
*Type*: Boolean  
*Required*: No

## AutoScalingRollingUpdate policy<a name="cfn-attributes-updatepolicy-rollingupdate"></a>

To specify how AWS CloudFormation handles rolling updates for an Auto Scaling group, use the `AutoScalingRollingUpdate` policy\. Rolling updates enable you to specify whether AWS CloudFormation updates instances that are in an Auto Scaling group in batches or all at once\.

**Important**  
During a rolling update, some Auto Scaling processes might make changes to the Auto Scaling group before AWS CloudFormation completes the rolling update\. These changes might cause the rolling update to fail\. To prevent Auto Scaling from running processes during a rolling update, use the `SuspendProcesses` property\. For more information, see [What are some recommended best practices for performing Auto Scaling group rolling updates?](https://aws.amazon.com/premiumsupport/knowledge-center/auto-scaling-group-rolling-updates/)

Be aware that, during stack update rollback operations, CloudFormation uses the `UpdatePolicy` configuration specified in the template before the current stack update operation\. For example, suppose you have updated the `MaxBatchSize` in your stack template's `UpdatePolicy` from 1 to 10\. You then perform a stack update, and that update fails and CloudFormation initiates an update rollback operation\. In such a case, CloudFormation will use 1 as the maximum batch size, rather than 10\. For this reason, we recommend you make changes to the `UpdatePolicy` configuration in a stack update separate from, and prior to, any updates to the `AWS::AutoScaling::AutoScalingGroup` resource that are likely to trigger rolling updates\.

### Syntax<a name="cfn-attributes-updatepolicy-replacingupdate-syntax"></a>

#### JSON<a name="aws-attribute-updatepolicy-rollingupdate-syntax.json"></a>

```
"UpdatePolicy" : {
  "AutoScalingRollingUpdate" : {
    "MaxBatchSize" : Integer,
    "MinInstancesInService" : Integer,
    "MinSuccessfulInstancesPercent" : Integer,
    "PauseTime" : String,
    "SuspendProcesses" : [ List of processes ],
    "WaitOnResourceSignals" : Boolean
  }
}
```

#### YAML<a name="aws-attribute-updatepolicy-rollingupdate-syntax.yaml"></a>

```
UpdatePolicy:
  AutoScalingRollingUpdate:
    MaxBatchSize: Integer
    MinInstancesInService: Integer
    MinSuccessfulInstancesPercent: Integer
    PauseTime: String
    SuspendProcesses:
      - List of processes
    WaitOnResourceSignals: Boolean
```

### Properties<a name="aws-attribute-updatepolicy-rollingupdate-properties"></a>

`MaxBatchSize`  <a name="cfn-attributes-updatepolicy-rollingupdate-maxbatchsize"></a>
Specifies the maximum number of instances that AWS CloudFormation updates\.  
*Default*: `1`  
*Type*: Integer  
*Required*: No

`MinInstancesInService`  <a name="cfn-attributes-updatepolicy-rollingupdate-mininstancesinservice"></a>
Specifies the minimum number of instances that must be in service within the Auto Scaling group while AWS CloudFormation updates old instances\. This value must be less than the [MaxSize](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#cfn-as-group-maxsize) of the Auto Scaling group\.  
*Default*: `0`  
*Type*: Integer  
*Required*: No

`MinSuccessfulInstancesPercent`  <a name="cfn-attributes-updatepolicy-rollingupdate-minsuccessfulinstancespercent"></a>
Specifies the percentage of instances in an Auto Scaling rolling update that must signal success for an update to succeed\. You can specify a value from `0` to `100`\. AWS CloudFormation rounds to the nearest tenth of a percent\. For example, if you update five instances with a minimum successful percentage of `50`, three instances must signal success\.  
If an instance doesn't send a signal within the time specified in the `PauseTime` property, AWS CloudFormation assumes that the instance wasn't updated\.  
If you specify this property, you must also enable the `WaitOnResourceSignals` and `PauseTime` properties\.  
The `MinSuccessfulInstancesPercent` parameter applies only to instances only for signaling purpose\. To specify the number of instances in your autoscaling group, see the `MinSize`, `MaxSize`, and `DesiredCapacity` properties fo the [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) resource\.  
*Default*: `100`  
*Type*: Integer  
*Required*: No

`PauseTime`  <a name="cfn-attributes-updatepolicy-rollingupdate-pausetime"></a>
The amount of time that AWS CloudFormation pauses after making a change to a batch of instances to give those instances time to start software applications\. For example, you might need to specify `PauseTime` when scaling up the number of instances in an Auto Scaling group\.   
If you enable the `WaitOnResourceSignals` property, `PauseTime` is the amount of time that AWS CloudFormation should wait for the Auto Scaling group to receive the required number of valid signals from added or replaced instances\. If the `PauseTime` is exceeded before the Auto Scaling group receives the required number of signals, the update fails\. For best results, specify a time period that gives your applications sufficient time to get started\. If the update needs to be rolled back, a short `PauseTime` can cause the rollback to fail\.  
Specify `PauseTime` in the [ISO8601 duration format](http://en.wikipedia.org/wiki/ISO_8601#Durations) \(in the format `PT#H#M#S`, where each *\#* is the number of hours, minutes, and seconds, respectively\)\. The maximum `PauseTime` is one hour \(`PT1H`\)\.  
*Default*: `PT0S` \(zero seconds\)\. If the `WaitOnResourceSignals` property is set to `true`, the default is `PT5M`\.  
*Type*: String  
*Required*: No

`SuspendProcesses`  <a name="cfn-attributes-updatepolicy-rollingupdate-suspendprocesses"></a>
Specifies the Auto Scaling processes to suspend during a stack update\. Suspending processes prevents Auto Scaling from interfering with a stack update\. For example, you can suspend alarming so that Amazon EC2 Auto Scaling doesn't execute scaling policies associated with an alarm\. For valid values, see the `ScalingProcesses.member.N` parameter for the [SuspendProcesses](https://docs.aws.amazon.com/autoscaling/ec2/APIReference/API_SuspendProcesses.html) action in the *Amazon EC2 Auto Scaling API Reference*\.  
*Default*: Not specified  
*Type*: List of Auto Scaling processes  
*Required*: No

`WaitOnResourceSignals`  <a name="cfn-attributes-updatepolicy-rollingupdate-waitonresourcesignals"></a>
Specifies whether the Auto Scaling group waits on signals from new instances during an update\. Use this property to ensure that instances have completed installing and configuring applications before the Auto Scaling group update proceeds\. AWS CloudFormation suspends the update of an Auto Scaling group after new EC2 instances are launched into the group\. AWS CloudFormation must receive a signal from each new instance within the specified `PauseTime` before continuing the update\. To signal the Auto Scaling group, use the [cfn\-signal](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-signal.html) helper script or [https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_SignalResource.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_SignalResource.html) API\.  
To have instances wait for an Elastic Load Balancing health check before they signal success, add a health\-check verification by using the [cfn\-init](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-init.html) helper script\. For an example, see the `verify_instance_health` command in the [Auto Scaling rolling updates](https://github.com/awslabs/aws-cloudformation-templates/blob/master/aws/services/AutoScaling/AutoScalingRollingUpdates.yaml) sample template\.  
*Default*: `false`  
*Type*: Boolean  
*Required*: Conditional\. If you specify the `MinSuccessfulInstancesPercent` property, you must also enable the `WaitOnResourceSignals` and `PauseTime` properties\.

## AutoScalingScheduledAction policy<a name="cfn-attributes-updatepolicy-scheduledactions"></a>

To specify how AWS CloudFormation handles updates for the `MinSize`, `MaxSize`, and `DesiredCapacity` properties when the `AWS::AutoScaling::AutoScalingGroup` resource has an associated scheduled action, use the `AutoScalingScheduledAction` policy\.

With scheduled actions, the group size properties of an Auto Scaling group can change at any time\. When you update a stack with an Auto Scaling group and scheduled action, AWS CloudFormation always sets the group size property values of your Auto Scaling group to the values that are defined in the `AWS::AutoScaling::AutoScalingGroup` resource of your template, even if a scheduled action is in effect\. 

If you do not want AWS CloudFormation to change any of the group size property values when you have a scheduled action in effect, use the `AutoScalingScheduledAction` update policy and set `IgnoreUnmodifiedGroupSizeProperties` to `true` to prevent AWS CloudFormation from changing the `MinSize`, `MaxSize`, or `DesiredCapacity` properties unless you have modified these values in your template\.

### Syntax<a name="cfn-attributes-updatepolicy-scheduledactions-syntax"></a>

#### JSON<a name="aws-attribute-updatepolicy-scheduledactions-syntax.json"></a>

```
"UpdatePolicy" : {
  "AutoScalingScheduledAction" : {
    "IgnoreUnmodifiedGroupSizeProperties" : Boolean
  }
}
```

#### YAML<a name="aws-attribute-updatepolicy-scheduledactions-syntax.yaml"></a>

```
UpdatePolicy:
  AutoScalingScheduledAction:
    IgnoreUnmodifiedGroupSizeProperties: Boolean
```

### Properties<a name="cfn-attributes-updatepolicy-scheduledactions-properties"></a>

`IgnoreUnmodifiedGroupSizeProperties`  <a name="cfn-attributes-updatepolicy-scheduledactions-ignoreunmodifiedgroupsizeproperties"></a>
If `true`, AWS CloudFormation ignores differences in group size properties between your current Auto Scaling group and the Auto Scaling group described in the `AWS::AutoScaling::AutoScalingGroup` resource of your template during a stack update\. If you modify any of the group size property values in your template, AWS CloudFormation uses the modified values and updates your Auto Scaling group\.  
*Default*: `false`  
*Type*: Boolean  
*Required*: No

## UseOnlineResharding policy<a name="cfn-attributes-updatepolicy-useonlineresharding"></a>

To modify a replication group's shards by adding or removing shards, rather than replacing the entire [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html) resource, use the `UseOnlineResharding` update policy\.

If `UseOnlineResharding` is set to `true`, you can update the `NumNodeGroups` and `NodeGroupConfiguration` properties of the `AWS::ElastiCache::ReplicationGroup` resource, and CloudFormation will update those properties without interruption\. When `UseOnlineResharding` is set to `false`, or not specified, updating the `NumNodeGroups` and `NodeGroupConfiguration` properties results in CloudFormation replacing the entire `AWS::ElastiCache::ReplicationGroup` resource\.

The `UseOnlineResharding` update policy has no properties\.

Things to consider when setting the `UseOnlineResharding` update policy to `true`:
+ We strongly recommend you perform updates to the `NumNodeGroups` and `NodeGroupConfiguration` properties as the only updates in a given stack update operation\.

  Updating the node group configuration of a replication group is a resource\-intensive operation\. If a stack update fails, CloudFormation does not roll back changes to the node group configuration of a replication group\. However, CloudFormation will roll back any other properties that were changed as part of the failed update operation\.
+ Any node group updates require identifying all node groups\.

  If you specify the `NodeGroupConfiguration` property, you must also specify the NodeGroupId for each node group configuration in order for CloudFormation to update the number of nodes without interruption\. 

  When creating a replication group, if you do not specify an ID for each node group, ElastiCache automatically generates an ID for each node group\. To update the replication group without interruption, use the ElastiCache console \([https://console\.aws\.amazon\.com/elasticache/](https://console.aws.amazon.com/elasticache/)\) or [DescribeReplicationGroups](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_DescribeReplicationGroups.html) to retrieve the IDs for all node groups in the replication group\. Then specify the ID for each node group in your stack template before attempting to add or remove shards\.
**Note**  
As a best practice, when you create a replication group in a stack template, include an ID for each node group you specify\.

  In addition, updating the number of nodes without interruption requires that you have accurately specified the `PrimaryAvailabilityZone`, `ReplicaAvailabilityZones`, and `ReplicaCount` properties for each `NodeGroupConfiguration` as well\. Again, you can use the ElastiCache console \([https://console\.aws\.amazon\.com/elasticache/](https://console.aws.amazon.com/elasticache/)\) or [DescribeReplicationGroups](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_DescribeReplicationGroups.html) to retrieve the actual values for each node group and compare them to the values in your stack template\. You can update the property values of the node groups as a separate stack update, or as part of the same stack update that changes the number of node groups\.

  When you use an `UseOnlineResharding` update policy to update the number of node groups without interruption, ElastiCache evenly distributes the keyspaces between the specified number of slots\. This cannot be updated later\. Therefore, after updating the number of node groups in this way, you should remove the value specified for the `Slots` property of each `NodeGroupConfiguration` from the stack template, as it no longer reflects the actual values in each node group\.
+ Actual node group removal results may vary\.

  When you specify a `NumNodeGroups` value that is less than the current number of node groups, CloudFormation instructs ElastiCache to remove as many node groups as necessary to reach the specified number of nodes\. However, ElastiCache may not always be able to remove the desired number of node groups\. In the event ElastiCache cannot remove the desired number of node groups, CloudFormation generates a stack event alerting you to this\. In cases where ElastiCache cannot remove *any* node groups, the CloudFormation resource update fails\.

For more information on modifying replication groups, see [ModifyReplicationGroupShardConfiguration](https://docs.aws.amazon.com/AmazonElastiCache/latest/APIReference/API_ModifyReplicationGroupShardConfiguration.html) in the *Amazon ElastiCache API Reference*\.

### Syntax<a name="cfn-attributes-updatepolicy-useonlineresharding-syntax"></a>

#### JSON<a name="cfn-attributes-updatepolicy-useonlineresharding-syntax.json"></a>

```
"UpdatePolicy" : {
  "UseOnlineResharding" : Boolean
}
```

#### YAML<a name="cfn-attributes-updatepolicy-useonlineresharding-syntax.yaml"></a>

```
UpdatePolicy:
  UseOnlineResharding: Boolean
```

## EnableVersionUpgrade policy<a name="cfn-attributes-updatepolicy-upgradeelasticsearchdomain"></a>

To upgrade an Amazon ES domain to a new version of Elasticsearch rather than replacing the entire [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html) resource, use the `EnableVersionUpgrade` update policy\.

If `EnableVersionUpgrade` is set to `true`, you can update the `ElasticsearchVersion` property of the `AWS::Elasticsearch::Domain` resource, and CloudFormation will update that property without interruption\. When `EnableVersionUpgrade` is set to `false`, or not specified, updating the `ElasticsearchVersion` property results in CloudFormation replacing the entire `AWS::Elasticsearch::Domain` resource\.

The `EnableVersionUpgrade` update policy has no properties\.

For more information about upgrading Amazon ES domains, see [UpgradeElasticsearchDomain](https://docs.aws.amazon.com/elasticsearch-service/latest/developerguide/es-configuration-api.html#es-configuration-api-actions-upgrade-domain) in the Amazon Elasticsearch Service Developer Guide\.

### Syntax<a name="cfn-attributes-updatepolicy-upgradeelasticsearchdomain-syntax"></a>

#### JSON<a name="cfn-attributes-updatepolicy-upgradeelasticsearchdomain-syntax.json"></a>

```
"UpdatePolicy" : {
  "EnableVersionUpgrade" : Boolean
}
```

#### YAML<a name="cfn-attributes-updatepolicy-upgradeelasticsearchdomain-syntax.yaml"></a>

```
UpdatePolicy:
  EnableVersionUpgrade: Boolean
```

## CodeDeployLambdaAliasUpdate policy<a name="cfn-attributes-updatepolicy-codedeploylambdaaliasupdate"></a>

To perform an CodeDeploy deployment when the version changes on an `AWS::Lambda::Alias` resource, use the `CodeDeployLambdaAliasUpdate` update policy\.

### Syntax<a name="cfn-attributes-updatepolicy-codedeploylambdaaliasupdate-syntax"></a>

#### JSON<a name="aws-attribute-updatepolicy-codedeploylambdaaliasupdate-syntax.json"></a>

```
"UpdatePolicy" : {
  "CodeDeployLambdaAliasUpdate" : {
    "AfterAllowTrafficHook" : String,
    "ApplicationName" : String,
    "BeforeAllowTrafficHook" : String,
    "DeploymentGroupName" : String
  }
}
```

#### YAML<a name="aws-attribute-updatepolicy-codedeploylambdaaliasupdate-syntax.yaml"></a>

```
UpdatePolicy:
  CodeDeployLambdaAliasUpdate:
    AfterAllowTrafficHook: String
    ApplicationName: String
    BeforeAllowTrafficHook: String
    DeploymentGroupName: String
```

### Properties<a name="aws-attribute-updatepolicy-codedeploylambdaaliasupdate-properties"></a>

`AfterAllowTrafficHook`  <a name="cfn-attributes-updatepolicy-codedeploylambdaaliasupdate-afterallowtraffichook"></a>
The name of the Lambda function to run after traffic routing completes\.  
*Required: *No  
*Type: *String

`ApplicationName`  <a name="cfn-attributes-updatepolicy-codedeploylambdaaliasupdate-applicationname"></a>
The name of the CodeDeploy application\.  
*Required: *Yes  
*Type: *String

`BeforeAllowTrafficHook`  <a name="cfn-attributes-updatepolicy-codedeploylambdaaliasupdate-beforeallowtraffichook"></a>
The name of the Lambda function to run before traffic routing starts\.  
*Required: *No  
*Type: *String

`DeploymentGroupName`  <a name="cfn-attributes-updatepolicy-codedeploylambdaaliasupdate-deploymentgroupname"></a>
The name of the CodeDeploy deployment group\. This is where the traffic\-shifting policy is set\.  
*Required: *Yes  
*Type: *String

For an example that specifies the `UpdatePolicy` attribute for an `AWS::Lambda::Alias` resource, see [Lambda alias update policy](#aws-resource-lambda-alias-example)\.

## Examples<a name="aws-attribute-updatepolicy-examples"></a>

The following examples show how to add an update policy to an Auto Scaling group and how to maintain availability when updating metadata\.

### Add an UpdatePolicy to an Auto Scaling group<a name="w7739ab1c33c23c23c19b4"></a>

The following example shows how to add an update policy\. During an update, the Auto Scaling group updates instances in batches of two and keeps a minimum of one instance in service\. Because the `WaitOnResourceSignals` flag is set, the Auto Scaling group waits for new instances that are added to the group\. The new instances must signal the Auto Scaling group before it updates the next batch of instances\.

#### JSON<a name="attribute-updatepolicy-example-1.json"></a>

```
"ASG" : {
   "Type" : "AWS::AutoScaling::AutoScalingGroup",
   "Properties" : {
      "AvailabilityZones" : [
         "us-east-1a",
         "us-east-1b"
      ],
      "DesiredCapacity" : "1",
      "LaunchConfigurationName" : {
         "Ref" : "LaunchConfig"
      },
      "MaxSize" : "4",
      "MinSize" : "1"
   },
   "UpdatePolicy" : {
      "AutoScalingScheduledAction" : {
         "IgnoreUnmodifiedGroupSizeProperties" : "true"
      },
      "AutoScalingRollingUpdate" : {
         "MinInstancesInService" : "1",
         "MaxBatchSize" : "2",
         "WaitOnResourceSignals" : "true",
         "PauseTime" : "PT10M"
      }
   }
 },
"ScheduledAction" : {
   "Type" : "AWS::AutoScaling::ScheduledAction",
   "Properties" : {
      "AutoScalingGroupName" : {
         "Ref" : "ASG"
      },
      "DesiredCapacity" : "2",
      "StartTime" : "2017-06-02T20 : 00 : 00Z"
   }
}
```

#### YAML<a name="attribute-updatepolicy-example-1.yaml"></a>

```
ASG:
  Type: 'AWS::AutoScaling::AutoScalingGroup'
  Properties:
    AvailabilityZones:
    - us-east-1a
    - us-east-1b
    DesiredCapacity: '1'
    LaunchConfigurationName:
      Ref: LaunchConfig
    MaxSize: '4'
    MinSize: '1'
  UpdatePolicy:
    AutoScalingScheduledAction:
      IgnoreUnmodifiedGroupSizeProperties: 'true'
    AutoScalingRollingUpdate:
      MinInstancesInService: '1'
      MaxBatchSize: '2'
      WaitOnResourceSignals: 'true'
      PauseTime: PT10M
ScheduledAction:
  Type: 'AWS::AutoScaling::ScheduledAction'
  Properties:
    AutoScalingGroupName:
      Ref: ASG
    DesiredCapacity: '2'
    StartTime: '2017-06-02T20 : 00 : 00Z'
```

### AutoScalingReplacingUpdate policy<a name="w7739ab1c33c23c23c19b6"></a>

The following example declares a policy that forces an associated Auto Scaling group to be replaced during an update\. For the update to succeed, a percentage of instances \(specified by the `MinSuccessfulPercentParameter` parameter\) must signal success within the `Timeout` period\.

#### JSON<a name="attribute-updatepolicy-example-2.json"></a>

```
"UpdatePolicy" : {
  "AutoScalingReplacingUpdate" : {
    "WillReplace" : "true"
  }
},
"CreationPolicy" : {
  "ResourceSignal" : {
    "Count" : { "Ref" : "ResourceSignalsOnCreate"},
    "Timeout" : "PT10M"
  },
  "AutoScalingCreationPolicy" : {
    "MinSuccessfulInstancesPercent" : { "Ref" : "MinSuccessfulPercentParameter" }
  }
}
```

#### YAML<a name="attribute-updatepolicy-example-2.yaml"></a>

```
UpdatePolicy:
  AutoScalingReplacingUpdate:
    WillReplace: 'true'
CreationPolicy:
  ResourceSignal:
    Count: !Ref 'ResourceSignalsOnCreate'
    Timeout: PT10M
  AutoScalingCreationPolicy:
    MinSuccessfulInstancesPercent: !Ref 'MinSuccessfulPercentParameter'
```

### Maintain availability when updating the metadata for the cfn\-init helper script<a name="w7739ab1c33c23c23c19b8"></a>

When you install software applications on your instances, you might use the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-init.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-init.html) metadata key and the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-init.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-init.html) helper script to bootstrap the instances in your Auto Scaling group\. AWS CloudFormation installs the packages, runs the commands, and performs other bootstrapping actions described in the metadata\.

When you update only the metadata \(for example, when updating a package to another version\), you can use the `[cfn\-hup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-hup.html)` helper daemon to detect and apply the updates\. However, the `cfn-hup` daemon runs independently on each instance\. If the daemon happens to runs at the same time on all instances, your application or service might be unavailable during the update\. To guarantee availability, you can force a rolling update so that AWS CloudFormation updates your instances one batch at a time\.

**Important**  
Forcing a rolling update requires AWS CloudFormation to create a new instance and then delete the old one\. Any information stored on the old instance is lost\.

To force a rolling update, change the logical ID of the launch configuration resource, and then update the stack and any references pointing to the original logic ID \(such as the associated Auto Scaling group\)\. AWS CloudFormation triggers a rolling update on the Auto Scaling group, replacing all instances\.

### Original template<a name="w7739ab1c33c23c23c19c10"></a>

```
"LaunchConfig": {
  "Type" : "AWS::AutoScaling::LaunchConfiguration",
  "Metadata" : {
    "Comment" : "Install a simple PHP application",
    "AWS::CloudFormation::Init" : {
    ...
    }
  }
}
```

### Updated logical ID<a name="w7739ab1c33c23c23c19c12"></a>

```
"LaunchConfigUpdateRubygemsPkg": {
  "Type" : "AWS::AutoScaling::LaunchConfiguration",
  "Metadata" : {
    "Comment" : "Install a simple PHP application",
    "AWS::CloudFormation::Init" : {
    ...
    }
  }
}
```

### Lambda alias update policy<a name="aws-resource-lambda-alias-example"></a>

The following example specifies the `UpdatePolicy` attribute for an `AWS::Lambda::Alias` resource\. All the details for the deployment are defined by the application and deployment group that are passed into the policy\.

#### JSON<a name="aws-attribute-updatepolicy-codedeploylambda.json"></a>

```
"Alias": {
  "Type": "AWS::Lambda::Alias",
  "Properties": {
    "FunctionName": {
      "Ref": "LambdaFunction"
    },
    "FunctionVersion": {
      "Fn::GetAtt": [
        "FunctionVersionTwo",
        "Version"
      ]
    },
    "Name": "MyAlias"
  },
  "UpdatePolicy": {
    "CodeDeployLambdaAliasUpdate": {
      "ApplicationName": {
        "Ref": "CodeDeployApplication"
      },
      "DeploymentGroupName": {
        "Ref": "CodeDeployDeploymentGroup"
      },
      "BeforeAllowTrafficHook": {
        "Ref": "PreHookLambdaFunction"
      },
      "AfterAllowTrafficHook": {
        "Ref": "PreHookLambdaFunction"
      }
    }
  }
}
```

#### YAML<a name="aws-attribute-updatepolicy-codedeploylambda-example.yaml"></a>

```
Alias:
  Type: 'AWS::Lambda::Alias'
  Properties:
    FunctionName: !Ref LambdaFunction
    FunctionVersion: !GetAtt FunctionVersionTwo.Version
    Name: MyAlias
  UpdatePolicy:
    CodeDeployLambdaAliasUpdate:
      ApplicationName: !Ref CodeDeployApplication
      DeploymentGroupName: !Ref CodeDeployDeploymentGroup
      BeforeAllowTrafficHook: !Ref PreHookLambdaFunction
      AfterAllowTrafficHook: !Ref PreHookLambdaFunction
```