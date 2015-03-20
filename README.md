# dbpediaweights
DBpedia Weights

This page contains the DBpedia counts for computing the DBpedia node/edge weighting metrics

* combIC
* jointIC
* PMI

As described in 
Michael Schuhmacher and Simone Paolo Ponzetto: Knowledge-based Graph Document Modeling. In Proceedings of WSDM'14, pp. 543-552, ACM, 2014 ([paper](http://dx.doi.org/10.1145/2556195.2556250),  [presentation](http://dws.informatik.uni-mannheim.de/fileadmin/lehrstuehle/ki/pub/michael/WSDM14_Schuhmacher_Knowledge-based_Graph_Document_Modeling.pdf))

### Loading tab files
For loading the DBpedia2014 files into a mysql database, [create the tables](https://github.com/mschuhma/dbpediaweights/blob/master/dbpcounts_db_structure.sql.bz2) first, then load the files 

    load data infile 'ObjectCount.tab'
    INTO TABLE dbpcounts39.ObjCnt
    FIELDS TERMINATED BY '\t' enclosed by '"'
    LINES TERMINATED BY '\n';
