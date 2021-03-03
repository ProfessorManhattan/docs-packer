## Formatting the Template JSON

In each of our Packer repositories, you will see a file named `template.json`. This serves as the configuration file that Packer uses when building our boxes. Please follow the guidelines below when formatting a `template.json` file:

* The `"variables"` section should be at the top of the `template.json` file
* Make sure the variable names are consistent across [our Packer repositories]({{ }}).
* Prefer naming the variables after the section they will be placed.
	* For example, the variable used for `ssh_password` should also be named `ssh_password` so it looks like this: `"ssh_password": "{{ user \`ssh_password\` }}"`.
* All the JSON objects should be in alphabetical order with the following exceptions:
	* The `"variables"` section should be at the top of the file.
	* The `"type"` field should be at the top of its section.
* All environment variables should be referenced in capitals so `http_proxy` should be `HTTP_PROXY` (the actual user variables in the `variables` section should all be lowercased, however).
* Any text that is shared between multiple builders should be stored as a variable. The only exception is data that is specific to each builder like shutdown command.
* Use the https://mirror.arizona.edu as the download location.
* All the variables should start with {{ and then a space. The same is true for the opposite side of the variable.
	* **GOOD:** `{{ user 'variable' }}`
	* **BAD:** `{{user 'variable'}}`
* In general, the `template.json` file should look nearly identical across our different Packer repositories.
