PS C:\dev\Developer\sk-sandbox-backend> pip list
Package    Version
---------- -------
pip        19.2.3
setuptools 41.2.0
Could not fetch URL https://pypi.org/simple/pip/: There was a problem confirming the ssl certificate: HTTPSConnectionPool(host='pypi.org', port=443): Max retries exceeded with url: /simple/pip/ (Caused by SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: unable to get local issuer certificate (_ssl.c:1108)'))) - skipping
PS C:\dev\Developer\sk-sandbox-backend> pip config list
global.cert='C:\\dev\\certs\\ca-certificates.crt'
PS C:\dev\Developer\sk-sandbox-backend> pip config set global.trusted-host tools.rbspeople.com
Writing to C:\Users\dzikohn\AppData\Roaming\pip\pip.ini
PS C:\dev\Developer\sk-sandbox-backend> pip list
Package    Version
---------- -------
pip        19.2.3
setuptools 41.2.0
Could not fetch URL https://pypi.org/simple/pip/: There was a problem confirming the ssl certificate: HTTPSConnectionPool(host='pypi.org', port=443): Max retries exceeded with url: /simple/pip/ (Caused by SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: unable to get local issuer certificate (_ssl.c:1108)'))) - skipping
PS C:\dev\Developer\sk-sandbox-backend>
