# Java on Ubuntu 18.04
According to [Stephen Colebourne](https://blog.joda.org/2018/09/time-to-look-beyond-oracles-jdk.html) it is 
__Time to look beyond Oracle's JDK__.
If you want to run your Java applications for $free, 
Oracle will support any version of Oracle JDK only for one month after a new version has been released.

You can use alternative builds of OpenJDK from your Linux provider, or from https://adoptopenjdk.net/
AdoptOpenJDK is a community effort, backed by IBM, and Red Hat. Because AdoptOpenJDK provides the JDK for 8
different platforms, i.a. Linux, Windows, and MacOS, it should be the variant to go.

You can install by Synaptic the package __openjdk-11-jdk__. This results in the error 
```
E: ca-certificates-java: Unterprozess installed ca-certificates-java package post-installation script gab den Fehler-Ausgangsstatus 1 zurück
E: openjdk-11-jre-headless: 63.2076:Abhängigkeitsprobleme - verbleibt unkonfiguriert
E: openjdk-11-jdk-headless: 65.0943:Abhängigkeitsprobleme - verbleibt unkonfiguriert
E: openjdk-11-jdk: 75.4717:Abhängigkeitsprobleme - verbleibt unkonfiguriert
E: openjdk-11-jre: 77.3585:Abhängigkeitsprobleme - verbleibt unkonfiguriert
```
The full log of the failed installation texts as follows:
```
Vormals nicht ausgewähltes Paket openjdk-11-jre-headless:amd64 wird gewählt.
(Lese Datenbank ... 255709 Dateien und Verzeichnisse sind derzeit installiert.)
Vorbereitung zum Entpacken von .../00-openjdk-11-jre-headless_10.0.2+13-1ubuntu0.18.04.4_amd64.deb ...
Entpacken von openjdk-11-jre-headless:amd64 (10.0.2+13-1ubuntu0.18.04.4) ...
Vormals nicht ausgewähltes Paket ca-certificates-java wird gewählt.
Vorbereitung zum Entpacken von .../01-ca-certificates-java_20180516ubuntu1~18.04.1_all.deb ...
Entpacken von ca-certificates-java (20180516ubuntu1~18.04.1) ...
Vormals nicht ausgewähltes Paket libatk-wrapper-java wird gewählt.
Vorbereitung zum Entpacken von .../02-libatk-wrapper-java_0.33.3-20ubuntu0.1_all.deb ...
Entpacken von libatk-wrapper-java (0.33.3-20ubuntu0.1) ...
Vormals nicht ausgewähltes Paket libatk-wrapper-java-jni:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../03-libatk-wrapper-java-jni_0.33.3-20ubuntu0.1_amd64.deb ...
Entpacken von libatk-wrapper-java-jni:amd64 (0.33.3-20ubuntu0.1) ...
Vormals nicht ausgewähltes Paket libgif7:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../04-libgif7_5.1.4-2_amd64.deb ...
Entpacken von libgif7:amd64 (5.1.4-2) ...
Vormals nicht ausgewähltes Paket xorg-sgml-doctools wird gewählt.
Vorbereitung zum Entpacken von .../05-xorg-sgml-doctools_1%3a1.11-1_all.deb ...
Entpacken von xorg-sgml-doctools (1:1.11-1) ...
Vormals nicht ausgewähltes Paket x11proto-dev wird gewählt.
Vorbereitung zum Entpacken von .../06-x11proto-dev_2018.4-4_all.deb ...
Entpacken von x11proto-dev (2018.4-4) ...
Vormals nicht ausgewähltes Paket x11proto-core-dev wird gewählt.
Vorbereitung zum Entpacken von .../07-x11proto-core-dev_2018.4-4_all.deb ...
Entpacken von x11proto-core-dev (2018.4-4) ...
Vormals nicht ausgewähltes Paket libice-dev:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../08-libice-dev_2%3a1.0.9-2_amd64.deb ...
Entpacken von libice-dev:amd64 (2:1.0.9-2) ...
Vormals nicht ausgewähltes Paket libpthread-stubs0-dev:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../09-libpthread-stubs0-dev_0.3-4_amd64.deb ...
Entpacken von libpthread-stubs0-dev:amd64 (0.3-4) ...
Vormals nicht ausgewähltes Paket libsm-dev:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../10-libsm-dev_2%3a1.2.2-1_amd64.deb ...
Entpacken von libsm-dev:amd64 (2:1.2.2-1) ...
Vormals nicht ausgewähltes Paket libxau-dev:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../11-libxau-dev_1%3a1.0.8-1_amd64.deb ...
Entpacken von libxau-dev:amd64 (1:1.0.8-1) ...
Vormals nicht ausgewähltes Paket libxdmcp-dev:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../12-libxdmcp-dev_1%3a1.1.2-3_amd64.deb ...
Entpacken von libxdmcp-dev:amd64 (1:1.1.2-3) ...
Vormals nicht ausgewähltes Paket xtrans-dev wird gewählt.
Vorbereitung zum Entpacken von .../13-xtrans-dev_1.3.5-1_all.deb ...
Entpacken von xtrans-dev (1.3.5-1) ...
Vormals nicht ausgewähltes Paket libxcb1-dev:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../14-libxcb1-dev_1.13-1_amd64.deb ...
Entpacken von libxcb1-dev:amd64 (1.13-1) ...
Vormals nicht ausgewähltes Paket libx11-dev:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../15-libx11-dev_2%3a1.6.4-3ubuntu0.1_amd64.deb ...
Entpacken von libx11-dev:amd64 (2:1.6.4-3ubuntu0.1) ...
Vormals nicht ausgewähltes Paket libx11-doc wird gewählt.
Vorbereitung zum Entpacken von .../16-libx11-doc_2%3a1.6.4-3ubuntu0.1_all.deb ...
Entpacken von libx11-doc (2:1.6.4-3ubuntu0.1) ...
Vormals nicht ausgewähltes Paket libxt-dev:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../17-libxt-dev_1%3a1.1.5-1_amd64.deb ...
Entpacken von libxt-dev:amd64 (1:1.1.5-1) ...
Vormals nicht ausgewähltes Paket openjdk-11-jre:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../18-openjdk-11-jre_10.0.2+13-1ubuntu0.18.04.4_amd64.deb ...
Entpacken von openjdk-11-jre:amd64 (10.0.2+13-1ubuntu0.18.04.4) ...
Vormals nicht ausgewähltes Paket openjdk-11-jdk-headless:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../19-openjdk-11-jdk-headless_10.0.2+13-1ubuntu0.18.04.4_amd64.deb ...
Entpacken von openjdk-11-jdk-headless:amd64 (10.0.2+13-1ubuntu0.18.04.4) ...
Vormals nicht ausgewähltes Paket openjdk-11-jdk:amd64 wird gewählt.
Vorbereitung zum Entpacken von .../20-openjdk-11-jdk_10.0.2+13-1ubuntu0.18.04.4_amd64.deb ...
Entpacken von openjdk-11-jdk:amd64 (10.0.2+13-1ubuntu0.18.04.4) ...
ca-certificates-java (20180516ubuntu1~18.04.1) wird eingerichtet ...
Neue Version der Konfigurationsdatei /etc/ca-certificates/update.d/jks-keystore wird installiert ...
Keystore /etc/ssl/certs/java/cacerts wird in /etc/ssl/certs/java/cacerts.dpkg-new importiert...
Exception in thread "main" java.lang.ExceptionInInitializerError
	at java.base/javax.crypto.SecretKeyFactory.nextSpi(SecretKeyFactory.java:303)
	at java.base/javax.crypto.SecretKeyFactory.<init>(SecretKeyFactory.java:121)
	at java.base/javax.crypto.SecretKeyFactory.getInstance(SecretKeyFactory.java:168)
	at java.base/sun.security.pkcs12.PKCS12KeyStore.getPBEKey(PKCS12KeyStore.java:846)
	at java.base/sun.security.pkcs12.PKCS12KeyStore.engineLoad(PKCS12KeyStore.java:2085)
	at java.base/sun.security.util.KeyStoreDelegator.engineLoad(KeyStoreDelegator.java:222)
	at java.base/java.security.KeyStore.load(KeyStore.java:1479)
	at java.base/sun.security.tools.keytool.Main.loadSourceKeyStore(Main.java:2142)
	at java.base/sun.security.tools.keytool.Main.doCommands(Main.java:1184)
	at java.base/sun.security.tools.keytool.Main.run(Main.java:397)
	at java.base/sun.security.tools.keytool.Main.main(Main.java:390)
Caused by: java.lang.SecurityException: Can not initialize cryptographic mechanism
	at java.base/javax.crypto.JceSecurity.<clinit>(JceSecurity.java:118)
	... 11 more
Caused by: java.lang.SecurityException: Couldn't parse jurisdiction policy files in: unlimited
	at java.base/javax.crypto.JceSecurity.setupJurisdictionPolicies(JceSecurity.java:355)
	at java.base/javax.crypto.JceSecurity.access$000(JceSecurity.java:73)
	at java.base/javax.crypto.JceSecurity$1.run(JceSecurity.java:109)
	at java.base/javax.crypto.JceSecurity$1.run(JceSecurity.java:106)
	at java.base/java.security.AccessController.doPrivileged(Native Method)
	at java.base/javax.crypto.JceSecurity.<clinit>(JceSecurity.java:105)
	... 11 more
failed to convert PKCS12 keystore to JKS
dpkg: Fehler beim Bearbeiten des Paketes ca-certificates-java (--configure):
 Unterprozess installed ca-certificates-java package post-installation script gab den Fehler-Ausgangsstatus 1 zurück
Trigger für mime-support (3.60ubuntu1) werden verarbeitet ...
Trigger für desktop-file-utils (0.23-1ubuntu3.18.04.2) werden verarbeitet ...
libpthread-stubs0-dev:amd64 (0.3-4) wird eingerichtet ...
xorg-sgml-doctools (1:1.11-1) wird eingerichtet ...
dpkg: Abhängigkeitsprobleme verhindern Konfiguration von openjdk-11-jre-headless:amd64:
 openjdk-11-jre-headless:amd64 hängt ab von ca-certificates-java; aber:
  Paket ca-certificates-java ist noch nicht konfiguriert.

dpkg: Fehler beim Bearbeiten des Paketes openjdk-11-jre-headless:amd64 (--configure):
 Abhängigkeitsprobleme - verbleibt unkonfiguriert
libgif7:amd64 (5.1.4-2) wird eingerichtet ...
dpkg: Abhängigkeitsprobleme verhindern Konfiguration von openjdk-11-jdk-headless:amd64:
 openjdk-11-jdk-headless:amd64 hängt ab von openjdk-11-jre-headless (= 10.0.2+13-1ubuntu0.18.04.4); aber:
  Paket openjdk-11-jre-headless:amd64 ist noch nicht konfiguriert.

dpkg: Fehler beim Bearbeiten des Paketes openjdk-11-jdk-headless:amd64 (--configure):
 Abhängigkeitsprobleme - verbleibt unkonfiguriert
Trigger für sgml-base (1.29) werden verarbeitet ...
x11proto-dev (2018.4-4) wird eingerichtet ...
Trigger für bamfdaemon (0.5.3+18.04.20180207.2-0ubuntu1) werden verarbeitet ...
Rebuilding /usr/share/applications/bamf-2.index...
xtrans-dev (1.3.5-1) wird eingerichtet ...
libxdmcp-dev:amd64 (1:1.1.2-3) wird eingerichtet ...
Trigger für libc-bin (2.27-3ubuntu1) werden verarbeitet ...
libice-dev:amd64 (2:1.0.9-2) wird eingerichtet ...
libx11-doc (2:1.6.4-3ubuntu0.1) wird eingerichtet ...
Trigger für man-db (2.8.3-2ubuntu0.1) werden verarbeitet ...
dpkg: Abhängigkeitsprobleme verhindern Konfiguration von openjdk-11-jdk:amd64:
 openjdk-11-jdk:amd64 hängt ab von openjdk-11-jdk-headless (= 10.0.2+13-1ubuntu0.18.04.4); aber:
  Paket openjdk-11-jdk-headless:amd64 ist noch nicht konfiguriert.

dpkg: Fehler beim Bearbeiten des Paketes openjdk-11-jdk:amd64 (--configure):
 Abhängigkeitsprobleme - verbleibt unkonfiguriert
Trigger für gnome-menus (3.13.3-11ubuntu1.1) werden verarbeitet ...
Trigger für ca-certificates (20180409) werden verarbeitet ...
Updating certificates in /etc/ssl/certs...
0 added, 0 removed; done.
Running hooks in /etc/ca-certificates/update.d...

org.debian.security.InvalidKeystorePasswordException: Cannot open Java keystore. Is the password correct?
	at org.debian.security.KeyStoreHandler.load(KeyStoreHandler.java:68)
	at org.debian.security.KeyStoreHandler.<init>(KeyStoreHandler.java:52)
	at org.debian.security.UpdateCertificates.<init>(UpdateCertificates.java:65)
	at org.debian.security.UpdateCertificates.main(UpdateCertificates.java:51)
Caused by: java.io.IOException: Invalid keystore format
	at java.base/sun.security.provider.JavaKeyStore.engineLoad(JavaKeyStore.java:659)
	at java.base/sun.security.util.KeyStoreDelegator.engineLoad(KeyStoreDelegator.java:222)
	at java.base/java.security.KeyStore.load(KeyStore.java:1479)
	at org.debian.security.KeyStoreHandler.load(KeyStoreHandler.java:66)
	... 3 more
E: /etc/ca-certificates/update.d/jks-keystore exited with code 1.
done.
libatk-wrapper-java (0.33.3-20ubuntu0.1) wird eingerichtet ...
Trigger für hicolor-icon-theme (0.17-2) werden verarbeitet ...
dpkg: Abhängigkeitsprobleme verhindern Konfiguration von openjdk-11-jre:amd64:
 openjdk-11-jre:amd64 hängt ab von openjdk-11-jre-headless (= 10.0.2+13-1ubuntu0.18.04.4); aber:
  Paket openjdk-11-jre-headless:amd64 ist noch nicht konfiguriert.

dpkg: Fehler beim Bearbeiten des Paketes openjdk-11-jre:amd64 (--configure):
 Abhängigkeitsprobleme - verbleibt unkonfiguriert
libsm-dev:amd64 (2:1.2.2-1) wird eingerichtet ...
x11proto-core-dev (2018.4-4) wird eingerichtet ...
libxau-dev:amd64 (1:1.0.8-1) wird eingerichtet ...
libatk-wrapper-java-jni:amd64 (0.33.3-20ubuntu0.1) wird eingerichtet ...
libxcb1-dev:amd64 (1.13-1) wird eingerichtet ...
libx11-dev:amd64 (2:1.6.4-3ubuntu0.1) wird eingerichtet ...
libxt-dev:amd64 (1:1.1.5-1) wird eingerichtet ...
Trigger für libc-bin (2.27-3ubuntu1) werden verarbeitet ...
Fehler traten auf beim Bearbeiten von:
 ca-certificates-java
 openjdk-11-jre-headless:amd64
 openjdk-11-jdk-headless:amd64
 openjdk-11-jdk:amd64
 openjdk-11-jre:amd64
E: Sub-process /usr/bin/dpkg returned an error code (1)
Ein Paket konnte nicht installiert werden. Wiederherstellung wird versucht:
ca-certificates-java (20180516ubuntu1~18.04.1) wird eingerichtet ...
Keystore /etc/ssl/certs/java/cacerts wird in /etc/ssl/certs/java/cacerts.dpkg-new importiert...
Exception in thread "main" java.lang.ExceptionInInitializerError
	at java.base/javax.crypto.SecretKeyFactory.nextSpi(SecretKeyFactory.java:303)
	at java.base/javax.crypto.SecretKeyFactory.<init>(SecretKeyFactory.java:121)
	at java.base/javax.crypto.SecretKeyFactory.getInstance(SecretKeyFactory.java:168)
	at java.base/sun.security.pkcs12.PKCS12KeyStore.getPBEKey(PKCS12KeyStore.java:846)
	at java.base/sun.security.pkcs12.PKCS12KeyStore.engineLoad(PKCS12KeyStore.java:2085)
	at java.base/sun.security.util.KeyStoreDelegator.engineLoad(KeyStoreDelegator.java:222)
	at java.base/java.security.KeyStore.load(KeyStore.java:1479)
	at java.base/sun.security.tools.keytool.Main.loadSourceKeyStore(Main.java:2142)
	at java.base/sun.security.tools.keytool.Main.doCommands(Main.java:1184)
	at java.base/sun.security.tools.keytool.Main.run(Main.java:397)
	at java.base/sun.security.tools.keytool.Main.main(Main.java:390)
Caused by: java.lang.SecurityException: Can not initialize cryptographic mechanism
	at java.base/javax.crypto.JceSecurity.<clinit>(JceSecurity.java:118)
	... 11 more
Caused by: java.lang.SecurityException: Couldn't parse jurisdiction policy files in: unlimited
	at java.base/javax.crypto.JceSecurity.setupJurisdictionPolicies(JceSecurity.java:355)
	at java.base/javax.crypto.JceSecurity.access$000(JceSecurity.java:73)
	at java.base/javax.crypto.JceSecurity$1.run(JceSecurity.java:109)
	at java.base/javax.crypto.JceSecurity$1.run(JceSecurity.java:106)
	at java.base/java.security.AccessController.doPrivileged(Native Method)
	at java.base/javax.crypto.JceSecurity.<clinit>(JceSecurity.java:105)
	... 11 more
failed to convert PKCS12 keystore to JKS
dpkg: Fehler beim Bearbeiten des Paketes ca-certificates-java (--configure):
 Unterprozess installed ca-certificates-java package post-installation script gab den Fehler-Ausgangsstatus 1 zurück
dpkg: Abhängigkeitsprobleme verhindern Konfiguration von openjdk-11-jre-headless:amd64:
 openjdk-11-jre-headless:amd64 hängt ab von ca-certificates-java; aber:
  Paket ca-certificates-java ist noch nicht konfiguriert.

dpkg: Fehler beim Bearbeiten des Paketes openjdk-11-jre-headless:amd64 (--configure):
 Abhängigkeitsprobleme - verbleibt unkonfiguriert
dpkg: Abhängigkeitsprobleme verhindern Konfiguration von openjdk-11-jdk-headless:amd64:
 openjdk-11-jdk-headless:amd64 hängt ab von openjdk-11-jre-headless (= 10.0.2+13-1ubuntu0.18.04.4); aber:
  Paket openjdk-11-jre-headless:amd64 ist noch nicht konfiguriert.

dpkg: Fehler beim Bearbeiten des Paketes openjdk-11-jdk-headless:amd64 (--configure):
 Abhängigkeitsprobleme - verbleibt unkonfiguriert
dpkg: Abhängigkeitsprobleme verhindern Konfiguration von openjdk-11-jdk:amd64:
 openjdk-11-jdk:amd64 hängt ab von openjdk-11-jdk-headless (= 10.0.2+13-1ubuntu0.18.04.4); aber:
  Paket openjdk-11-jdk-headless:amd64 ist noch nicht konfiguriert.

dpkg: Fehler beim Bearbeiten des Paketes openjdk-11-jdk:amd64 (--configure):
 Abhängigkeitsprobleme - verbleibt unkonfiguriert
dpkg: Abhängigkeitsprobleme verhindern Konfiguration von openjdk-11-jre:amd64:
 openjdk-11-jre:amd64 hängt ab von openjdk-11-jre-headless (= 10.0.2+13-1ubuntu0.18.04.4); aber:
  Paket openjdk-11-jre-headless:amd64 ist noch nicht konfiguriert.

dpkg: Fehler beim Bearbeiten des Paketes openjdk-11-jre:amd64 (--configure):
 Abhängigkeitsprobleme - verbleibt unkonfiguriert
Trigger für ca-certificates (20180409) werden verarbeitet ...
Updating certificates in /etc/ssl/certs...
0 added, 0 removed; done.
Running hooks in /etc/ca-certificates/update.d...

org.debian.security.InvalidKeystorePasswordException: Cannot open Java keystore. Is the password correct?
	at org.debian.security.KeyStoreHandler.load(KeyStoreHandler.java:68)
	at org.debian.security.KeyStoreHandler.<init>(KeyStoreHandler.java:52)
	at org.debian.security.UpdateCertificates.<init>(UpdateCertificates.java:65)
	at org.debian.security.UpdateCertificates.main(UpdateCertificates.java:51)
Caused by: java.io.IOException: Invalid keystore format
	at java.base/sun.security.provider.JavaKeyStore.engineLoad(JavaKeyStore.java:659)
	at java.base/sun.security.util.KeyStoreDelegator.engineLoad(KeyStoreDelegator.java:222)
	at java.base/java.security.KeyStore.load(KeyStore.java:1479)
	at org.debian.security.KeyStoreHandler.load(KeyStoreHandler.java:66)
	... 3 more
E: /etc/ca-certificates/update.d/jks-keystore exited with code 1.
done.
Fehler traten auf beim Bearbeiten von:
 ca-certificates-java
 openjdk-11-jre-headless:amd64
 openjdk-11-jdk-headless:amd64
 openjdk-11-jdk:amd64
 openjdk-11-jre:amd64
```
Anscheinend klappt die Konfiguration des Paketes `ca-certificates-java` nicht. Denn im Log erscheint 
```
Keystore /etc/ssl/certs/java/cacerts wird in /etc/ssl/certs/java/cacerts.dpkg-new importiert
...
failed to convert PKCS12 keystore to JKS
dpkg: Fehler beim Bearbeiten des Paketes ca-certificates-java (--configure):
```

ALSO: Versuch, das Paket `ca-certificates-java` auf der Kommandozeile zu installieren:
`apt-get install ca-certificates-java`
