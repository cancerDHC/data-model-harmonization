
Minimal documentation:

1. Install Visual Studio Code (VSC)
1. Install the "YAML" VSC extension. It's the one with a red icon that says "YML" on it.
1. Open the json-examples.code-workspace seen in this folder in Visual Studio Code.
1. Create create *.json or *.yaml data example files under one of the examples directories.
1. Files starting with "temp-" will be git ignored. You can name files like this to play with examples locally without worrying that they will show up in the Git repository at GitHub. When ready, rename them to remove the "temp-" prefix to be able to commit and push them.
1. The outer most value in a file is an object. Create some self descriptive key in that object and then make the value of that key an object. This object is called the "Example Object" (EO) below At this point you should get VSC autocomplete and validation support according to the schema assigned to the directory containing the file.


The Example Object (EO) is a wrapper object that has this schema:
1. A required "Title" key and string value to give a nice name for your example.
2. A required "Schema" key and a selection from the enumeration for this field. Use auto complete to get the suggestions and start typing some part of the entity's name that you'd like to instantiate. The selection you make here becomes the effective schema for the "Example"'s value to support auto completion and validation.

    * For now, only select an entry that starts with "ccdh.0713."
    * This will provide validation according to this CCDH JSON Schema file that was built on 7/13/2021: https://github.com/cancerDHC/ccdhmodel/tree/de4452ca5120b22b4bf519ffb189b6d083b2ba45/jsonschema
    * Few local manual schema fixes and additions were applied and will be propagated to future builds as needed.

3. An optional "Example" key and an object value that validates according to the selection made in 2 above.
4. Ignore the remaining possible keys of the EO object for now. They are work in progress to add a "testing" framework that applies additional validation rules for testing purposes.


WIP below, please ignore for now:

The other variations of the model are "ccdh.0713cc" for entities with CodeableConcept and "ccdh.0713core" for entities with CodeableConcept and without the "profiling" entities.
