# Fotoquest DAO Mappings for 52n DAO SPI module

<img style="width: 60%; height: 60%" alt="series-rest-api architecture overview" src="https://52north.github.io/series-rest-api/img/big-picture.png">

## Description

**Provide database customizations to provide Fotoquest data via 52n Series REST API.**

_This module provides custom Hibernate mappings and database views. It enables the [52n DAO SPI module](https://github.com/52North/dao-series-api) 
to connect to a Fotoquest database. The Web application provides then RESTful data access via 52n Series REST API._ 

The Fotoquest module provides customizations on the default behaviour of accessing 52n series data model. Accessing
Fotoquest data is therefore technically transparent for the DAO module which serves as backend access layer 
to retrieve data. The well defined RESTful Web interface makes it easy for lightweight clients to query and work with
the data. Besides pure data access, the data can be preprocessed with common IO functionalities e.g. 
  * prerendering of series data, 
  * generalization, 
  * overlaying of data from multiple series
  * conversion of raw data to other formats like pdf and png

The following main frameworks are used to provide this API:
- [Hibernate](https://hibernate.org/) 
- [52°North DAO SPI Impl](https://github.com/52North/dao-series-api/)
- [52°North Series API](https://github.com/52North/series-rest-api/) 

## References
tbd

## License

The module is published under the [GNU General Public License v2 (GPLv2)](http://www.gnu.org/licenses/gpl-2.0.html).

## Changelog
- https://github.com/52North/fotoquest-series-api/blob/develop/CHANGELOG.md
- for detailed infos check https://github.com/52North/fotoquest-series-api/pulls?q=is%3Apr+is%3Aclosed

## Contributing
We try to follow [the GitFlow model](http://nvie.com/posts/a-successful-git-branching-model/), 
although we do not see it that strict. 

However, make sure to do pull requests for features, hotfixes, etc. by
making use of GitFlow. Altlassian provides [a good overview]
(https://www.atlassian.com/de/git/workflows#!workflow-gitflow). of the 
most common workflows.

## Contact
Henning Bredel (h.bredel@52north.org)

## Quick Start
### Webapp Installation
- tbd: deployment configuration
- tbd: build from source
- tbd: externalize config before build

### Configuration
- general config options 
  - Generalizer
  - Prerendering
  - Date formatting 
  - Rendering Hints
  - Status Intervals
  - Metadata from a Database

#### Logging
Depending on which build environment you've chosen open one the `WEB-INF/classes/logback-{dev,ci,prod}.xml`. Here
you can edit log levels and log outputs.

### Client development
Refer to the official [Series REST API documentation](http://52north.github.io/series-rest-api) to get a detailed 
overview on how to access the data provided by the API. 
