## What is CFNDSL?

> "The cnfdsl gem provides a simple DSL that allows you to write equivalent templates in a more friendly language and generate the correct json templates from the CLI"

```ruby
CloudFormation {
  Description "Test"

  Parameter("One") {
    String
    Default "Test"
    MaxLength 15
  }

  Output(:One,FnBase64( Ref("One")))

  Resource("MyInstance") {
    Type "AWS::EC2::Instance"
    Property("ImageId","ami-14341342")
  }

}
```

Note:
<ul>
  <li>Clean DSL format and easy to read</li>
  <li>CLI tool that is passed the template to generate the JSON from</li>
  <li>Validates the resource types and properties and checks for invalid refs</li>
</ul>
