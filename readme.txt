不得有这样的配置：
zuulsrv
	application.yml
	application-dev.yml
	application-prod.yml


假如profiles.active: prod，服务从config server读取 application-prod.yml 后，还会重复加载默认的 application.yml
解决办法：servername.yml servername-dev.yml servername-prod.yml
