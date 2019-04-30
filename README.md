# Assignment1
小组成员
16301093	黄镇海
16301094	黄琛深
16301103	谢俊

Basic requirements:
开发环境:
		jdk		1.8.0_211
		redis	Redis-x64-3.0.504
		IDEA	IntelliJIdea2019.1
		Mysql      8.0.16（64位）




Spring Data JPA implementation:（详情在A1-report.docx文档）

基于springboot框架

多数据源，联表查询

Web Caching:
	验证方式:
		在getContactById 方法中 加入sleep 函数,并打印相关信息到控制台
	
	Spring cache:	
		在....application填写@EnableCaching注解
		在ContactServiceImpl 中的getContactById 声明前 填写@Cacheable("contacts") 注解
		
	redis cache:
		配置填写
		spring.cache.type=redis
		spring.redis.host=localhost
		spring.redis.port=6379
		添加依赖:
		<dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-redis</artifactId>
        </dependency>
		
		由于中的getContactById方法返回的是一个object 不可直接序列化
			方法:contact对象 实现 Serializable 接口	也可以转json实现序列化
		
					
		
