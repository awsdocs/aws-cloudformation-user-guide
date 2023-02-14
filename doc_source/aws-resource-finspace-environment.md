# AWS::FinSpace::Environment<a name="aws-resource-finspace-environment"></a>

 The `AWS::FinSpace::Environment` resource represents an Amazon FinSpace environment\. 

## Syntax<a name="aws-resource-finspace-environment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-finspace-environment-syntax.json"></a>

```
{
  "Type" : "AWS::FinSpace::Environment",
  "Properties" : {
      "[DataBundles](#cfn-finspace-environment-databundles)" : [ String, ... ],
      "[Description](#cfn-finspace-environment-description)" : String,
      "[FederationMode](#cfn-finspace-environment-federationmode)" : String,
      "[FederationParameters](#cfn-finspace-environment-federationparameters)" : FederationParameters,
      "[KmsKeyId](#cfn-finspace-environment-kmskeyid)" : String,
      "[Name](#cfn-finspace-environment-name)" : String,
      "[SuperuserParameters](#cfn-finspace-environment-superuserparameters)" : SuperuserParameters
    }
}
```

### YAML<a name="aws-resource-finspace-environment-syntax.yaml"></a>

```
Type: AWS::FinSpace::Environment
Properties: 
  [DataBundles](#cfn-finspace-environment-databundles): 
    - String
  [Description](#cfn-finspace-environment-description): String
  [FederationMode](#cfn-finspace-environment-federationmode): String
  [FederationParameters](#cfn-finspace-environment-federationparameters): 
    FederationParameters
  [KmsKeyId](#cfn-finspace-environment-kmskeyid): String
  [Name](#cfn-finspace-environment-name): String
  [SuperuserParameters](#cfn-finspace-environment-superuserparameters): 
    SuperuserParameters
```

## Properties<a name="aws-resource-finspace-environment-properties"></a>

`DataBundles`  <a name="cfn-finspace-environment-databundles"></a>
The list of Amazon Resource Names \(ARN\) of the data bundles to install\. Currently supported data bundle ARNs:  
+  `arn:aws:finspace:${Region}::data-bundle/capital-markets-sample` \- Contains sample Capital Markets datasets, categories and controlled vocabularies\.
+  `arn:aws:finspace:${Region}::data-bundle/taq` \(default\) \- Contains trades and quotes data in addition to sample Capital Markets data\.
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-finspace-environment-description"></a>
The description of the FinSpace environment\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Pattern*: `^[a-zA-Z0-9. ]{1,1000}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FederationMode`  <a name="cfn-finspace-environment-federationmode"></a>
The authentication mode for the environment\.  
*Required*: No  
*Type*: String  
*Allowed values*: `FEDERATED | LOCAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FederationParameters`  <a name="cfn-finspace-environment-federationparameters"></a>
Configuration information when authentication mode is FEDERATED\.  
*Required*: No  
*Type*: [FederationParameters](aws-properties-finspace-environment-federationparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-finspace-environment-kmskeyid"></a>
The KMS key id used to encrypt in the FinSpace environment\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1000`  
*Pattern*: `^[a-zA-Z-0-9-:\/]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-finspace-environment-name"></a>
The name of the FinSpace environment\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9]+[a-zA-Z0-9-]*[a-zA-Z0-9]$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SuperuserParameters`  <a name="cfn-finspace-environment-superuserparameters"></a>
Configuration information for the superuser\.  
*Required*: No  
*Type*: [SuperuserParameters](aws-properties-finspace-environment-superuserparameters.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-finspace-environment-return-values"></a>

### Ref<a name="aws-resource-finspace-environment-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

 `{ "Ref": "myEnvironment" }` 

For the Amazon FinSpace environment group `myEnvironment`, `Ref` returns the name of the environment\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-finspace-environment-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-finspace-environment-return-values-fn--getatt-fn--getatt"></a>

`AwsAccountId`  <a name="AwsAccountId-fn::getatt"></a>
The ID of the AWS account in which the FinSpace environment is created\. 

`DedicatedServiceAccountId`  <a name="DedicatedServiceAccountId-fn::getatt"></a>
The AWS account ID of the dedicated service account associated with your FinSpace environment\. 

`EnvironmentArn`  <a name="EnvironmentArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of your FinSpace environment\. 

`EnvironmentId`  <a name="EnvironmentId-fn::getatt"></a>
The identifier of the FinSpace environment\. 

`EnvironmentUrl`  <a name="EnvironmentUrl-fn::getatt"></a>
The sign\-in url for the web application of your FinSpace environment\. 

`SageMakerStudioDomainUrl`  <a name="SageMakerStudioDomainUrl-fn::getatt"></a>
The url of the integrated FinSpace notebook environment in your web application\. 

`Status`  <a name="Status-fn::getatt"></a>
The current status of creation of the FinSpace environment\. 

## Examples<a name="aws-resource-finspace-environment--examples"></a>



### Creating environments<a name="aws-resource-finspace-environment--examples--Creating_environments"></a>

The following examples create new FinSpace environments\.

#### YAML<a name="aws-resource-finspace-environment--examples--Creating_environments--yaml"></a>

```
Resources:
  FinSpaceEnvironment:
    Type: 'AWS::FinSpace::Environment'
    Properties:
        Name: MyEnvironment
        KmsKeyId: arn:aws:kms:us-east-1:123456789012:key/44efed01-30d0-4b39-80e7-165d5ed34524
        FederationMode: LOCAL
```

#### JSON<a name="aws-resource-finspace-environment--examples--Creating_environments--json"></a>

```
{
   "Resources": {
      "FinSpaceEnvironment": {
         "Type": "AWS::FinSpace::Environment",
         "Properties": {
            "Name": "MyEnvironment",
            "KmsKeyId": "arn:aws:kms:us-east-1:123456789012:key/44efed01-30d0-4b39-80e7-165d5ed34524",
            "FederationMode": "LOCAL"
         }
      }
   }
}
```