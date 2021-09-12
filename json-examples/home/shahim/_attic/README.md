This directory is setup to write JSON and Yaml examples of the CCDH model. To get started:

  - Download and install Visual Studio Code (VSC)
    - Install the "YAML" extension in VSC. This one: https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml
    - The extension can be installed in VSC from the Extensions


All .json files in this directory will have the json-schema-examples/schemas/examples-schema.json applied to them in Visual Studio Code and Intellij but only VSC has good schema based editing support.

Intellij, as of now, will not provide autocomplete support but it does look like it validates the JSON. However, the validation error messages are not helpful at all. VSC gives specific and helpful error messages regarding what's wrong with the JSON.

If you edit the schema file, it is likely that you will need to restart VSC to pick up those schema changes. VSC seems to, at least with this large schema file, to hold on to the initial evaluation of the schema when the IDE is started. Intellij seems to update its evaluation with any change but given that it doesn't help with editing the JSON examples, it's not a very useful IDE for example editing right now.
