# SystemProxyConfig

`SystemProxyConfig` is a Windows system proxy configuration utility that allows you to set system proxy settings
programmatically. It can be used in tools like v2ray, trojan-go, and other similar tools that require setting the
`System IE proxy`.

### Usage

```c++
#include <print>
#include <string>
#include "SystemProxyConfig.h"

int main()
{
    auto proxy = SystemProxy::Builder().SetMode(SystemProxy::Pac).SetPacUrl("http://example.com/proxy.pac").Build();
    proxy->ApplyConfig();

    // 基于现有配置创建新配置
    auto newBuilder = proxy->GetBuilder();
    auto modifiedProxy = newBuilder->SetMode(SystemProxy::Manual).SetProxy("localhost", "8080").Build();

    return 0;
}
```

```json

```