# Download-Problem at any usage of Maven 3.5.2
On a freshly installed Ubuntu 18.04 with OpenJDK 10 or OracleJDK 8 and the distributed Maven in version 3.5.2 
during any Maven operation, which involves downloading of artifacts, I get the following failure message:

`... Unexpected error: java.security.InvalidAlgorithmParameterException: the trustAnchors parameter must be non-empty and 'parent.relativePath' points at wrong local POM @ line 11, column 10`

A similar security-related exception we get on Windows with a new Maven.

According to https://stackoverflow.com/questions/6784463/error-trustanchors-parameter-must-be-non-empty 
and https://bugs.launchpad.net/ubuntu/+source/ca-certificates-java/+bug/1770553 there has been a change, 
that the default Java keystore is password protected, whereas it has not been in former versions.

But for me it looks like Maven has switched to **https** connections instead of http.

We can verify the keystore problem by command <br>
`keytool -list -keystore /etc/ssl/certs/java/cacerts` <br>
If you enter an empty password, the keys from the keystore will not get listed.
If you in contrary enter the Oracle default password `changeit`, the 133 keys will get listed.

## Solution
You must provide the keystore password for all Java applications, which make https- or ssl-connections. You have several options:
1. Provide it on the command line for the Maven run: `mvn -Djavax.net.ssl.trustStorePassword=changeit package`
2. Provide it for all Maven runs: Define the environment variable <br>
`MAVEN_OPTS="$MAVEN_OPTS -Djavax.net.ssl.trustStorePassword=changeit"`
3. Provide it for all Java applications: Define the environment variable <br>
`JAVA_OPTS="$JAVA_OPTS -Djavax.net.ssl.trustStorePassword=changeit"`

There are several ways to define an environment variable, be it in a shell script, for one user, or for all users. This is not explained here.
