Open the json-examples.code-workspace in Visual Studio Code.

The **json-schema-examples** folder has been configured to apply schema validation according to CCDH JSON Schema from this GitHub version: https://github.com/cancerDHC/ccdhmodel/blob/de4452ca5120b22b4bf519ffb189b6d083b2ba45/jsonschema/ccdhmodel.schema.json

The entities for the CCDH built schema, as is, have prefix names "ccdh.0713...". For example, when you'd like to create a Diagnosis example of this schema, you'd enter (with autocomplete support) "ccdh.0713.Diagnosis" for the "Schema" filed. See the existing simple "example.json" file in the "examples" directory.

The other variations of the model are "ccdh.0713cc" for entities with CodeableConcept and "ccdh.0713core" for entities with CodeableConcept and without the "profiling" entities.

For now, just use the Title, Description, Schema, and Example fields. The use of other fields will be documented once they are fully implemented. Basically, the other fields will allow a testing setup where examples are created to test if they pass or fail validation rules that go beyond the entity's definition in its schema.
