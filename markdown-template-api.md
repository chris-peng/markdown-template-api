<!-- 模板文件 -->

# 通则

>##### baseUrl:
  
* 测试环境：`https://xxx.xx:888/xx`
* 生产环境：`https://yyy.yy/yy`

>##### 接口url说明


 * url中的 `{xx}` 表示路径参数，参数名为xx


>##### 返回数据说明

* <font color="green">2XX</font>  
    成功，返回的数据格式见具体接口描述
* <font color="red">401</font>  
    授权失败，通常情况下，这意味着需要提醒用户重新登录
* <font color="red">其他>=400</font>  
    请求失败，具体含义可以[参考这里](https://baike.baidu.com/item/HTTP%E7%8A%B6%E6%80%81%E7%A0%81)，通常情况下，同时返回如下数据：

        { 
            "code": -1, // 错误码 
            "message": " 数据不存在！ ", // 错误信息 
            "data": {...} // 附加数据 
        }
<br/>
<br/>
************************************
<br/>
<br/>

# 接口列表


## 获取产品信息
### `GET` **/product/{id}**

> Path Parameters:

参数名     |   必须   |  说明
--        |   :--:   |  -- 
id        |    y     |  产品id

> Headers:

名称      |   必须   |  说明
--        | :--:     |  --

> Query Parameters:

参数名     |   必须   |  说明
--        |   :--:   |  -- 

> Response:

* 200:Ok
        
        样例：
        {
            "name": "Matrix VR",
            "description": "Awesome!",
            "produceDate": "2018/6/21"
        }
* 404:Not Found


## 提交产品
### `POST` **/product/**

> Post Body:

    样例：
    {
        "name": "Matrix VR",
        "description": "Awesome!",
        "produceDate": "2018/6/21"
    }
> Response:

* 200:Ok
