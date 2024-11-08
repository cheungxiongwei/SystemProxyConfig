# SystemProxyConfig

`SystemProxyConfig` is a Windows system proxy configuration utility that allows you to set system proxy settings
programmatically. It can be used in tools like v2ray, trojan-go, and other similar tools that require setting the
`System IE proxy`.

### Usage

```c++
#include "SystemProxyConfig.h"

int main()
{
    SystemProxyConfig proxy;

    // query proxy
    proxy.getServerAddress();
    proxy.getBypass();
    proxy.proxyEnabled();

    // setting proxy
    proxy.setServerAddress("127.0.0.1:1080");
    proxy.setBypass("localhost;127.*;192.168.*");
    proxy.setProxyEnabled(true);
    proxy.apply();
    return 0;
}
```
