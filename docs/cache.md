## Mybatis �Ļ������
Ĭ�϶�������������
<setting name="cacheEnabled" value="true"> </setting>
** false �� �رջ��棬�رյ��Ƕ������棬�Լ�����һֱ������ **

** һ�����棨���ػ��棩 ** 

	sqlSession ����Ļ��棬 һ��������һֱ�����ģ�
	�����ݿ�ͬһ�λỰ�ڼ��ѯ�������ݻ�ŵ����ػ����С�
	һ������ʧЧ�����
	A. sqlSession ��ͬ
	B. sqlSession ��ͬ����ѯ������ͬ
	C. sqlSession ��ͬ�����β�ѯ֮������ɾ��
    D. sqlSession ��ͬ���ֶ������һ�����档 ʹ��SQLSession.cleanCheache()������
    
** �������� ��ȫ�ֻ��棩����namespace ����Ļ��棬 һ��namespace ��Ӧһ����������** 

	��������
	1. һ���Ự��ѯһ�����ݣ�������ݾͻᱻ����һ�������У�
	2. ����Ự�رգ�һ�������е����ݾͻᱻ���ڶ�������У��µĻỰ��ѯ��Ϣ���Ϳ��Բ��ն��������е���Ϣ
	3. sqlSession == EmployeeMapper ==>Employee
	                 DepartmentMapper ==>Department
	��ͬnamespace��ѯ���������ݾͻ�����Լ���Ӧ�Ļ�����
	
	ʹ��
	A. <setting name="cacheEnabled" value="true"> </setting>
	B. mapper.xml��ʹ��
	<cache></cache>
		����
		<cache eviction=""></cache>
		eviction������Ļ��ղ��ԣ� Ĭ�ϣ�LRU��
		   LRU�� �������ʹ�ã��Ƴ��ʱ�䲻��ʹ�õĶ���
		   FIFO���Ƚ��ȳ�����������뻺���˳�����Ƴ����ǡ�
		   SOFT��������:�Ƴ�����������������״̬�������ù���Ķ���
		   WEAK�������ã����������Ƴ����������ռ���״̬�������ù���Ķ���
		flushInterval�������ˢ�¼��
		readOlay�� 
			true ֻ��
			false ��ֻ�� ��Ĭ�ϣ�	   
		size�� ����Ĭ�ϷŶ��ٸ�Ԫ��
		type�� ָ���Զ��建���ȫ����   
	C. ���ǵ�POJO��Ҫʵ�����л��ӿ�

** �����������ú�����** 
	
	1. Ĭ�϶�������������  false �� �رջ��棬�رյ��Ƕ������棬�Լ�����һֱ������	   
	name="cacheEnabled" value="true"
	2. ÿ��select��ǩ����useCache="true"  
		true�� 
		false�������û��棨һ��������Ȼ���ã��������治���ã�
	3. ÿ����ɾ�ı�ǩ��flushCache="true"
		��ɾ����ɺ�ͻ��������
		����:һ�����汻�������������Ҳ�ᱻ���
	4. sqlSession.cleanCache()��ֻ�����ǰsession��һ�����档
	5. localCacheScpoe�����ػ���������
		session����ǰ�Ự���������ݱ����ڻ����У�
		statement�����Խ����Լ�����

**Mybatis ����ͼ��**
![](https://github.com/wangjianxiongwjx/mybatis01/blob/master/src/main/img/1562407790.jpg)

	   
	   
	   
	   
	   
	   
	   
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	
	





