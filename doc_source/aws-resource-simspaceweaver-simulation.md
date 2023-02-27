# AWS::SimSpaceWeaver::Simulation<a name="aws-resource-simspaceweaver-simulation"></a>

Use the `AWS::SimSpaceWeaver::Simulation` resource to specify a simulation that AWS CloudFormation starts in the AWS Cloud, in your AWS account\. In the resource properties section of your template, provide the name of an existing IAM role configured with the proper permissions, and the name of an existing Amazon S3 bucket\. Your account must have permissions to read the Amazon S3 bucket\. The Amazon S3 bucket must contain a valid schema\. The schema must refer to simulation assets that are already uploaded to the AWS Cloud\. For more information, see the [ detailed tutorial](https://docs.aws.amazon.com/simspaceweaver/latest/userguide/getting-started_detailed.html) in the *AWS SimSpace Weaver User Guide*\.

## Syntax<a name="aws-resource-simspaceweaver-simulation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-simspaceweaver-simulation-syntax.json"></a>

```
{
  "Type" : "AWS::SimSpaceWeaver::Simulation",
  "Properties" : {
      "[Name](#cfn-simspaceweaver-simulation-name)" : String,
      "[RoleArn](#cfn-simspaceweaver-simulation-rolearn)" : String,
      "[SchemaS3Location](#cfn-simspaceweaver-simulation-schemas3location)" : S3Location
    }
}
```

### YAML<a name="aws-resource-simspaceweaver-simulation-syntax.yaml"></a>

```
Type: AWS::SimSpaceWeaver::Simulation
Properties: 
  [Name](#cfn-simspaceweaver-simulation-name): String
  [RoleArn](#cfn-simspaceweaver-simulation-rolearn): String
  [SchemaS3Location](#cfn-simspaceweaver-simulation-schemas3location): 
    S3Location
```

## Properties<a name="aws-resource-simspaceweaver-simulation-properties"></a>

`Name`  <a name="cfn-simspaceweaver-simulation-name"></a>
The name of the simulation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-simspaceweaver-simulation-rolearn"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role that the simulation assumes to perform actions\. For more information about ARNs, see [Amazon Resource Names \(ARNs\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\. For more information about IAM roles, see [IAM roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles.html) in the *AWS Identity and Access Management User Guide*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaS3Location`  <a name="cfn-simspaceweaver-simulation-schemas3location"></a>
The location of the simulation schema in Amazon Simple Storage Service \(Amazon S3\)\. For more information about Amazon S3, see the [https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)\.   
*Required*: No  
*Type*: [S3Location](aws-properties-simspaceweaver-simulation-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-simspaceweaver-simulation-return-values"></a>

### Ref<a name="aws-resource-simspaceweaver-simulation-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the `Simulation`\. For example, `MyTestSimulation_22-12-15_12_00_00`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-simspaceweaver-simulation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-simspaceweaver-simulation-return-values-fn--getatt-fn--getatt"></a>

`DescribePayload`  <a name="DescribePayload-fn::getatt"></a>
The JSON blob that the [DescribeSimulation](https://docs.aws.amazon.com/simspaceweaver/latest/APIReference/API_DescribeSimulation.html) action returns\.

## Examples<a name="aws-resource-simspaceweaver-simulation--examples"></a>



### Start a simulation<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation"></a>

The following example specifies a simulation resource in the AWS Cloud\.

#### JSON<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation--json"></a>

```
{
  "Description" : "SimSpace Weaver Simulation example 1",
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
Description: "SimSpace Weaver Simulation example 1"
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

### Start a simulation with assets that you created with the app SDK scripts<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_assets_that_you_created_with_the_app_SDK_scripts"></a>

The following example specifies a simulation resource in the AWS Cloud with assets that you created with the app SDK scripts\. In this example, the `create-project` script used `--name MyTestSimulation` and uploaded to `us-west-2`\. For more information, see the [detailed tutorial](https://docs.aws.amazon.com/simspaceweaver/latest/userguide/getting-started_detailed.html) in the *AWS SimSpace Weaver User Guide*\.

#### JSON<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_assets_that_you_created_with_the_app_SDK_scripts--json"></a>

```
{
  "Description" : "SimSpace Weaver Simulation example 2",
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

#### YAML<a name="aws-resource-simspaceweaver-simulation--examples--Start_a_simulation_with_assets_that_you_created_with_the_app_SDK_scripts--yaml"></a>

```
Description: "SimSpace Weaver Simulation example 2"
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