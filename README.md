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
 
    
    
   