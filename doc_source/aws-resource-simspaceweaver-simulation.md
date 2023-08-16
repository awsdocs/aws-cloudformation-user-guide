# AWS::SimSpaceWeaver::Simulation<a name="aws-resource-simspaceweaver-simulation"></a>

Use the `AWS::SimSpaceWeaver::Simulation` resource to specify a simulation that AWS CloudFormation starts in the AWS Cloud, in your AWS account\. In the resource properties section of your template, provide the name of an existing IAM role configured with the proper permissions, and the name of an existing Amazon S3 bucket\. Your account must have permissions to read the Amazon S3 bucket\. The Amazon S3 bucket must contain a valid schema\. The schema must refer to simulation assets that are already uploaded to the AWS Cloud\. For more information, see the [ detailed tutorial](https://docs.aws.amazon.com/simspaceweaver/latest/userguide/getting-started_detailed.html) in the *AWSSimSpace Weaver User Guide*\. 

Specify a `SnapshotS3Location` to start a simulation from a snapshot instead of from a schema\. When you start a simulation from a snapshot, SimSpace Weaver initializes the entity data in the State Fabric with data saved in the snapshot, starts the spatial and service apps that were running when the snapshot was created, and restores the clock to the appropriate tick\. Your app zip files must be in the same location in Amazon S3 as they were in for the original simulation\. You must start any custom apps separately\. For more information about snapshots, see [Snapshots](https://docs.aws.amazon.com/simspaceweaver/latest/userguide/working-with_snapshots.html) in the *AWSSimSpace Weaver User Guide*\. 

## Syntax<a name="aws-resource-simspaceweaver-simulation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-simspaceweaver-simulation-syntax.json"></a>

```
{
  "Type" : "AWS::SimSpaceWeaver::Simulation",
  "Properties" : {
      "[MaximumDuration](#cfn-simspaceweaver-simulation-maximumduration)" : String,
      "[Name](#cfn-simspaceweaver-simulation-name)" : String,
      "[RoleArn](#cfn-simspaceweaver-simulation-rolearn)" : String,
      "[SchemaS3Location](#cfn-simspaceweaver-simulation-schemas3location)" : S3Location,
      "[SnapshotS3Location](#cfn-simspaceweaver-simulation-snapshots3location)" : S3Location
    }
}
```

### YAML<a name="aws-resource-simspaceweaver-simulation-syntax.yaml"></a>

```
Type: AWS::SimSpaceWeaver::Simulation
Properties: 
  [MaximumDuration](#cfn-simspaceweaver-simulation-maximumduration): String
  [Name](#cfn-simspaceweaver-simulation-name): String
  [RoleArn](#cfn-simspaceweaver-simulation-rolearn): String
  [SchemaS3Location](#cfn-simspaceweaver-simulation-schemas3location): 
    S3Location
  [SnapshotS3Location](#cfn-simspaceweaver-simulation-snapshots3location): 
    S3Location
```

## Properties<a name="aws-resource-simspaceweaver-simulation-properties"></a>

`MaximumDuration`  <a name="cfn-simspaceweaver-simulation-maximumduration"></a>
The maximum running time of the simulation, specified as a number of minutes \(m or M\), hours \(h or H\), or days \(d or D\)\. The simulation stops when it reaches this limit\. The maximum value is `14D`, or its equivalent in the other units\. The default value is `14D`\. A value equivalent to `0` makes the simulation immediately transition to `STOPPING` as soon as it reaches `STARTED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-simspaceweaver-simulation-name"></a>
The name of the simulation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-simspaceweaver-simulation-rolearn"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role that the simulation assumes to perform actions\. For more information about ARNs, see [Amazon Resource Names \(ARNs\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\. For more information about IAM roles, see [IAM roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html) in the *AWS Identity and Access Management User Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SchemaS3Location`  <a name="cfn-simspaceweaver-simulation-schemas3location"></a>
The location of the simulation schema in Amazon Simple Storage Service \(Amazon S3\)\. For more information about Amazon S3, see the [https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)\.   
Provide a `SchemaS3Location` to start your simulation from a schema\.  
If you provide a `SchemaS3Location` then you can't provide a `SnapshotS3Location`\.  
*Required*: No  
*Type*: [S3Location](aws-properties-simspaceweaver-simulation-s3location.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SnapshotS3Location`  <a name="cfn-simspaceweaver-simulation-snapshots3location"></a>
The location of the snapshot in Amazon Simple Storage Service \(Amazon S3\)\. For more information about Amazon S3, see the [https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)\.   
Provide a `SnapshotS3Location` to start your simulation from a snapshot\.  
If you provide a `SnapshotS3Location` then you can't provide a `SchemaS3Location`\.  
*Required*: No  
*Type*: [S3Location](aws-properties-simspaceweaver-simulation-s3location.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-simspaceweaver-simulation-return-values"></a>

### Ref<a name="aws-resource-simspaceweaver-simulation-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the name of the `Simulation`\. For example, `MyTestSimulation_22-12-15_12_00_00`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-simspaceweaver-simulation-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-simspaceweaver-simulation-return-values-fn--getatt-fn--getatt"></a>

`DescribePayload`  <a name="DescribePayload-fn::getatt"></a>
The JSON blob that the [DescribeSimulation](https://docs.aws.amazon.com/simspaceweaver/latest/APIReference/API_DescribeSimulation.html) action returns\.

## Examples<a name="aws-resource-simspaceweaver-simulation--examples"></a>



### Start a simulation<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation"></a>

The following example specifies a simulation resource in the AWS Cloud\.

#### JSON<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation--json"></a>

```
{
  "Description" : "Example - Start a simulation",
  "Resources" : {
    "MyTestSimulation" : {
      "Type" : "AWS::SimSpaceWeaver::Simulation",
      "Properties" : {
        "Name" : "MyTestSimulation",
        "RoleArn" : "arn:aws:iam::111122223333:role/my-test-simulation-app-role",
        "SchemaS3Location" : {
          "BucketName" : "MyTestSimulationBucket",
          "ObjectKey" : "MyTestSimulation-schema.yaml"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation--yaml"></a>

```
Description: "Example - Start a simulation"
Resources:
  MyTestSimulation:
    Type: "AWS::SimSpaceWeaver::Simulation"
    Properties:
      Name: "MyTestSimulation"
      RoleArn: "arn:aws:iam::111122223333:role/my-test-simulation-app-role"   
      SchemaS3Location:
        BucketName: "MyTestSimulationBucket"
        ObjectKey: "MyTestSimulation-schema.yaml"
```

### Start a simulation with assets that you created with the app SDK scripts \- version 1\.12\.x<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_assets_that_you_created_with_the_app_SDK_scripts_-_version_1.12.x"></a>

The following example specifies a simulation resource in the AWS Cloud with assets that you created with the app SDK scripts \(version 1\.12\.x\)\. The version 1\.12\.x scripts upload your app zips and schema to separate buckets for each project\. In this example, the `create-project` script used `--name MyTestSimulation` and uploaded to `us-west-2`\. For more information, see the [detailed tutorial](https://docs.aws.amazon.com/simspaceweaver/latest/userguide/getting-started_detailed.html) in the *AWS SimSpace Weaver User Guide*\.

#### JSON<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_assets_that_you_created_with_the_app_SDK_scripts_-_version_1.12.x--json"></a>

```
{
  "Description" : "Example - Start an app SDK project simulation v.1.12.x",
  "Resources" : {
    "MyTestSimulation" : {
      "Type" : "AWS::SimSpaceWeaver::Simulation",
      "Properties" : {
        "Name" : "MyTestSimulation_22-12-15_12_00_00",
        "RoleArn" : "arn:aws:iam::111122223333:role/weaver-MyTestSimulation-app-role",
        "SchemaS3Location" : {
          "BucketName" : "weaver-mytestsimulation-111122223333-schemas-us-west-2",
          "ObjectKey" : "MyTestSimulation-schema.yaml"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_assets_that_you_created_with_the_app_SDK_scripts_-_version_1.12.x--yaml"></a>

```
Description: "Example - Start an app SDK project simulation v.1.12.x"
Resources:
  MyTestSimulation:
    Type: "AWS::SimSpaceWeaver::Simulation"
    Properties:
      Name: "MyTestSimulation_22-12-15_12_00_00"
      RoleArn: "arn:aws:iam::111122223333:role/weaver-MyTestSimulation-app-role"   
      SchemaS3Location:
        BucketName: "weaver-mytestsimulation-111122223333-schemas-us-west-2"
        ObjectKey: "MyTestSimulation-schema.yaml"
```

### Start a simulation with assets that you created with the app SDK scripts \- version 1\.13\.x<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_assets_that_you_created_with_the_app_SDK_scripts_-_version_1.13.x"></a>

The following example specifies a simulation resource in the AWS Cloud with assets that you created with the app SDK scripts \(version 1\.13\.x\)\. The version 1\.13\.x scripts upload your project artifacts to a single bucket for each project\. In this example, the `create-project` script used `--name MyTestSimulation` and uploaded to `us-west-2`\. For more information, see the [detailed tutorial](https://docs.aws.amazon.com/simspaceweaver/latest/userguide/getting-started_detailed.html) in the *AWS SimSpace Weaver User Guide*\.

#### JSON<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_assets_that_you_created_with_the_app_SDK_scripts_-_version_1.13.x--json"></a>

```
{
  "Description" : "Example - Start an app SDK project simulation v.1.13.x",
  "Resources" : {
    "MyTestSimulation" : {
      "Type" : "AWS::SimSpaceWeaver::Simulation",
      "Properties" : {
        "Name" : "MyTestSimulation_22-12-15_12_00_00",
        "RoleArn" : "arn:aws:iam::111122223333:role/weaver-MyTestSimulation-app-role",
        "SchemaS3Location" : {
          "BucketName" : "weaver-mytestsimulation-111122223333-artifacts-us-west-2",
          "ObjectKey" : "MyTestSimulation-schema.yaml"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_assets_that_you_created_with_the_app_SDK_scripts_-_version_1.13.x--yaml"></a>

```
Description: "Example - Start an app SDK project simulation v.1.13.x"
Resources:
  MyTestSimulation:
    Type: "AWS::SimSpaceWeaver::Simulation"
    Properties:
      Name: "MyTestSimulation_22-12-15_12_00_00"
      RoleArn: "arn:aws:iam::111122223333:role/weaver-MyTestSimulation-app-role"   
      SchemaS3Location:
        BucketName: "weaver-mytestsimulation-111122223333-artifacts-us-west-2"
        ObjectKey: "MyTestSimulation-schema.yaml"
```

### Start a simulation with a 1 hour maximum duration<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_a_1_hour_maximum_duration"></a>

The following example adds a 1 hour `MaximumDuration` to the previous example\. This simulation will automatically stop after it reaches the maximum duration\.

#### JSON<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_a_1_hour_maximum_duration--json"></a>

```
{
  "Description" : "Example - Start a simulation with 1H maximum duration",
  "Resources" : {
    "MyTestSimulation" : {
      "Type" : "AWS::SimSpaceWeaver::Simulation",
      "Properties" : {
        "MaximumDuration" : "1H",
        "Name" : "MyTestSimulation_22-12-15_12_00_00",
        "RoleArn" : "arn:aws:iam::111122223333:role/weaver-MyTestSimulation-app-role",
        "SchemaS3Location" : {
          "BucketName" : "weaver-mytestsimulation-111122223333-artifacts-us-west-2",
          "ObjectKey" : "MyTestSimulation-schema.yaml"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_a_1_hour_maximum_duration--yaml"></a>

```
Description: "Example - Start a simulation with 1H maximum duration"
Resources:
  MyTestSimulation:
    Type: "AWS::SimSpaceWeaver::Simulation"
    Properties:
      MaximumDuration: "1H"
      Name: "MyTestSimulation_22-12-15_12_00_00"
      RoleArn: "arn:aws:iam::111122223333:role/weaver-MyTestSimulation-app-role"   
      SchemaS3Location:
        BucketName: "weaver-mytestsimulation-111122223333-artifacts-us-west-2"
        ObjectKey: "MyTestSimulation-schema.yaml"
```

### Start a simulation from a snapshot<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_from_a_snapshot"></a>

The following example starts a simulation from a snapshot instead of from a schema\. The snapshot in this example was created from the simulation in the previous example\. Note that the `MaximumDuration` setting isn't preserved in the snapshot\. This simulation is a new simulation with a new `MaximumDuration` of 2 days\.

We recommend that you make and use a copy of your original simulation's app role\. The original simulation's app role could be deleted if you delete that simulation's AWS CloudFormation stack\.

#### JSON<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_from_a_snapshot--json"></a>

```
{
  "Description" : "Example - Start a simulation from a snapshot",
  "Resources" : {
    "MyTestSimulation" : {
      "Type" : "AWS::SimSpaceWeaver::Simulation",
      "Properties" : {
        "MaximumDuration" : "2D",
        "Name" : "MyTestSimulation_from_snapshot",
        "RoleArn" : "arn:aws:iam::111122223333:role/weaver-MyTestSimulation-app-role-copy",
        "SnapshotS3Location" : {
          "BucketName" : "weaver-mytestsimulation-111122223333-artifacts-us-west-2",
          "ObjectKey" : "snapshot/MyTestSimulation_22-12-15_12_00_00-230428-1207-13.zip"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_from_a_snapshot--yaml"></a>

```
Description: "Example - Start a simulation from a snapshot"
Resources:
  MyTestSimulation:
    Type: "AWS::SimSpaceWeaver::Simulation"
    Properties:
      MaximumDuration: "2D"
      Name: "MyTestSimulation_from_snapshot"
      RoleArn: "arn:aws:iam::111122223333:role/weaver-MyTestSimulation-app-role-copy"   
      SnapshotS3Location:
        BucketName: "weaver-mytestsimulation-111122223333-artifacts-us-west-2"
        ObjectKey: "snapshot/MyTestSimulation_22-12-15_12_00_00-230428-1207-13.zip"
```