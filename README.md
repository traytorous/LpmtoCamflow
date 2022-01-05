# LPM functionality to Camflow
-----------------------------

### Authors Tray Keller and Austin Waddell

CamFlow and the Linux Provenance Module (LPM) framework 
are both an excellent step in the right direction for whole-
system provenance, but each have weaknesses. For LPM, the
most significant downside is the difficulty in maintaining
code across updates to the Linux kernel, as LPM had to duplicate 
the Linux Security Modules framework in order to allow
stacking provenance collection with other functionality. In
contrast, CamFlow makes use of Netfilter hooks and advances
in LSM modules to greatly reduce the amount of code which
must be changed between kernel releases, making the design
more modular by implementing the provenance feature using
kernel modules. However, CamFlow’s network provenance
collection has room for improvement, as its method of packet
labeling is not scalable, in contrast with LPM’s packet labeling methods.
To address this scalability issue, we have ported
selected parts of LPM’s networking code to CamFlow.

(Full paper is inside of the pdf)
