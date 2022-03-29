application：
    实现feign【*FacadeImpl】@RestController
    【client,domain,shared】
client: 
    提供feign接口【*Facade】 遵循CQRS
    【common】
common：
domain：
    提供能力接口给application&实现
    【common】
infrastructure:
    cacheServiceImpl+自有查库
    【domain,shared】
infrastructure-rpc: 
    第三方包调用【非自己都叫第三方】
    【domain,shaered】
server:
    启动类，需要引入application不然扫描找不到*Controller
    【application】
shared：
    cache service
    【common】

------------------------------------------------------------------
创建maven archetype
1. mvn archetype:create-from-project
2. 修改target/generated-sources/src/main/resources/archetype-resources下的文件
3. 
