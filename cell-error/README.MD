## 自定义error
 * 实现go原生的error接口，自定义一个解码函数MyErrorEncoder，在[]kithttp.ServerOption{}里面包裹进去，MyErrorEncoder函数将状态码直接写进http status code里面，这种方式有利于日志错误分类的收集和统计
 * 访问`localhost:8000/user/2` 打开浏览器的调试工具会发现status code是406了
