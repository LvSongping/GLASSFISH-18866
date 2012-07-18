GLASSFISH-18866
===============

[Bug Description]
Two different wars with same context root can be deployed on server.

[Operations]
1deploy the test_sample1.war with context root value called "test_sample1" to the server in admin-gui

2.deploy the test_sample2.war to the server in admin-gui with the same context root value as test_sample1.war ,
and deploy will be failed at the first time because context root is not unique.

3.repeat the step 2 again,the test_sample2.war can be deployed successfully without any error message.

4.After step3, "http://localhost:8080/test_sample1" can be accessed successfully, however, the contents of repsonse comes from test_sample2.war.

5.by means of admin-cli, the results of step1～step3 are also the same as the results of admin-gui.

[Affected versions ]
1 4.0_b41
2 gf's trunk until 2012/06/22


 

