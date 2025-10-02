---
title: Security Considerations — Python 3.13.7 documentation
source: https://docs.python.org/3/library/security_warnings.html
---

# Security Considerations — Python 3.13.7 documentation


















Security Considerations — Python 3.13.7 documentation




















































    Theme
    
Auto
Light
Dark



Previous topic
xdrlib — Encode and decode XDR data


Next topic
Extending and Embedding the Python Interpreter


This page

Report a bug

Show source
        







Navigation


index

modules |

next |

previous |

Python »







3.13.7 Documentation »
    
The Python Standard Library »
Security Considerations







                     |
                


    Theme
    
Auto
Light
Dark

 |







Security Considerations¶
The following modules have specific security considerations:

base64: base64 security considerations in
RFC 4648
hashlib: all constructors take a “usedforsecurity” keyword-only
argument disabling known insecure and blocked algorithms
http.server is not suitable for production use, only implementing
basic security checks. See the security considerations.
logging: Logging configuration uses eval()
multiprocessing: Connection.recv() uses pickle
pickle: Restricting globals in pickle
random shouldn’t be used for security purposes, use secrets
instead
shelve: shelve is based on pickle and thus unsuitable for
dealing with untrusted sources
ssl: SSL/TLS security considerations
subprocess: Subprocess security considerations
tempfile: mktemp is deprecated due to vulnerability to race
conditions
xml: XML security
zipfile: maliciously prepared .zip files can cause disk volume
exhaustion

The -I command line option can be used to run Python in isolated
mode. When it cannot be used, the -P option or the
PYTHONSAFEPATH environment variable can be used to not prepend a
potentially unsafe path to sys.path such as the current directory, the
script’s directory or an empty string.








Previous topic
xdrlib — Encode and decode XDR data


Next topic
Extending and Embedding the Python Interpreter


This page

Report a bug

Show source
        





«





Navigation


index

modules |

next |

previous |

Python »







3.13.7 Documentation »
    
The Python Standard Library »
Security Considerations







                     |
                


    Theme
    
Auto
Light
Dark

 |



    © Copyright 2001-2025, Python Software Foundation.
    
    This page is licensed under the Python Software Foundation License Version 2.
    
    Examples, recipes, and other code in the documentation are additionally licensed under the Zero Clause BSD License.
    
    
      See History and License for more information.


    The Python Software Foundation is a non-profit corporation.
Please donate.


      Last updated on Oct 02, 2025 (07:37 UTC).
    
      Found a bug?
    
    

    Created using Sphinx 8.2.3.
    


