# Install trusted certificates for Java applications 🛅

When trying to make Http requests from Java applications to certain domains or even localhost (for JDK 1.8), an error is triggered:

```PKIX path building failed: sun.security.provider.certpath.SunCertPathBuilderException: unable to find valid certification path to requested target```

In order to solve this issue, you'll need to insert new certificates to allow TLS. 💻-------💻

## Run Project

- Clone the project 

```bash
  git clone https://github.com/ramong1145/java-InstallTrustedCertificates
```

- Go to the project main class directory:

```bash
  cd java-InstallTrustedCertificates/src
```

- Run Project 🚀

Pass the domains you want to add. Ports and Passphrase are optional:

```bash
  java InstallCert.java <host>[:port] [passphrase]
```

- Enter certificate to add to trusted keystore. ENTER to continue. Q to quit and rollback.

- In root directory, there should be a new file ```jssecacerts```. Move this file to: ```JDK_HOME\jre\lib\security\``` folder.
*PRO TIP: Backup your previous ```cacerts``` file* 😉
- Rename file to ```cacerts``` and replace the previous one. 



  
## Tech Stack

**Language:** Java ☕
  
## Optimizations

What optimizations did you make in your code? E.g. refactors, performance improvements, accessibility

- File rename and replace should be done by the application (@ramong1145)

  
## Feedback

If you have any feedback, please reach out to me directly: ramong1145@gmail.com

  
