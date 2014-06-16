## Why did we build upon it?

```shell
gem install bbc-cosmos-tools

bash-3.2$ bbc-cosmos-tools stack update election-data-renderer --env=test
```

* CLI tool for removing some of the complexities of managing multiple components in cosmos. <!-- .element: class="padded" -->
* Allows stack, deployment and config related tasks to be performed against the cosmos API. <!-- .element: class="padded" -->
* One central place to store all resources and configuration for a given project. <!-- .element: class="padded" -->

Note:
<ul>
  <li>Talk about SQS queue ARN for IAM Role and Queue name for renderer</li>
</ul>
