# STIRData data catalog
Data catalog for datasets used in STIRData.
You can fill in a DCAT-AP metadata record in [our form](https://stirdata.opendata.cz/formulář/) and then commit the resulting JSON-LD file to this repository.

Some rules:
1. Dataset IRI should start with `https://stirdata.opendata.cz/resource/dataset/<country>/`
2. We should have folders in this repository named `<country>`

We support metadata in English and one other language, specified by the appropriate language tag.
The form saves and loads JSON-LD files with the metadata records.
You can, for instance, load an exsiting JSON-LD file from this repository by browsing to it, clicking `Raw` and using the URL of the raw representation in the "Load from URL" dialog on the first page of the [form](https://stirdata.opendata.cz/formulář/).

Once commited to the repo, a LinkedPipes ETL pipeline runs automatically, populating the [user interface](https://stirdata.opendata.cz/datasets) and [SPARQL endpoint](https://api.triplydb.com/s/TEW-uznU-).
If you used the proper dataset IRI, it should also become dereferencable.
