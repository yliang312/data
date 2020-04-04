# tar & split
tar czvf test.tar.gz test/
split -b 30m influxdb.tar.gz influxdb.tar.gz.split
cat influxdb.tar.gz.splita* > influxdb.tar.gz
tar xvf influxdb.tar.gz
