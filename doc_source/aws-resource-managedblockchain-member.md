# AWS::ManagedBlockchain::Member<a name="aws-resource-managedblockchain-member"></a>

Creates a member within a Managed Blockchain network\.

Applies only to Hyperledger Fabric\.

## Syntax<a name="aws-resource-managedblockchain-member-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-managedblockchain-member-syntax.json"></a>

```
{
  "Type" : "AWS::ManagedBlockchain::Member",
  "Properties" : {
      "[InvitationId](#cfn-managedblockchain-member-invitationid)" : String,
      "[MemberConfiguration](#cfn-managedblockchain-member-memberconfiguration)" : MemberConfiguration,
      "[NetworkConfiguration](#cfn-managedblockchain-member-networkconfiguration)" : NetworkConfiguration,
      "[NetworkId](#cfn-managedblockchain-member-networkid)" : String
    }
}
```

### YAML<a name="aws-resource-managedblockchain-member-syntax.yaml"></a>

```
Type: AWS::ManagedBlockchain::Member
Properties: 
  [InvitationId](#cfn-managedblockchain-member-invitationid): String
  [MemberConfiguration](#cfn-managedblockchain-member-memberconfiguration): 
    MemberConfiguration
  [NetworkConfiguration](#cfn-managedblockchain-member-networkconfiguration): 
    NetworkConfiguration
  [NetworkId](#cfn-managedblockchain-member-networkid): String
```

## Properties<a name="aws-resource-managedblockchain-member-properties"></a>

`InvitationId`  <a name="cfn-managedblockchain-member-invitationid"></a>
The unique identifier of the invitation to join the network sent to the account that creates the member\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MemberConfiguration`  <a name="cfn-managedblockchain-member-memberconfiguration"></a>
Configuration properties of the member\.  
*Required*: Yes  
*Type*: [MemberConfiguration](aws-properties-managedblockchain-member-memberconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkConfiguration`  <a name="cfn-managedblockchain-member-networkconfiguration"></a>
Configuration properties of the network to which the member belongs\.  
*Required*: No  
*Type*: [NetworkConfiguration](aws-properties-managedblockchain-member-networkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkId`  <a name="cfn-managedblockchain-member-networkid"></a>
The unique identifier of the network to which the member belongs\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-managedblockchain-member-return-values"></a>

### Ref<a name="aws-resource-managedblockchain-member-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the member ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-managedblockchain-member-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-managedblockchain-member-return-values-fn--getatt-fn--getatt"></a>

`MemberId`  <a name="MemberId-fn::getatt"></a>
The unique identifier of the member\.

`NetworkId`  <a name="NetworkId-fn::getatt"></a>
The unique identifier of the network to which the member belongs\.

## Examples<a name="aws-resource-managedblockchain-member--examples"></a>



### Create a new Managed Blockchain network for Hyperledger Fabric and the first member<a name="aws-resource-managedblockchain-member--examples--Create_a_new_Managed_Blockchain_network_for_Hyperledger_Fabric_and_the_first_member"></a>

When you create the first member in a Managed Blockchain network, you also specify parameters to create the network\.

#### YAML<a name="aws-resource-managedblockchain-member--examples--Create_a_new_Managed_Blockchain_network_for_Hyperledger_Fabric_and_the_first_member--yaml"></a>

```
Description: "Basic initial member template"
Parameters:
  MemberName:
    Type: String
  MemberDescription:
    Type: String
  MemberAdminUsername:
    Type: String
  MemberAdminPassword:
    Type: String
  NetworkName:
    Type: String
  NetworkDescription:
    Type: String
  Edition:
    Type: String
  ThresholdPercentage:
    Type: Number
  ThresholdComparator:
    Type: String
  ProposalDurationInHours:
    Type: Number

Resources:
  Member:
    Type: "AWS::ManagedBlockchain::Member"
    Properties:
      NetworkConfiguration:
        Name: !Ref NetworkName
        Description: !Ref NetworkDescription
        Framework: "HYPERLEDGER_FABRIC"
        FrameworkVersion: "1.2"
        NetworkFrameworkConfiguration:
          NetworkFabricConfiguration:
            Edition: !Ref Edition
        VotingPolicy:
          ApprovalThresholdPolicy:
            ThresholdPercentage: !Ref ThresholdPercentage
            ProposalDurationInHours: !Ref ProposalDurationInHours
            ThresholdComparator: !Ref ThresholdComparator
      MemberConfiguration:
        Name: !Ref MemberName
        Description: !Ref MemberDescription
        MemberFrameworkConfiguration:
          MemberFabricConfiguration:
            AdminUsername: !Ref MemberAdminUsername
            AdminPassword: !Ref MemberAdminPassword
```

#### JSON<a name="aws-resource-managedblockchain-member--examples--Create_a_new_Managed_Blockchain_network_for_Hyperledger_Fabric_and_the_first_member--json"></a>

```
{
  "Description": "Basic initial member template",
  "Parameters": {
    "MemberName": {
      "Type": "String"
    },
    "MemberDescription": {
      "Type": "String"
    },
    "MemberAdminUsername": {
      "Type": "String"
    },
    "MemberAdminPassword": {
      "Type": "String"
    },
    "NetworkName": {
      "Type": "String"
    },
    "NetworkDescription": {
      "Type": "String"
    },
    "Edition": {
      "Type": "String"
    },
    "ThresholdPercentage": {
      "Type": "Number"
    },
    "ThresholdComparator": {
      "Type": "String"
    },
    "ProposalDurationInHours": {
      "Type": "Number"
    }
  },
  "Resources": {
    "Member": {
      "Type": "AWS::ManagedBlockchain::Member",
      "Properties": {
        "NetworkConfiguration": {
          "Name": "NetworkName",
          "Description": "NetworkDescription",
          "Framework": "HYPERLEDGER_FABRIC",
          "FrameworkVersion": "1.2",
          "NetworkFrameworkConfiguration": {
            "NetworkFabricConfiguration": {
              "Edition": "Edition"
            }
          },
          "VotingPolicy": {
            "ApprovalThresholdPolicy": {
              "ThresholdPercentage": "ThresholdPercentage",
              "ProposalDurationInHours": "ProposalDurationInHours",
              "ThresholdComparator": "ThresholdComparator"
            }
          }
        },
        "MemberConfiguration": {
          "Name": "MemberName",
          "Description": "MemberDescription",
          "MemberFrameworkConfiguration": {
            "MemberFabricConfiguration": {
              "AdminUsername": "MemberAdminUsername",
              "AdminPassword": "MemberAdminPassword"
            }
          }
        }
      }
    }
  }
}
```

### Create an additional member in an existing Hyperledger Fabric network<a name="aws-resource-managedblockchain-member--examples--Create_an_additional_member_in_an_existing_Hyperledger_Fabric_network"></a>



#### YAML<a name="aws-resource-managedblockchain-member--examples--Create_an_additional_member_in_an_existing_Hyperledger_Fabric_network--yaml"></a>

```
Description: "Basic additional member template"
Parameters:
  MemberName:
    Type: String
  MemberDescription:
    Type: String
  MemberAdminUsername:
    Type: String
  MemberAdminPassword:
    Type: String
  NetworkId:
    Type: String
  InvitationId:
    Type: String
Resources:
  Member:
    Type: 'AWS::ManagedBlockchain::Member'
    Properties:
      MemberConfiguration:
        Name: !Ref MemberName
        Description: !Ref MemberDescription
        MemberFrameworkConfiguration:
          MemberFabricConfiguration:
            AdminUsername: !Ref MemberAdminUsername
            AdminPassword: !Ref MemberAdminPassword
      NetworkId: !Ref NetworkId
      InvitationId: !Ref InvitationId
```

#### JSON<a name="aws-resource-managedblockchain-member--examples--Create_an_additional_member_in_an_existing_Hyperledger_Fabric_network--json"></a>

```
{
           "Description": "Basic additional member template",
  "Parameters": {
      "MemberName": {
          "Type": "String"
      },
      "MemberDescription": {
          "Type": "String"
      },
      "MemberAdminUsername": {
          "Type": "String"
      },
      "MemberAdminPassword": {
          "Type": "String"
      },
      "NetworkId": {
          "Type": "String"
      },
      "InvitationId": {
          "Type": "String"
      }
  },
  "Resources": {
      "Member": {
          "Type": "AWS::ManagedBlockchain::Member",
          "Properties": {
              "MemberConfiguration": {
                  "Name": {
                      "Ref": "MemberName"
                  },
                  "MemberFrameworkConfiguration": {
                      "MemberFabricConfiguration": {
                          "AdminUsername": {
                              "Ref": "MemberAdminUsername"
                          },
                          "AdminPassword": {
                              "Ref": "MemberAdminPassword"
                          }
                      }
                  }
              },
              "NetworkId": {
                  "Ref": "NetworkId"
              },
              "InvitationId": {
                  "Ref": "InvitationId"
              }
          }
      }
  }
}
```