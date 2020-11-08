---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096496"
---
# <span data-ttu-id="332ce-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="332ce-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="332ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="332ce-102">SYNOPSIS</span></span>
<span data-ttu-id="332ce-103">TCP, HTTP veya ıCMP üzerinden test değerlendirmesi gerçekleştirmek için kullanılan protokol yapılandırması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="332ce-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="332ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="332ce-104">SYNTAX</span></span>

### <span data-ttu-id="332ce-105">TC</span><span class="sxs-lookup"><span data-stu-id="332ce-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="332ce-106">HTTP</span><span class="sxs-lookup"><span data-stu-id="332ce-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="332ce-107">ICMP</span><span class="sxs-lookup"><span data-stu-id="332ce-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="332ce-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="332ce-108">DESCRIPTION</span></span>
<span data-ttu-id="332ce-109">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet, TCP, HTTP veya ıCMP üzerinden test değerlendirmesi gerçekleştirmek için kullanılan protokol yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="332ce-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="332ce-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="332ce-110">EXAMPLES</span></span>

### <span data-ttu-id="332ce-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="332ce-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="332ce-112">Bağlantı noktası: 80 Disable, Oute: false</span><span class="sxs-lookup"><span data-stu-id="332ce-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="332ce-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="332ce-113">PARAMETERS</span></span>

### <span data-ttu-id="332ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="332ce-114">-DefaultProfile</span></span>
<span data-ttu-id="332ce-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="332ce-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-116">-Disable, Oute</span><span class="sxs-lookup"><span data-stu-id="332ce-116">-DisableTraceRoute</span></span>
<span data-ttu-id="332ce-117">İzleme rotası ile yol değerlendirmenin devre dışı bırakılıp bırakılmadığını gösteren değer.</span><span class="sxs-lookup"><span data-stu-id="332ce-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="332ce-118">-HttpProtocol</span></span>
<span data-ttu-id="332ce-119">HTTP protokolü anahtarı</span><span class="sxs-lookup"><span data-stu-id="332ce-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="332ce-120">-IcmpProtocol</span></span>
<span data-ttu-id="332ce-121">ICMP Protokolü anahtarı.</span><span class="sxs-lookup"><span data-stu-id="332ce-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-122">-Yöntem</span><span class="sxs-lookup"><span data-stu-id="332ce-122">-Method</span></span>
<span data-ttu-id="332ce-123">Kullanılacak HTTP yöntemi.</span><span class="sxs-lookup"><span data-stu-id="332ce-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-124">-Yol</span><span class="sxs-lookup"><span data-stu-id="332ce-124">-Path</span></span>
<span data-ttu-id="332ce-125">URI 'nin yol bileşeni.</span><span class="sxs-lookup"><span data-stu-id="332ce-125">The path component of the URI.</span></span> <span data-ttu-id="332ce-126">Örneğin, \" /dir1/dir2 \" .</span><span class="sxs-lookup"><span data-stu-id="332ce-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-127">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="332ce-127">-Port</span></span>
<span data-ttu-id="332ce-128">Bağlanılacak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="332ce-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="332ce-129">-PreferHTTPS</span></span>
<span data-ttu-id="332ce-130">Seçeneğin açık olmadığı durumlarda HTTPS 'nin HTTP üzerinden tercih edilip edilmeyeceğini gösteren değer.</span><span class="sxs-lookup"><span data-stu-id="332ce-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="332ce-131">-RequestHeader</span></span>
<span data-ttu-id="332ce-132">İstekle birlikte iletilecek HTTP üstbilgileri.</span><span class="sxs-lookup"><span data-stu-id="332ce-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="332ce-133">-TcpProtocol</span></span>
<span data-ttu-id="332ce-134">TCP iletişim kuralı anahtarı.</span><span class="sxs-lookup"><span data-stu-id="332ce-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="332ce-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="332ce-136">Başarılı olacak HTTP durum kodları.</span><span class="sxs-lookup"><span data-stu-id="332ce-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="332ce-137">Örneğin, \" 2xx, 301-304418 \" .</span><span class="sxs-lookup"><span data-stu-id="332ce-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="332ce-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="332ce-138">CommonParameters</span></span>
<span data-ttu-id="332ce-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="332ce-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="332ce-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="332ce-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="332ce-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="332ce-141">INPUTS</span></span>

### <span data-ttu-id="332ce-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="332ce-142">None</span></span>

## <span data-ttu-id="332ce-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="332ce-143">OUTPUTS</span></span>

### <span data-ttu-id="332ce-144">Microsoft. Azure. Commands. Network. model. PSConnectionMonitorTcpConfiguration</span><span class="sxs-lookup"><span data-stu-id="332ce-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="332ce-145">Microsoft. Azure. Commands. Network. model. PSConnectionMonitorHttpConfiguration</span><span class="sxs-lookup"><span data-stu-id="332ce-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="332ce-146">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorIcmpConfiguration</span><span class="sxs-lookup"><span data-stu-id="332ce-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="332ce-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="332ce-147">NOTES</span></span>

## <span data-ttu-id="332ce-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="332ce-148">RELATED LINKS</span></span>
