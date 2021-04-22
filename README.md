# produce-gsc-3-FH
production package containing codes from "produce-gsc-un-46", "produce-gsc-osm-46", etc


## install
```console
git clone https://github.com/un-vector-tile-toolkit/produce-gsc-3-FH
cd produce-gsc-3-FH
npm install
vi produce-gsc-un-46/config/default.hjson //edit config info, e.g. host, dbUser, dbPassword, etc.
vi produce-gsc-osm-46/config/default.hjson //edit config info, e.g. host, dbUser, dbPassword, etc.
```

## Possible workflow
run "work_undata.sh" to create un sourced vector tiles (update frequency is irregular/ when needed.)  
run "work_every.sh" everyday up create/update priority area (daily update).  
run "work_day0X" once a week to create/update othere areas (weekly update).     

Please be advised that "work_every" and "work_day0x" newly create (update) the data from osm only, but they will be merged with un source vectortile using tile-join.  
