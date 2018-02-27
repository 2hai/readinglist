# readinglist
Sping Boot Demo

## <Spring Boot实战>读书笔记:

	1.Spring Boot 四个核心: 
		自动配置：针对很多Spring应用程序常见的应用功能，SpringBoot能自动提供相关配置。 
	
		起步依赖：告诉SpringBoot需要什么功能，它就能引入需要的库。 
		
		命令行界面：这是SpringBoot的可选特性借此你只需写代码就能完成完整的应用程序，无需传统项目构建。 
		
		Actuator：让你能够深入运行中的Spring Boot应用程序，一探究竟。

	
	2.下载地址:
			https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#getting-started-installing-the-cli
			
	3.在IDEA运行时出现没有jar包依赖问题,解决办法是在pom.xml中加下面代码:
	
	<!--打包时使用了maven默认的maven-jar-plugin插件，而不是spring-boot-maven-plugin插件这里加了依赖-->
		<build>
			<plugins>
				<plugin>
					<groupId>org.apache.maven.plugins</groupId>
					<artifactId>maven-compiler-plugin</artifactId>
				</plugin>
				<plugin>
					<groupId>org.springframework.boot</groupId>
					<artifactId>spring-boot-maven-plugin</artifactId>
					<version>${spring.boot.version}</version>
				</plugin>
			</plugins>
	</build>
	
	4.替换与去除起步依赖 : 当起步依赖中有多余的依赖包时,可以用<exclusions>来去除它的依赖,能精简项目.
						   直接把依赖的包写到pom.xml(<dependency>)中,就能覆盖依赖关系.就近原则.
