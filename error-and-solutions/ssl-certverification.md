---
description: SSLCertVerificationError
---

# SSL CertVerification

Two-line solution

```python
import ssl
ssl._create_default_https_context = ssl._create_unverified_context # set certificate for scraper
```



