
-	1:安装oracle for .net驱动程序(ODTwithODAC121012)
-	2：连接时设置点击方式为ES（这样不用配置TNSNames.ora）
-	3：config文件中添加：

````xml
<system.data>
  <DbProviderFactories>
    <add name="OracleClient Data Provider" invariant="System.Data.OracleClient" description=".Net Framework Data Provider for Oracle" type="System.Data.OracleClient.OracleClientFactory, System.Data.OracleClient, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"/>
  </DbProviderFactories>
</system.data>
````

-	4：若是x64系统，需要安装64位驱动，或者配置应用连接池 ：启用32位应用程序。

## 参考网址：

http://www.cnblogs.com/zhenhong/p/3745452.html

## 常用config provider

````xml
<DbProviderFactories>
           <add name="Odbc Data Provider" invariant="System.Data.Odbc" description=".Net Framework Data Provider for Odbc" type="System.Data.Odbc.OdbcFactory, System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"/>
           <add name="OleDb Data Provider" invariant="System.Data.OleDb" description=".Net Framework Data Provider for OleDb" type="System.Data.OleDb.OleDbFactory, System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"/>
           <add name="OracleClient Data Provider" invariant="System.Data.OracleClient" description=".Net Framework Data Provider for Oracle" type="System.Data.OracleClient.OracleClientFactory, System.Data.OracleClient, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"/>
           <add name="SqlClient Data Provider" invariant="System.Data.SqlClient" description=".Net Framework Data Provider for SqlServer" type="System.Data.SqlClient.SqlClientFactory, System.Data, Version=2.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089"/>
        <add name="Microsoft SQL Server Compact Data Provider 4.0" invariant="System.Data.SqlServerCe.4.0" description=".NET Framework Data Provider for Microsoft SQL Server Compact" type="System.Data.SqlServerCe.SqlCeProviderFactory, System.Data.SqlServerCe, Version=4.0.0.0, Culture=neutral, PublicKeyToken=89845dcd8080cc91"/></DbProviderFactories>

````