## What is CFNDSL?

```bash
bash-3.2$ cfndsl /path/to/my/template.rb

{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "Test",
    "Outputs": {
        "One": {
            "Value": {
                "Fn::Base64": {
                    "Ref": "One"
                }
            }
        }
    },
    "Parameters": {
        "One": {
            "Default": "Test",
            "MaxLength": 15,
            "Type": "String"
        }
    },
    "Resources": {
        "MyInstance": {
            "Properties": {
                "ImageId": "ami-14341342"
            },
            "Type": "AWS::EC2::Instance"
        }
    }
}
```

Note:
<ul>
  <li>Clean DSL format and easy to read</li>
  <li>CLI tool that is passed the template to generate the JSON from</li>
  <li>Validates the resource types and properties and checks for invalid refs</li>
</ul>
