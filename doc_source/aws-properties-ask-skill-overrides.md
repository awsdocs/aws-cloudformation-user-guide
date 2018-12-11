# Alexa::ASK::Skill Overrides<a name="aws-properties-ask-skill-overrides"></a>

<a name="aws-properties-ask-skill-overrides-description"></a>The `Overrides` property type provides overrides to the skill package to apply when creating or updating the skill\. Values provided here do not modify the contents of the original skill package\. Currently, only overriding values inside of the skill manifest component of the package is supported\.

<a name="aws-properties-ask-skill-overrides-inheritance"></a> `Overrides` is a property of the [SkillPackage](aws-properties-ask-skill-skillpackage.md) property type\.

## Syntax<a name="aws-properties-ask-skill-overrides-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ask-skill-overrides-syntax.json"></a>

```
{
  "[Manifest](#cfn-ask-skill-overrides-manifest)" : JSON object
}
```

### YAML<a name="aws-properties-ask-skill-overrides-syntax.yaml"></a>

```
[Manifest](#cfn-ask-skill-overrides-manifest): JSON object
```

## Properties<a name="aws-properties-ask-skill-overrides-properties"></a>

`Manifest`  <a name="cfn-ask-skill-overrides-manifest"></a>
Overrides to apply to the skill manifest inside of the skill package\. The skill manifest contains metadata about the skill\. For more information, see [Skill Manifest Schemas](https://developer.amazon.com/docs/smapi/skill-manifest.html)\.  
 *Required*: No  
 *Type*: JSON object  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="cfn-ask-skill-overrides-example"></a>

### JSON<a name="aws-properties-ask-skill-overrides-example.json"></a>

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

### YAML<a name="aws-properties-ask-skill-overrides-example.yaml"></a>

```
Manifest:
  publishingInformation:
    locales:
      en-US:
        summary: "Sample Short Description"
    category: "EDUCATION_AND_REFERENCE"
```