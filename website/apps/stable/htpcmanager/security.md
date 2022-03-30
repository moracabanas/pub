---
hide:
  - toc
---

# Security Overview

<link href="https://truecharts.org/_static/trivy.css" type="text/css" rel="stylesheet" />

## Helm-Chart

##### Scan Results

#### Chart Object: htpcmanager/templates/common.yaml



| Type         |    Misconfiguration ID   |   Check  |  Severity |                   Explaination                   | Links  |
|:----------------|:------------------:|:-----------:|:------------------:|-----------------------------------------|-----------------------------------------|
| Kubernetes Security Check         |    KSV001   |   Process can elevate its own privileges  |  MEDIUM | <details><summary>Expand...</summary> A program inside the container can elevate its own privileges and run as root, which might give the program control over the container and node. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.allowPrivilegeEscalation&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv001">https://avd.aquasec.com/appshield/ksv001</a><br></details>  |
| Kubernetes Security Check         |    KSV003   |   Default capabilities not dropped  |  LOW | <details><summary>Expand...</summary> The container should drop all default capabilities and add only those that are needed for its execution. <br> <hr> <br> Container &#39;RELEASE-NAME-htpcmanager&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should add &#39;ALL&#39; to &#39;securityContext.capabilities.drop&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/">https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/</a><br><a href="https://avd.aquasec.com/appshield/ksv003">https://avd.aquasec.com/appshield/ksv003</a><br></details>  |
| Kubernetes Security Check         |    KSV003   |   Default capabilities not dropped  |  LOW | <details><summary>Expand...</summary> The container should drop all default capabilities and add only those that are needed for its execution. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should add &#39;ALL&#39; to &#39;securityContext.capabilities.drop&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/">https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/</a><br><a href="https://avd.aquasec.com/appshield/ksv003">https://avd.aquasec.com/appshield/ksv003</a><br></details>  |
| Kubernetes Security Check         |    KSV011   |   CPU not limited  |  LOW | <details><summary>Expand...</summary> Enforcing CPU limits prevents DoS via resource exhaustion. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;resources.limits.cpu&#39; </details>| <details><summary>Expand...</summary><a href="https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits">https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits</a><br><a href="https://avd.aquasec.com/appshield/ksv011">https://avd.aquasec.com/appshield/ksv011</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;RELEASE-NAME-htpcmanager&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;RELEASE-NAME-htpcmanager&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV015   |   CPU requests not specified  |  LOW | <details><summary>Expand...</summary> When containers have resource requests specified, the scheduler can make better decisions about which nodes to place pods on, and how to deal with resource contention. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;resources.requests.cpu&#39; </details>| <details><summary>Expand...</summary><a href="https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits">https://cloud.google.com/blog/products/containers-kubernetes/kubernetes-best-practices-resource-requests-and-limits</a><br><a href="https://avd.aquasec.com/appshield/ksv015">https://avd.aquasec.com/appshield/ksv015</a><br></details>  |
| Kubernetes Security Check         |    KSV016   |   Memory requests not specified  |  LOW | <details><summary>Expand...</summary> When containers have memory requests specified, the scheduler can make better decisions about which nodes to place pods on, and how to deal with resource contention. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;resources.requests.memory&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-resources-limits-memory/">https://kubesec.io/basics/containers-resources-limits-memory/</a><br><a href="https://avd.aquasec.com/appshield/ksv016">https://avd.aquasec.com/appshield/ksv016</a><br></details>  |
| Kubernetes Security Check         |    KSV017   |   Privileged container  |  HIGH | <details><summary>Expand...</summary> Privileged containers share namespaces with the host system and do not offer any security. They should be used exclusively for system containers that require high privileges. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.privileged&#39; to false </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/appshield/ksv017">https://avd.aquasec.com/appshield/ksv017</a><br></details>  |
| Kubernetes Security Check         |    KSV018   |   Memory not limited  |  LOW | <details><summary>Expand...</summary> Enforcing memory limits prevents DoS via resource exhaustion. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;resources.limits.memory&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-resources-limits-memory/">https://kubesec.io/basics/containers-resources-limits-memory/</a><br><a href="https://avd.aquasec.com/appshield/ksv018">https://avd.aquasec.com/appshield/ksv018</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-htpcmanager&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-htpcmanager&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;hostpatch&#39; of Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV023   |   hostPath volumes mounted  |  MEDIUM | <details><summary>Expand...</summary> HostPath volumes must be forbidden. <br> <hr> <br> Deployment &#39;RELEASE-NAME-htpcmanager&#39; should not set &#39;spec.template.volumes.hostPath&#39; </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline">https://kubernetes.io/docs/concepts/security/pod-security-standards/#baseline</a><br><a href="https://avd.aquasec.com/appshield/ksv023">https://avd.aquasec.com/appshield/ksv023</a><br></details>  |
| Kubernetes Security Check         |    KSV029   |   A root primary or supplementary GID set  |  LOW | <details><summary>Expand...</summary> Containers should be forbidden from running with a root primary or supplementary GID. <br> <hr> <br> Deployment &#39;RELEASE-NAME-htpcmanager&#39; should set &#39;spec.securityContext.runAsGroup&#39;, &#39;spec.securityContext.supplementalGroups[*]&#39; and &#39;spec.securityContext.fsGroup&#39; to integer greater than 0 </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv029">https://avd.aquasec.com/appshield/ksv029</a><br></details>  |

## Containers

##### Detected Containers

          tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583
          tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583
          tccr.io/truecharts/htpcmanager:v2021.11.17

##### Scan Results


#### Container: tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583 (alpine 3.15.2)


**alpine**


| No Vulnerabilities found         |
|:---------------------------------|




#### Container: tccr.io/truecharts/alpine:v3.15.2@sha256:29ed3480a0ee43f7af681fed5d4fc215516abf1c41eade6938b26d8c9c2c7583 (alpine 3.15.2)


**alpine**


| No Vulnerabilities found         |
|:---------------------------------|




#### Container: Python


**python-pkg**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| Pillow         |    CVE-2022-22815   |   CRITICAL  |  8.4.0 | 9.0.0 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-22815">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-22815</a><br><a href="https://github.com/advisories/GHSA-pw3c-h7wp-cvhx">https://github.com/advisories/GHSA-pw3c-h7wp-cvhx</a><br><a href="https://github.com/python-pillow/Pillow/blob/c5d9223a8b5e9295d15b5a9b1ef1dae44c8499f3/src/path.c#L331">https://github.com/python-pillow/Pillow/blob/c5d9223a8b5e9295d15b5a9b1ef1dae44c8499f3/src/path.c#L331</a><br><a href="https://github.com/python-pillow/Pillow/commit/c48271ab354db49cdbd740bc45e13be4f0f7993c">https://github.com/python-pillow/Pillow/commit/c48271ab354db49cdbd740bc45e13be4f0f7993c</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/01/msg00018.html">https://lists.debian.org/debian-lts-announce/2022/01/msg00018.html</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-22815">https://nvd.nist.gov/vuln/detail/CVE-2022-22815</a><br><a href="https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#fixed-imagepath-path-array-handling">https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#fixed-imagepath-path-array-handling</a><br><a href="https://ubuntu.com/security/notices/USN-5227-1">https://ubuntu.com/security/notices/USN-5227-1</a><br><a href="https://ubuntu.com/security/notices/USN-5227-2">https://ubuntu.com/security/notices/USN-5227-2</a><br><a href="https://www.debian.org/security/2022/dsa-5053">https://www.debian.org/security/2022/dsa-5053</a><br></details>  |
| Pillow         |    CVE-2022-22817   |   CRITICAL  |  8.4.0 | 9.0.1 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-22817">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-22817</a><br><a href="https://github.com/advisories/GHSA-8vj2-vxx3-667w">https://github.com/advisories/GHSA-8vj2-vxx3-667w</a><br><a href="https://github.com/python-pillow/Pillow/commit/8531b01d6cdf0b70f256f93092caa2a5d91afc11">https://github.com/python-pillow/Pillow/commit/8531b01d6cdf0b70f256f93092caa2a5d91afc11</a><br><a href="https://linux.oracle.com/cve/CVE-2022-22817.html">https://linux.oracle.com/cve/CVE-2022-22817.html</a><br><a href="https://linux.oracle.com/errata/ELSA-2022-0643.html">https://linux.oracle.com/errata/ELSA-2022-0643.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/01/msg00018.html">https://lists.debian.org/debian-lts-announce/2022/01/msg00018.html</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-22817">https://nvd.nist.gov/vuln/detail/CVE-2022-22817</a><br><a href="https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#fixed-imagepath-path-array-handling">https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#fixed-imagepath-path-array-handling</a><br><a href="https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#restrict-builtins-available-to-imagemath-eval">https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#restrict-builtins-available-to-imagemath-eval</a><br><a href="https://pillow.readthedocs.io/en/stable/releasenotes/9.0.1.html#security">https://pillow.readthedocs.io/en/stable/releasenotes/9.0.1.html#security</a><br><a href="https://ubuntu.com/security/notices/USN-5227-1">https://ubuntu.com/security/notices/USN-5227-1</a><br><a href="https://ubuntu.com/security/notices/USN-5227-2">https://ubuntu.com/security/notices/USN-5227-2</a><br><a href="https://www.debian.org/security/2022/dsa-5053">https://www.debian.org/security/2022/dsa-5053</a><br></details>  |
| Pillow         |    CVE-2022-22816   |   MEDIUM  |  8.4.0 | 9.0.0 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-22816">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-22816</a><br><a href="https://github.com/advisories/GHSA-xrcv-f9gm-v42c">https://github.com/advisories/GHSA-xrcv-f9gm-v42c</a><br><a href="https://github.com/python-pillow/Pillow/blob/c5d9223a8b5e9295d15b5a9b1ef1dae44c8499f3/src/path.c#L331">https://github.com/python-pillow/Pillow/blob/c5d9223a8b5e9295d15b5a9b1ef1dae44c8499f3/src/path.c#L331</a><br><a href="https://linux.oracle.com/cve/CVE-2022-22816.html">https://linux.oracle.com/cve/CVE-2022-22816.html</a><br><a href="https://linux.oracle.com/errata/ELSA-2022-0643.html">https://linux.oracle.com/errata/ELSA-2022-0643.html</a><br><a href="https://lists.debian.org/debian-lts-announce/2022/01/msg00018.html">https://lists.debian.org/debian-lts-announce/2022/01/msg00018.html</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-22816">https://nvd.nist.gov/vuln/detail/CVE-2022-22816</a><br><a href="https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#fixed-imagepath-path-array-handling">https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#fixed-imagepath-path-array-handling</a><br><a href="https://ubuntu.com/security/notices/USN-5227-1">https://ubuntu.com/security/notices/USN-5227-1</a><br><a href="https://ubuntu.com/security/notices/USN-5227-2">https://ubuntu.com/security/notices/USN-5227-2</a><br><a href="https://www.debian.org/security/2022/dsa-5053">https://www.debian.org/security/2022/dsa-5053</a><br></details>  |
| Pillow         |    CVE-2022-24303   |   MEDIUM  |  8.4.0 | 9.0.1 | <details><summary>Expand...</summary><a href="https://github.com/advisories/GHSA-9j59-75qj-795w">https://github.com/advisories/GHSA-9j59-75qj-795w</a><br><a href="https://github.com/python-pillow/Pillow/commit/427221ef5f19157001bf8b1ad7cfe0b905ca8c26">https://github.com/python-pillow/Pillow/commit/427221ef5f19157001bf8b1ad7cfe0b905ca8c26</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2022-24303">https://nvd.nist.gov/vuln/detail/CVE-2022-24303</a><br><a href="https://pillow.readthedocs.io/en/stable/releasenotes/9.0.1.html">https://pillow.readthedocs.io/en/stable/releasenotes/9.0.1.html</a><br><a href="https://pillow.readthedocs.io/en/stable/releasenotes/9.0.1.html#security">https://pillow.readthedocs.io/en/stable/releasenotes/9.0.1.html#security</a><br></details>  |
| Pillow         |    GHSA-4fx9-vc88-q2xc   |   LOW  |  8.4.0 | 9.0.0 | <details><summary>Expand...</summary><a href="https://github.com/advisories/GHSA-4fx9-vc88-q2xc">https://github.com/advisories/GHSA-4fx9-vc88-q2xc</a><br><a href="https://github.com/python-pillow/Pillow/commit/baae9ec4b67c68e3adaf1208cf54e8de5e38a6fd">https://github.com/python-pillow/Pillow/commit/baae9ec4b67c68e3adaf1208cf54e8de5e38a6fd</a><br><a href="https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#ensure-jpegimageplugin-stops-at-the-end-of-a-truncated-file">https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#ensure-jpegimageplugin-stops-at-the-end-of-a-truncated-file</a><br></details>  |
| Pillow         |    pyup.io-44524   |   UNKNOWN  |  8.4.0 | 9.0.0 | <details><summary>Expand...</summary></details>  |
| Pillow         |    pyup.io-44525   |   UNKNOWN  |  8.4.0 | 9.0.0 | <details><summary>Expand...</summary></details>  |

**cargo**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| chrono         |    RUSTSEC-2020-0159   |   UNKNOWN  |  0.4.19 |  | <details><summary>Expand...</summary><a href="https://github.com/chronotope/chrono/issues/499">https://github.com/chronotope/chrono/issues/499</a><br></details>  |

**cargo**


| No Vulnerabilities found         |
|:---------------------------------|



**cargo**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| crossbeam-deque         |    RUSTSEC-2021-0093   |   UNKNOWN  |  0.7.3 | &gt;= 0.7.4, &lt; 0.8.0, &gt;= 0.8.1 | <details><summary>Expand...</summary><a href="https://github.com/crossbeam-rs/crossbeam/security/advisories/GHSA-pqqp-xmhj-wgcw">https://github.com/crossbeam-rs/crossbeam/security/advisories/GHSA-pqqp-xmhj-wgcw</a><br></details>  |
| regex         |    RUSTSEC-2022-0013   |   UNKNOWN  |  1.3.9 | &gt;= 1.5.5 | <details><summary>Expand...</summary><a href="https://groups.google.com/g/rustlang-security-announcements/c/NcNNL1Jq7Yw">https://groups.google.com/g/rustlang-security-announcements/c/NcNNL1Jq7Yw</a><br></details>  |

**cargo**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| regex         |    RUSTSEC-2022-0013   |   UNKNOWN  |  1.2.0 | &gt;= 1.5.5 | <details><summary>Expand...</summary><a href="https://groups.google.com/g/rustlang-security-announcements/c/NcNNL1Jq7Yw">https://groups.google.com/g/rustlang-security-announcements/c/NcNNL1Jq7Yw</a><br></details>  |
| thread_local         |    RUSTSEC-2022-0006   |   UNKNOWN  |  0.3.6 | &gt;= 1.1.4 | <details><summary>Expand...</summary><a href="https://github.com/Amanieu/thread_local-rs/issues/33">https://github.com/Amanieu/thread_local-rs/issues/33</a><br></details>  |

**cargo**


| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| regex         |    RUSTSEC-2022-0013   |   UNKNOWN  |  1.5.4 | &gt;= 1.5.5 | <details><summary>Expand...</summary><a href="https://groups.google.com/g/rustlang-security-announcements/c/NcNNL1Jq7Yw">https://groups.google.com/g/rustlang-security-announcements/c/NcNNL1Jq7Yw</a><br></details>  |

**cargo**


| No Vulnerabilities found         |
|:---------------------------------|