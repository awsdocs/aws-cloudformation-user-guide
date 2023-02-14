# Alexa::ASK::Skill Overrides<a name="aws-properties-ask-skill-overrides"></a>

The `Overrides` property type provides overrides to the skill package to apply when creating or updating the skill\. Values provided here do not modify the contents of the original skill package\. Currently, only overriding values inside of the skill manifest component of the package is supported\.

 `Overrides` is a property of the `Alexa::ASK::Skill SkillPackage` property type\.

## Syntax<a name="aws-properties-ask-skill-overrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ask-skill-overrides-syntax.json"></a>

```
{
  "[Manifest](#cfn-ask-skill-overrides-manifest)" : Json
}
```

### YAML<a name="aws-properties-ask-skill-overrides-syntax.yaml"></a>

```
  [Manifest](#cfn-ask-skill-overrides-manifest): Json
```

## Properties<a name="aws-properties-ask-skill-overrides-properties"></a>

`Manifest`  <a name="cfn-ask-skill-overrides-manifest"></a>
Overrides to apply to the skill manifest inside of the skill package\. The skill manifest contains metadata about the skill\. For more information, see [Skill Manifest Schemas](https://developer.amazon.com/docs/smapi/skill-manifest.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-ask-skill-overrides--examples"></a>



### Alexa Skill Overrides Resource Configuration<a name="aws-properties-ask-skill-overrides--examples--Alexa_Skill_Overrides_Resource_Configuration"></a>

#### JSON<a name="aws-properties-ask-skill-overrides--examples--Alexa_Skill_Overrides_Resource_Configuration--json"></a>

```
"Manifest": {
  "publishingInformation": {
    "locales": {
      "en-US": {
        "summary": "Sample Short Description",
      }
    },
    "category": "EDUCATION_AND_REFERENCE"
  }
}
```

#### YAML<a name="aws-properties-ask-skill-overrides--examples--Alexa_Skill_Overrides_Resource_Configuration--yaml"></a>

```
Manifest:
  publishingInformation:
    locales:
      en-US:
        summary: "Sample Short Description"
    category: "EDUCATION_AND_REFERENCE"
```