Dynamic SQL ����̬sql��




## mybatis�������ļ�
1. properties ����
   resource ����

2. seting ����

   mapUnderscoreToCamelCase�� �Ƿ����Զ��շ���������camel case��ӳ�䣬���Ӿ������ݿ����� A_COLUMN ������ Java ������ aColumn ������ӳ�䡣 Ĭ��false
   
3. typeAliases ���ͱ���: ֻ��Ϊ�������������

	package����Ϊ�������µ�����java��������� �����������԰��л��и�������ͬ���Ƶ�java�� �� ����ʹ��@Alisa ��ָ����java �������
	   
	  ![](https://github.com/wangjianxiongwjx/mybatis01/blob/master/src/main/img/1562387700.jpg)
  
4. typeHanders ���ʹ�����

	������ MyBatis ��Ԥ������䣨PreparedStatement��������һ������ʱ�����Ǵӽ������ȡ��һ��ֵʱ�� ���������ʹ���������ȡ��ֵ�Ժ��ʵķ�ʽת���� Java ���͡�

5. plugins (���)

	Executor (update, query, flushStatements, commit, rollback, getTransaction, close, isClosed)
	ParameterHandler (getParameterObject, setParameters)
	ResultSetHandler (handleResultSets, handleOutputParameters)
	StatementHandler (prepare, parameterize, batch, update, query)

6. environments���������ã�

	�����������transactionManager��
	����Դ��dataSource��
 
7. mysql ֧�ֶ�����Դ����

8. mapper ��ǩ

    resource ���ػ������ļ�
    url ���Ի����µ���Դ
    class ���ýӿ� 1. ��sqlӳ���ļ���ӳ���ļ���mapper�ļ�ͬ���� ������ͬһ��������
    
    
 **ע��** ����ǩ����û�е��Ǳ�ǩ��˳���ܴ���
 
  ��ȡ��������
useGeneratedKey   �൱��jdbc statement.getGenerratedKeys()
keyProperty  ��ֵ���ƶ����ֶ�


## ��������

1. �������� �������⴦��#{������} ȥ������
2. ���������
	 ��������ᱻ��װ��һ��map
	key �� param1 ... paramN�� ���߲��������� 
	������������ȷָ����װ����ʱ��map��key @paramע��
3. ����POJO ����

4. mybatis ����������� 
![](https://github.com/wangjianxiongwjx/mybatis01/blob/master/src/main/img/1562396468.jpg)

5. ����ֻ��ȡ#{} �� ${}

	 #{} Ԥ�������ʽ�ŵ�sql�У�����sql ע��
	 ${} ��ֱֵ��ƴ��sql��ԭ��jdbc ��֧��ռλ���ĵط����� ${}����ȡֵ
	 ���磺 �ֱ�,���򣬰���ݷֱ�
	 select * from${}_salary where ....
	 
	 #{}���ḻ���÷� 
	   �涨������һ������
	 javaType�� jdbcType�� mode���洢���̣���resultMap...
	 jdbcType: ͨ����Ҫ��Ŀ�����������±����ã�
	 ����������λnull��ʱ����Щ���ݿ���ܲ���ʶ��mybatis��null��Ĭ�ϴ�������oracle
	 #{id, jdbcType=NULL}
	 ����ȫ�������У�jdbcTypeForNull=OTHER
	 <setings>
	     <string name="jdbcTypeForNull" value="NULL">
	 </setings>
	 
mybatis ����һ��Map<Integer, Employee> ���Ǽ�¼��������value��һ������

	ʹ��@Mapkey("id") ע�� ����mybatismap��key������

resultMap ����

	1. �������Է�װ����� <result columns="did" property="dept.id">
	2. association ָ��������ԵĶ�������
	<association property="dept" javaType="com.wjx.Dept"> 
	   <id columns="did" property="id"></id>
	   <result columns="dname" property="dname"></result>
	</association>
	3.�ֲ���ѯ
	  A.association�����������ķ�װ����
	  B.select��������ǰ�����ǵ���selectָ���ķ�������Ľ��
	  C.columns��ָ������һ�е�ֵ�����������

lazyLoadingEnabled �ӳټ��أ�������أ�






 





	
  
 


 
 
 
    
    
   