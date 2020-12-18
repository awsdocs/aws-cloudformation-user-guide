# AWS::CodeDeployBlueGreen transform<a name="transform-aws-codedeploybluegreen"></a>

Use the `AWS::CodeDeployBlueGreen` transform to enable ECS blue/green deployments through CodeDeploy on your stack\. For more information, including a usage example, see [Perform ECS blue/green deployments through CodeDeploy using AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/blue-green.html)\.

## Usage<a name="aws-codedeploybluegreen-usage"></a>

Use the `AWS::CodeDeployBlueGreen` transform at the top level of the template\. You cannot use `AWS::CodeDeployBlueGreen` as a transform embedded in any other template section\.

The value for the transform declaration must be a literal string\. You cannot use a parameter or function to specify a transform value\. 

### Syntax at the top level of a template<a name="aws-codedeploybluegreen-syntax-top-level-overview"></a>

To include `AWS::CodeDeployBlueGreen` in the `Transform` section, use the following syntax\.

#### JSON<a name="aws-codedeploybluegreen-syntax-top-level.json"></a>

```
1. {
2.   "Transform": "AWS::CodeDeployBlueGreen",
3.     . . .
4. }
```

#### YAML<a name="aws-codedeploybluegreen-syntax-top-level.yaml"></a>

```
1. "Transform": [
2.     "AWS::CodeDeployBlueGreen"
3. ],
```

## Parameters<a name="aws-v-transform-parameters"></a>

The `AWS::CodeDeployBlueGreen` transform does not accept any parameters\. 

## Remarks<a name="aws-codedeploybluegreen-transform-remarks"></a>

For general considerations about using macros, see [Considerations when creating AWS CloudFormation macro definitions](template-macros.md#template-macros-considerations)

## Example<a name="aws-codedeploybluegreen-transform-examples"></a>

For a complete usage example, see [Perform ECS blue/green deployments through CodeDeploy using AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/blue-green.html)\.