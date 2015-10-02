## Python script to generate a malicious MP4 file exploiting the 'stsc' vulnerability (CVE-2015-1538) (#1),
and start reverse TCP listener on attacker machine.

## author: vvn (eudemonics)

### built upon original exploit code from @jduck

Original README:

    Included is a python script that generates an MP4 exploiting the ‘stsc’ vulnerability otherwise known as CVE-2015-1538 (#1). This is one of the most critical vulnerabilities I reported in the Stagefright library. The expected result of the exploit is a reverse shell as the media user. As detailed in my Black Hat and DEF CON presentations, this user also has access to quite a few groups such as inet, audio, camera, and mediadrm. These groups allow an attacker to take pictures or listen to the microphone remotely without exploiting additional vulnerabilities.

    This exploit has several caveats. First, it is not a generic exploit. It's only been tested to work on a single device model. My target was the Galaxy Nexus device running Android 4.0.4 containing only a partial implementation of ASLR. Also, due to variances in heap layout, this is not a 100% reliable exploit by itself. However, I was able achieve 100% reliability when delivered through an attack vector that allowed multiple attempts. Finally, this vulnerability was one of several that was neutered by GCC 5.0’s ‘new[]’ integer overflow mitigation present on Android 5.0 and later.

    Enjoy! Please consider contributing to Android security through research!
