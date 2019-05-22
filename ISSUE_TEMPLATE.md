Make sure you have provided the following information:

 - [ ] link to your code branch cloned from rhboot/shim-review in the form user/repo@tag
 - [x] completed README.md file with the necessary information
 - [x] shim.efi to be signed
 - [x] public portion of your certificate embedded in shim (the file passed to VENDOR_CERT_FILE)
 - [x] any extra patches to shim via your own git tree or as files
 - [x] any extra patches to grub via your own git tree or as files
 - [x] build logs


###### What organization or people are asking to have this signed:
Oracle Corporation

###### What product or service is this for:
Oracle Linux
https://www.oracle.com/linux/index.html

###### What is the origin and full version number of your shim?
We used upstream shim version 15
https://github.com/rhboot/shim/releases/tag/15

###### What's the justification that this really does need to be signed for the whole world to be able to boot it:
Oracle Linux is a popular enterprise Linux distribution with Secure Boot support.

###### How do you manage and protect the keys used in your SHIM?
The key is installed in the server with restricted physical and system access

###### Do you use EV certificates as embedded certificates in the SHIM?
Yes

###### What is the origin and full version number of your bootloader (GRUB or other)?
grub2 - upstream plus number of patches from RedHat and Oracle

###### If your SHIM launches any other components, please provide further details on what is launched
`[your text here]`

###### How do the launched components prevent execution of unauthenticated code?
grub verifies signatures on booted kernels

###### Does your SHIM load any loaders that support loading unsigned kernels (e.g. GRUB)?
No

###### What kernel are you using? Which patches does it includes to enforce Secure Boot?
4.18 based kernel with lockdown patches

###### What changes were made since your SHIM was last signed?
This is the first shim build for Oracle Linux 8

###### What is the hash of your final SHIM binary?
a6a559aa2473153a0300f83154e40a0b4ba0e3463b504c101dee80aac7918ef4  shimia32.efi
beb1fce87097df87abea14a98bf233f99e85c2041f8b99b36bbdd3b529980899  shimx64.efi

Public certificate:
-----BEGIN CERTIFICATE-----
MIIF2zCCBMOgAwIBAgIQA+YFGHHEE60dWTdlqxCjpDANBgkqhkiG9w0BAQsFADBs
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSswKQYDVQQDEyJEaWdpQ2VydCBFViBDb2RlIFNpZ25p
bmcgQ0EgKFNIQTIpMB4XDTE4MTAwODAwMDAwMFoXDTIxMTIyMjEyMDAwMFowgfEx
EzARBgsrBgEEAYI3PAIBAxMCVVMxGTAXBgsrBgEEAYI3PAIBAhMIRGVsYXdhcmUx
HTAbBgNVBA8MFFByaXZhdGUgT3JnYW5pemF0aW9uMRAwDgYDVQQFEwc0MDI4MTI1
MQswCQYDVQQGEwJVUzETMBEGA1UECBMKQ2FsaWZvcm5pYTEVMBMGA1UEBxMMUmVk
d29vZCBDaXR5MRswGQYDVQQKExJPcmFjbGUgQ29ycG9yYXRpb24xGzAZBgNVBAsT
Ek9yYWNsZSBDb3Jwb3JhdGlvbjEbMBkGA1UEAxMST3JhY2xlIENvcnBvcmF0aW9u
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAkvcd/qAEUeN9JpqzSGuh
7Azuy9FN2+ZwOZ0/WqWGBOxnDbVAKDIAxMT/XdezrtRGzGHwEDrKU3Wo1SOsZeNa
DXCy4mWxiXwYj4rvoDbwpq+uqFBs3fies1/YpHkx8SsOhuDGFdmLaXriYh8QyNHy
gqYUeaYNAcN4h7Cpxzthp3ER6Xx9giI597Ee9UArXzgmPH54UbJs2+8xflz9M7n4
GUhf9cTMmd1StSM0gJ6JmyTtqjl/QjCTFho6lN1MeWxKPBcUBP3ThQi3cEqvGixc
SwQ2ILbg3a+qXGa3EozK7FlZFf+bnRVu8wBECBh6oR+3P0TTeKWh2hZ9Tmjbxe1G
nwIDAQABo4IB8TCCAe0wHwYDVR0jBBgwFoAUj+h+8G0yagAFI8dwl2o6kP9r6tQw
HQYDVR0OBBYEFH9Vm46dngUYNICnFJ5aHeC8JlraMC4GA1UdEQQnMCWgIwYIKwYB
BQUHCAOgFzAVDBNVUy1ERUxBV0FSRS00MDI4MTI1MA4GA1UdDwEB/wQEAwIHgDAT
BgNVHSUEDDAKBggrBgEFBQcDAzB7BgNVHR8EdDByMDegNaAzhjFodHRwOi8vY3Js
My5kaWdpY2VydC5jb20vRVZDb2RlU2lnbmluZ1NIQTItZzEuY3JsMDegNaAzhjFo
dHRwOi8vY3JsNC5kaWdpY2VydC5jb20vRVZDb2RlU2lnbmluZ1NIQTItZzEuY3Js
MEsGA1UdIAREMEIwNwYJYIZIAYb9bAMCMCowKAYIKwYBBQUHAgEWHGh0dHBzOi8v
d3d3LmRpZ2ljZXJ0LmNvbS9DUFMwBwYFZ4EMAQMwfgYIKwYBBQUHAQEEcjBwMCQG
CCsGAQUFBzABhhhodHRwOi8vb2NzcC5kaWdpY2VydC5jb20wSAYIKwYBBQUHMAKG
PGh0dHA6Ly9jYWNlcnRzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEVWQ29kZVNpZ25p
bmdDQS1TSEEyLmNydDAMBgNVHRMBAf8EAjAAMA0GCSqGSIb3DQEBCwUAA4IBAQAv
yMvkUcvctEwi+tJSviZ9TpvhI/pQvNpRoMyPkI3zlNWb6b+luJ0KLr3vgJRIk7un
u37gYJ6AfBnPrXmGyJykp13+qE5Xr/LBkvnpwIxxwjELLttRIi4u5aG7N/shIRcM
ASORa02c8TO1SeoxwjXcuTveGDJE4hmCMD19FMUKMf5bZJNFLyhl+XavG+mAAXZ2
YIp69dO8Q1CCIXzg6MJ45j7nSaXf6akAX2bm0IfJpXhUwfHM0rUGCyQI2TQwpp+/
8eg8hkganUOOPhZA1V5MVg8jFME9WnL08Zyrf7fH7M9rTOR+Y88JOtogmb698P3g
aE3h/+nD3ZP72Yj5AXhK
-----END CERTIFICATE-----
