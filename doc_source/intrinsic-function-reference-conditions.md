# Condition functions<a name="intrinsic-function-reference-conditions"></a>

You can use intrinsic functions, such as `Fn::If`, `Fn::Equals`, and `Fn::Not`, to conditionally create stack resources\. These conditions are evaluated based on input parameters that you declare when you create or update a stack\. After you define all your conditions, you can associate them with resources or resource properties in the Resources and Outputs sections of a template\.

You define all conditions in the Conditions section of a template except for `Fn::If` conditions\. You can use the `Fn::If` condition in the metadata attribute, update policy attribute, and property values in the Resources section and Outputs sections of a template\.

You might use conditions when you want to reuse a template that can create resources in different contexts, such as a test environment versus a production environment\. In your template, you can add an `EnvironmentType` input parameter, which accepts either **prod** or **test** as inputs\. For the production environment, you might include Amazon EC2 instances with certain capabilities; however, for the test environment, you want to use less capabilities to save costs\. With conditions, you can define which resources are created and how they're configured for each environment type\.

For more information about the Conditions section, see [Conditions](conditions-section-structure.md)\.

**Note**  
You can only reference other conditions and values from the Parameters and Mappings sections of a template\. For example, you can reference a value from an input parameter, but you can't reference the logical ID of a resource in a condition\.

**Topics**
+ [Associating a condition](#associating-a-condition)
+ [Fn::And](#intrinsic-function-reference-conditions-and)
+ [Fn::Equals](#intrinsic-function-reference-conditions-equals)
+ [Fn::If](#intrinsic-function-reference-conditions-if)
+ [Fn::Not](#intrinsic-function-reference-conditions-not)
+ [Fn::Or](#intrinsic-function-reference-conditions-or)
+ [Supported functions](#w2ab1c33c28c21c29)
+ [Sample templates](conditions-sample-templates.md)
+ [Condition](intrinsic-function-reference-condition.md)

## Associating a condition<a name="associating-a-condition"></a>

To conditionally create resources, resource properties, or outputs, you must associate a condition with them\. Add the `Condition:` key and the logical ID of the condition as an attribute to associate a condition, as shown in the following snippet\. AWS CloudFormation creates the `NewVolume` resource only when the `CreateProdResources` condition evaluates to true\.

### JSON<a name="associating-conditions-example.json"></a>

```
"NewVolume" : {
  "Type" : "AWS::EC2::Volume",
  "Condition" : "CreateProdResources",
  "Properties" : {
     "Size" : "100",
     "AvailabilityZone" : { "Fn::GetAtt" : [ "EC2Instance", "AvailabilityZone" ]}
}
```

### YAML<a name="associating-conditions-example.yaml"></a>

```
NewVolume:
  Type: "AWS::EC2::Volume"
  Condition: CreateProdResources
  Properties: 
    Size: 100
    AvailabilityZone: !GetAtt EC2Instance.AvailabilityZone
```

### Fn::If<a name="fn-if-examples"></a>

For the `Fn::If` function, you only need to specify the condition name\. The following snippet shows how to use `Fn::If` to conditionally specify a resource property\. If the `CreateLargeSize` condition is true, CloudFormation sets the volume size to `100`\. If the condition is false, CloudFormation sets the volume size to `10`\.

#### JSON<a name="fn-if-examples.json"></a>

```
{
    "NewVolume": {
        "Type": "AWS::EC2::Volume",
        "Properties": {
            "Size": {
                "Fn::If": [
                    "CreateLargeSize",
                    "100",
                    "10"
                ]
            },
            "AvailabilityZone": {
                "Fn::GetAtt": [
                    "Ec2Instance",
                    "AvailabilityZone"
                ]
            }
        },
        "DeletionPolicy": "Snapshot"
    }
}
```

#### YAML<a name="fn-if-examples.yaml"></a>

```
NewVolume:
  Type: 'AWS::EC2::Volume'
  Properties:
    Size:
      'Fn::If':
        - CreateLargeSize
        - '100'
        - '10'
    AvailabilityZone:
      'Fn::GetAtt':
        - Ec2Instance
        - AvailabilityZone
  DeletionPolicy: Snapshot
```

#### Nested conditions<a name="nested-conditions"></a>

You can also use conditions inside other conditions\. The following snippet is from the `Conditions` section of a template\. The `MyAndCondition` condition includes the `SomeOtherCondition` condition:

##### JSON<a name="nested-conditions.json"></a>

```
"MyAndCondition": {
   "Fn::And": [
      {"Fn::Equals": ["sg-mysggroup", {"Ref": "ASecurityGroup"}]},
      {"Condition": "SomeOtherCondition"}
   ]
}
```

##### YAML<a name="nested-conditions.yaml"></a>

```
MyAndCondition: !And
  - !Equals ["sg-mysggroup", !Ref "ASecurityGroup"]
  - !Condition SomeOtherCondition
```

## Fn::And<a name="intrinsic-function-reference-conditions-and"></a>

Returns `true` if all the specified conditions evaluate to true, or returns `false` if any one of the conditions evaluates to false\. `Fn::And` acts as an AND operator\. The minimum number of conditions that you can include is 2, and the maximum is 10\.

### Declaration<a name="intrinsic-function-reference-conditions-and-syntax"></a>

#### JSON<a name="intrinsic-function-reference-conditions-and-syntax.json"></a>

```
"Fn::And": [{condition}, {...}]
```

#### YAML<a name="intrinsic-function-reference-conditions-and-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::And: [condition]
```

Syntax for the short form:

```
!And [condition]
```

### Parameters<a name="w2ab1c33c28c21c17b7"></a>

`condition`  <a name="fn-and-condition"></a>
A condition that evaluates to `true` or `false`\.

### Example<a name="w2ab1c33c28c21c17b9"></a>

The following `MyAndCondition` evaluates to true if the referenced security group name is equal to `sg-mysggroup` and if `SomeOtherCondition` evaluates to true:

#### JSON<a name="intrinsic-function-reference-conditions-and-example.json"></a>

```
"MyAndCondition": {
   "Fn::And": [
      {"Fn::Equals": ["sg-mysggroup", {"Ref": "ASecurityGroup"}]},
      {"Condition": "SomeOtherCondition"}
   ]
}
```

#### YAML<a name="intrinsic-function-reference-conditions-and-example.yaml"></a>

```
MyAndCondition: !And
  - !Equals ["sg-mysggroup", !Ref ASecurityGroup]
  - !Condition SomeOtherCondition
```

## Fn::Equals<a name="intrinsic-function-reference-conditions-equals"></a>

Compares if two values are equal\. Returns `true` if the two values are equal or `false` if they aren't\.

### Declaration<a name="intrinsic-function-reference-conditions-equals-syntax"></a>

#### JSON<a name="intrinsic-function-reference-conditions-equals-syntax.json"></a>

```
"Fn::Equals" : ["value_1", "value_2"]
```

#### YAML<a name="intrinsic-function-reference-conditions-equals-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Equals: [value_1, value_2]
```

Syntax for the short form:

```
!Equals [value_1, value_2]
```

### Parameters<a name="w2ab1c33c28c21c19b7"></a>

`value`  
A value of any type that you want to compare\.

### Example<a name="w2ab1c33c28c21c19b9"></a>

The following `UseProdCondition` condition evaluates to true if the value for the `EnvironmentType` parameter is equal to `prod`:

#### JSON<a name="intrinsic-function-reference-conditions-equals-example.json"></a>

```
"UseProdCondition" : {
   "Fn::Equals": [
      {"Ref": "EnvironmentType"},
      "prod"
   ]
}
```

#### YAML<a name="intrinsic-function-reference-conditions-equals-example.yaml"></a>

```
UseProdCondition:
  !Equals [!Ref EnvironmentType, prod]
```

## Fn::If<a name="intrinsic-function-reference-conditions-if"></a>

Returns one value if the specified condition evaluates to `true` and another value if the specified condition evaluates to `false`\. Currently, CloudFormation supports the `Fn::If` intrinsic function in the metadata attribute, update policy attribute, and property values in the Resources section and Outputs sections of a template\. You can use the `AWS::NoValue` pseudo parameter as a return value to remove the corresponding property\.

### Declaration<a name="intrinsic-function-reference-conditions-if-syntax"></a>

#### JSON<a name="intrinsic-function-reference-conditions-if-syntax.json"></a>

```
"Fn::If": [condition_name, value_if_true, value_if_false]
```

#### YAML<a name="intrinsic-function-reference-conditions-if-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::If: [condition_name, value_if_true, value_if_false]
```

Syntax for the short form:

```
!If [condition_name, value_if_true, value_if_false]
```

### Parameters<a name="w2ab1c33c28c21c23b7"></a>

`condition_name`  <a name="condition_name"></a>
A reference to a condition in the Conditions section\. Use the condition's name to reference it\.

`value_if_true`  <a name="value_if_true"></a>
A value to be returned if the specified condition evaluates to `true`\.

`value_if_false`  <a name="value_if_false"></a>
A value to be returned if the specified condition evaluates to `false`\.

### Examples<a name="w2ab1c33c28c21c23b9"></a>

To view additional samples, see [Sample templates](conditions-sample-templates.md)\.

#### Example 1<a name="w2ab1c33c28c21c23b9b5"></a>

The following snippet uses an `Fn::If` function in the `SecurityGroups` property for an Amazon EC2 resource\. If the `CreateNewSecurityGroup` condition evaluates to true, CloudFormation uses the referenced value of `NewSecurityGroup` to specify the `SecurityGroups` property; otherwise, CloudFormation uses the referenced value of `ExistingSecurityGroup`\.

##### JSON<a name="intrinsic-function-reference-conditions-if-example1.json"></a>

```
"SecurityGroups" : [{
  "Fn::If" : [
    "CreateNewSecurityGroup",
    {"Ref" : "NewSecurityGroup"},
    {"Ref" : "ExistingSecurityGroup"}
  ]
}]
```

##### YAML<a name="intrinsic-function-reference-conditions-if-example1.yaml"></a>

```
SecurityGroups:
  - !If [CreateNewSecurityGroup, !Ref NewSecurityGroup, !Ref ExistingSecurityGroup]
```

#### Example 2<a name="w2ab1c33c28c21c23b9b7"></a>

In the Output section of a template, you can use the `Fn::If` function to conditionally output information\. In the following snippet, if the `CreateNewSecurityGroup` condition evaluates to true, CloudFormation outputs the security group ID of the `NewSecurityGroup` resource\. If the condition is false, CloudFormation outputs the security group ID of the `ExistingSecurityGroup` resource\.

##### JSON<a name="intrinsic-function-reference-conditions-if-example2.json"></a>

```
"Outputs" : {
  "SecurityGroupId" : {
    "Description" : "Group ID of the security group used.",
    "Value" : {
      "Fn::If" : [
        "CreateNewSecurityGroup",
        {"Ref" : "NewSecurityGroup"},
        {"Ref" : "ExistingSecurityGroup"}
      ]
    }
  }
}
```

##### YAML<a name="intrinsic-function-reference-conditions-if-example2.yaml"></a>

```
Outputs:
  SecurityGroupId: 
    Description: Group ID of the security group used.
    Value: !If [CreateNewSecurityGroup, !Ref NewSecurityGroup, !Ref ExistingSecurityGroup]
```

#### Example 3<a name="w2ab1c33c28c21c23b9b9"></a>

The following snippet uses the `AWS::NoValue` pseudo parameter in an `Fn::If` function\. The condition uses a snapshot for an Amazon RDS DB instance only if a snapshot ID is provided\. If the `UseDBSnapshot` condition evaluates to true, CloudFormation uses the `DBSnapshotName` parameter value for the `DBSnapshotIdentifier` property\. If the condition evaluates to false, CloudFormation removes the `DBSnapshotIdentifier` property\.

##### JSON<a name="intrinsic-function-reference-conditions-if-example3.json"></a>

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

##### YAML<a name="intrinsic-function-reference-conditions-if-example3.yaml"></a>

```
MyDB:
  Type: "AWS::RDS::DBInstance"
  Properties: 
    AllocatedStorage: 5
    DBInstanceClass: db.t2.small
    Engine: MySQL
    EngineVersion: 5.5
    MasterUsername: !Ref DBUser
    MasterUserPassword: !Ref DBPassword
    DBParameterGroupName: !Ref MyRDSParamGroup
    DBSnapshotIdentifier:
      !If [UseDBSnapshot, !Ref DBSnapshotName, !Ref "AWS::NoValue"]
```

#### Example 4<a name="w2ab1c33c28c21c23b9c11"></a>

The following snippet provides an Auto Scaling update policy only if the `RollingUpdates` condition evaluates to true\. If the condition evaluates to false, CloudFormation removes the `AutoScalingRollingUpdate` update policy\.

##### JSON<a name="intrinsic-function-reference-conditions-if-example4.json"></a>

```
"UpdatePolicy": {
  "AutoScalingRollingUpdate": {
    "Fn::If": [
      "RollingUpdates",
      {
        "MaxBatchSize": "2",
        "MinInstancesInService": "2",
        "PauseTime": "PT0M30S"
      },
      {
        "Ref" : "AWS::NoValue"
      }
    ]
  }
}
```

##### YAML<a name="intrinsic-function-reference-conditions-if-example4.yaml"></a>

```
UpdatePolicy:
  AutoScalingRollingUpdate:
    !If 
      - RollingUpdates
      -
        MaxBatchSize: 2
        MinInstancesInService: 2
        PauseTime: PT0M30S
      - !Ref "AWS::NoValue"
```

## Fn::Not<a name="intrinsic-function-reference-conditions-not"></a>

Returns `true` for a condition that evaluates to `false` or returns `false` for a condition that evaluates to `true`\. `Fn::Not` acts as a NOT operator\.

### Declaration<a name="intrinsic-function-reference-conditions-not-syntax"></a>

#### JSON<a name="intrinsic-function-reference-conditions-not-syntax.json"></a>

```
"Fn::Not": [{condition}]
```

#### YAML<a name="intrinsic-function-reference-conditions-not-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Not: [condition]
```

Syntax for the short form:

```
!Not [condition]
```

### Parameters<a name="w2ab1c33c28c21c25b7"></a>

`condition`  <a name="condition"></a>
A condition such as `Fn::Equals` that evaluates to `true` or `false`\.

### Example<a name="w2ab1c33c28c21c25b9"></a>

The following `EnvCondition` condition evaluates to true if the value for the `EnvironmentType` parameter isn't equal to `prod`:

#### JSON<a name="intrinsic-function-reference-conditions-not-example.json"></a>

```
"MyNotCondition" : {
   "Fn::Not" : [{
      "Fn::Equals" : [
         {"Ref" : "EnvironmentType"},
         "prod"
      ]
   }]
}
```

#### YAML<a name="intrinsic-function-reference-conditions-not-example.yaml"></a>

```
MyNotCondition:
  !Not [!Equals [!Ref EnvironmentType, prod]]
```

## Fn::Or<a name="intrinsic-function-reference-conditions-or"></a>

Returns `true` if any one of the specified conditions evaluate to true, or returns `false` if all the conditions evaluates to false\. `Fn::Or` acts as an OR operator\. The minimum number of conditions that you can include is 2, and the maximum is 10\.

### Declaration<a name="intrinsic-function-reference-conditions-or-syntax"></a>

#### JSON<a name="intrinsic-function-reference-conditions-or-syntax.json"></a>

```
"Fn::Or": [{condition}, {...}]
```

#### YAML<a name="intrinsic-function-reference-conditions-or-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::Or: [condition, ...]
```

Syntax for the short form:

```
!Or [condition, ...]
```

### Parameters<a name="w2ab1c33c28c21c27b7"></a>

`condition`  
A condition that evaluates to `true` or `false`\.

### Example<a name="w2ab1c33c28c21c27b9"></a>

The following `MyOrCondition` evaluates to true if the referenced security group name is equal to `sg-mysggroup` or if `SomeOtherCondition` evaluates to true:

#### JSON<a name="intrinsic-function-reference-conditions-or-example.json"></a>

```
"MyOrCondition" : {
   "Fn::Or" : [
      {"Fn::Equals" : ["sg-mysggroup", {"Ref" : "ASecurityGroup"}]},
      {"Condition" : "SomeOtherCondition"}
   ]
}
```

#### YAML<a name="intrinsic-function-reference-conditions-or-example.yaml"></a>

```
MyOrCondition:
  !Or [!Equals [sg-mysggroup, !Ref ASecurityGroup], Condition: SomeOtherCondition]
```

## Supported functions<a name="w2ab1c33c28c21c29"></a>

You can use the following functions in the `Fn::If` condition:
+ `Fn::Base64`
+ `Fn::FindInMap`
+ `Fn::GetAtt`
+ `Fn::GetAZs`
+ `Fn::If`
+ `Fn::Join`
+ `Fn::Select`
+ `Fn::Sub`
+ `Ref`

You can use the following functions in all other condition functions, such as `Fn::Equals` and `Fn::Or`:
+ `Fn::FindInMap`
+ `Ref`
+ Other condition functions