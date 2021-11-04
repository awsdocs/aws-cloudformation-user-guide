# AWS::DataSync::LocationSMB MountOptions<a name="aws-properties-datasync-locationsmb-mountoptions"></a>

The mount options used by DataSync to access the SMB server\.

## Syntax<a name="aws-properties-datasync-locationsmb-mountoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationsmb-mountoptions-syntax.json"></a>

```
{
  "[Version](#cfn-datasync-locationsmb-mountoptions-version)" : String
}
```

### YAML<a name="aws-properties-datasync-locationsmb-mountoptions-syntax.yaml"></a>

```
  [Version](#cfn-datasync-locationsmb-mountoptions-version): String
```

## Properties<a name="aws-properties-datasync-locationsmb-mountoptions-properties"></a>

`Version`  <a name="cfn-datasync-locationsmb-mountoptions-version"></a>
The specific SMB version that you want DataSync to use to mount your SMB share\. If you don't specify a version, DataSync defaults to `AUTOMATIC`\. That is, DataSync automatically selects a version based on negotiation with the SMB server\.  
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | SMB2 | SMB3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)