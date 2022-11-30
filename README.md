# Toponym Resolution in Unstructured Texts Based on Heuristics

This repository presents two heuristics for geocoding: normalization of adjectival toponyms and geometric optimization by toponym type.

This code uses [ElasticSearch](https://www.elastic.co) through [docker](https://www.docker.com/) using [docker-compose](https://docs.docker.com/compose/). The [docker-compose file](docker-compose.yml) can be used to start a local ElasticSearch server for experiments. 

An ElasticSearch index can be imported, using this [notebook](/src/Import_Index_ElasticSearch.ipynb), or created, using this [notebook](/src/Create_Index_ElasticSearch.ipynb). The index files are saved in a folder named `es_repo`.

The experiments related to the baseline definition can be found in the [Initial Experiments](/src/Initial_Experiments.ipynb).

The experiments comparing the baseline (HG) to the heuristics of normalization of adjectival toponyms (HG-A) and geometric optimization by toponym type (HG-T) can be found in the [Final Experiments](/src/Final_Experiments.ipynb). A geocoder using both heuristics (HG-AT) is also evaluated in the same notebook.

A comparison to the [CLAVIN](https://github.com/Novetta/CLAVIN-rest) geocoder can be found in this [notebook](/src/Comparisson_CLAVIN.ipynb). Please, remember to uncomment the lines related to CLAVIN in the [docker-compose file](docker-compose.yml).

A comparison to [CamCoder](https://github.com/milangritta/Geocoding-with-Map-Vector) can be found in this [notebook](/src/Comparisson_CamCoder.ipynb).

Files containing GeoWebNews and TR-News including geonames feature classes can be found in [datasets](/datasets). CamCoder geocoding results used for comparisons can be found in [outputs](/datasets/outputs).

This repository is related to the following publication: 
> Sá, Breno Dourado, Ticiana Coelho da Silva, and José Antônio Fernandes de Macêdo. "[Enhancing Geocoding of Adjectival Toponyms with Heuristics](https://aclanthology.org/2022.politicalnlp-1.6/)." Proceedings of the LREC 2022 workshop on Natural Language Processing for Political Sciences. 2022.
