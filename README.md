## WiNGS : The Widely Integrated NGS platform for federated genome analysis

![WiNGS logo](https://github.com/wings-public/wings-public/raw/main/images/wings_logo.png)

### Homepage

[WiNGS Web Interface](https://wings-platform.org)

[WiNGS USER-API](https://wings.esat.kuleuven.be/rest-api/api-docs/)

### What is WiNGS

WiNGS is built as a federated ecosystem in which all sensitive data remains on the premises of registered users (e.g., a genetic center) and is queried through a centralized interface. This architecture enables secure cross-center collaboration while supporting anonymized statistical analysis.

WiNGS also functions as an analysis platform for Whole Exome Sequencing (WES) and Whole Genome Sequencing (WGS) data, enabling users to process, analyze, and interpret large-scale genomic datasets via the REST API within the same secure environment.

The platform’s core functionality—including genomic data analysis—is exposed to end users through the REST API, while administrative features such as user management and filter creation are managed through a web-based interface.

![WiNGS infrastructure layout](https://github.com/wings-public/wings-public/raw/main/images/wingsarchitecture.png "WiNGS infrastructural layout")

### Setting up WiNGS

To setup WiNGS, we provide a manual [here (mongoDB)](https://dev.azure.com/wingsorg/wings_api_deploy) and [here (annotations)](https://dev.azure.com/wingsorg/wings_anno_deploy). In order to finalize the setup, you will have to register in the [central infrastructure](https://wings-platform.org) as well. To do so, please [contact us](mailto:geert.vandeweyer@uza.be).


### Available Repositories

Several repositories are available under this account. They are organized as follows: 

```mermaid
flowchart TD;
   A[wings-public] --> B[CENTRAL INFRASTRUCTURE];
   A --> C[FEDERATED INFRASTRCUTURE];
   B --> D["wings_cdb<br/>-------<br/>Central MSSQL database"]
   B --> E["wings_ui<br/>-------<br/>ASP.NET code of the Web-Interface"]
   B --> L["wings_rest_api<br/>-------<br/>API code for user interaction with WiNGS"]
   C --> F["wings_api_internal<br/>-------<br/>-Routines to communicate with central infrastructure<br/>-Routines to communicate with Annotation infrastructure<br/>-MongDB database"]
   C --> G["wings_anno_api<br/>-------<br/>-Routines to manage annotation tasks<br/>-Optional, can be used centrally"]
   G --> H["annotation_parser<br/>-------<br/>Routines to combine annotations from different subtasks"]
   G --> I["vep_annotations<br/>-------<br/>Extended container to perform Ensmbel VEP"]
   G --> J["cadd_annotations<br/>-------<br/>Extended container to perform cadd scoring"]
   C --> K["wings_rstats<br/>-------<br/>R deployment to perform anonymized statistics"]
```

### Demo 

An overview of the capabilities of WiNGS is available on [youtube](https://www.youtube.com/watch?v=XlAMtSvBuwI)


### License
WiNGS is available under the [*GNU Affero General Public License Version 3*](https://www.gnu.org/licenses/agpl-3.0.en.html)

 

### Contact

If you have questions, feel free to reach out at [geert.vandeweyer@uza.be](mailto:geert.vandeweyer@uza.be)


