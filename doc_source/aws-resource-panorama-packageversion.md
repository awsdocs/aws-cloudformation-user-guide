# AWS::Panorama::PackageVersion<a name="aws-resource-panorama-packageversion"></a>

Registers a package version\.

## Syntax<a name="aws-resource-panorama-packageversion-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-panorama-packageversion-syntax.json"></a>

```
{
  "Type" : "AWS::Panorama::PackageVersion",
  "Properties" : {
      "[MarkLatest](#cfn-panorama-packageversion-marklatest)" : Boolean,
      "[OwnerAccount](#cfn-panorama-packageversion-owneraccount)" : String,
      "[PackageId](#cfn-panorama-packageversion-packageid)" : String,
      "[PackageVersion](#cfn-panorama-packageversion-packageversion)" : String,
      "[PatchVersion](#cfn-panorama-packageversion-patchversion)" : String,
      "[UpdatedLatestPatchVersion](#cfn-panorama-packageversion-updatedlatestpatchversion)" : String
    }
}
```

### YAML<a name="aws-resource-panorama-packageversion-syntax.yaml"></a>

```
Type: AWS::Panorama::PackageVersion
Properties: 
  [MarkLatest](#cfn-panorama-packageversion-marklatest): Boolean
  [OwnerAccount](#cfn-panorama-packageversion-owneraccount): String
  [PackageId](#cfn-panorama-packageversion-packageid): String
  [PackageVersion](#cfn-panorama-packageversion-packageversion): String
  [PatchVersion](#cfn-panorama-packageversion-patchversion): String
  [UpdatedLatestPatchVersion](#cfn-panorama-packageversion-updatedlatestpatchversion): String
```

## Properties<a name="aws-resource-panorama-packageversion-properties"></a>

`MarkLatest`  <a name="cfn-panorama-packageversion-marklatest"></a>
Whether to mark the new version as the latest version\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OwnerAccount`  <a name="cfn-panorama-packageversion-owneraccount"></a>
An owner account\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `12`  
*Pattern*: `[0-9a-z\_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PackageId`  <a name="cfn-panorama-packageversion-packageid"></a>
A package ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9\-\_\/]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PackageVersion`  <a name="cfn-panorama-packageversion-packageversion"></a>
A package version\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `([0-9]+)\.([0-9]+)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PatchVersion`  <a name="cfn-panorama-packageversion-patchversion"></a>
A patch version\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[a-z0-9]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UpdatedLatestPatchVersion`  <a name="cfn-panorama-packageversion-updatedlatestpatchversion"></a>
If the version was marked latest, the new version to maker as latest\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `[a-z0-9]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-panorama-packageversion-return-values"></a>

### Ref<a name="aws-resource-panorama-packageversion-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-panorama-packageversion-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-panorama-packageversion-return-values-fn--getatt-fn--getatt"></a>

`IsLatestPatch`  <a name="IsLatestPatch-fn::getatt"></a>
Whether the package version is the latest version\.

`PackageArn`  <a name="PackageArn-fn::getatt"></a>
The package version's ARN\.

`PackageName`  <a name="PackageName-fn::getatt"></a>
The package version's name\.

`RegisteredTime`  <a name="RegisteredTime-fn::getatt"></a>
The package version's registered time\.

`Status`  <a name="Status-fn::getatt"></a>
The package version's status\.

`StatusDescription`  <a name="StatusDescription-fn::getatt"></a>
The package version's status description\.