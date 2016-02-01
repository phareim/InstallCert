# InstallCert

```
This is a program to help fix this problem:

Caused by: javax.net.ssl.SSLHandshakeException: sun.security.validator.ValidatorException: 
PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException: 
unable to find valid certification path to requested target
 
Caused by: sun.security.validator.ValidatorException: PKIX path building failed: 
sun.security.provider.certpath.SunCertPathBuilderException: unable to find 
valid certification path to requested target
 
Caused by: sun.security.provider.certpath.SunCertPathBuilderException: 
unable to find valid certification path to requested target
```

From: http://myshittycode.com/2014/06/05/java-https-unable-to-find-valid-certification-path-to-requested-target/ and http://www.mkyong.com/webservices/jax-ws/suncertpathbuilderexception-unable-to-find-valid-certification-path-to-requested-target/. 


The long story short here is to:
* Run java InstallCert `<server>:<port>` to generate a file called `jssecacerts`. 
* Then, drop this file in `${JAVA_HOME}/lib/security directory`.

