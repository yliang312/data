# tar & split
tar czvf test.tar.gz test/
split -b 30m influxdb.tar.gz influxdb.tar.gz.split
cat influxdb.tar.gz.splita* > influxdb.tar.gz
tar xvf influxdb.tar.gz

docker run --privileged --name some-docker -d -e DOCKER_TLS_CERTDIR="" docker:dind
docker run --rm -e DOCKER_TLS_CERTDIR="" --link some-docker:docker docker version //执行docker命令
https://blog.csdn.net/weixin_36572983/article/details/100162750
