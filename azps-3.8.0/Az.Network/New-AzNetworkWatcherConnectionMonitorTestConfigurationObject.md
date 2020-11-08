---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: f394d5aadb743f4439f3bda4cd5522f26f719516
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097269"
---
# <span data-ttu-id="dd4dd-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dd4dd-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="dd4dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4dd-103">Bağlantı İzleyicisi test yapılandırması oluşturma.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="dd4dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd4dd-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Int32>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd4dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd4dd-105">DESCRIPTION</span></span>
<span data-ttu-id="dd4dd-106">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet 'i bir bağlantı İzleyicisi test yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="dd4dd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd4dd-107">EXAMPLES</span></span>

### <span data-ttu-id="dd4dd-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd4dd-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="dd4dd-109">Ad: httpTC TestFrequencySec: 120 Tercihredıhttp sürümü: ProtocolConfiguration: {"BağlantıNoktası": 443, "method": "GET", "RequestHeaders": [{"ad": "Izin ver", "değer": "GET"}], "ValidStatusCodeRanges": ["$ xx", "300-308"], "tercihe bağlı"</span><span class="sxs-lookup"><span data-stu-id="dd4dd-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="dd4dd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd4dd-110">PARAMETERS</span></span>

### <span data-ttu-id="dd4dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd4dd-111">-DefaultProfile</span></span>
<span data-ttu-id="dd4dd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd4dd-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd4dd-113">-Name</span></span>
<span data-ttu-id="dd4dd-114">Bağlantı İzleyicisi test yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-114">The name of the connection monitor test configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4dd-115">-Tercih No</span><span class="sxs-lookup"><span data-stu-id="dd4dd-115">-PreferredIPVersion</span></span>
<span data-ttu-id="dd4dd-116">Test değerlendirmesinde kullanılacak tercih edilen IP sürümü.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="dd4dd-117">Bağlantı İzleyicisi başka parametrelere bağlı olarak farklı bir sürüm kullanmayı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4dd-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd4dd-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="dd4dd-119">Bazı protokolden test değerlendirmesi gerçekleştirmek için kullanılan parametreler.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4dd-120">-Başarılı Thresholdchecksfailedpercent</span><span class="sxs-lookup"><span data-stu-id="dd4dd-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="dd4dd-121">Testin başarılı olarak değerlendirmesi için izin verilen maksimum başarısız denetim yüzdesi.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4dd-122">-Başarılı eşik saat MS</span><span class="sxs-lookup"><span data-stu-id="dd4dd-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="dd4dd-123">Testin başarılı olarak değerlendirmesi için izin verilen en fazla gidiş dönüş süresi.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4dd-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="dd4dd-124">-TestFrequencySec</span></span>
<span data-ttu-id="dd4dd-125">Saniye cinsinden test değerlendirmesinin sıklığı.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4dd-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd4dd-126">-Confirm</span></span>
<span data-ttu-id="dd4dd-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4dd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd4dd-128">-WhatIf</span></span>
<span data-ttu-id="dd4dd-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd4dd-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4dd-131">CommonParameters</span></span>
<span data-ttu-id="dd4dd-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4dd-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dd4dd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4dd-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd4dd-134">INPUTS</span></span>

### <span data-ttu-id="dd4dd-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dd4dd-135">None</span></span>

## <span data-ttu-id="dd4dd-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd4dd-136">OUTPUTS</span></span>

### <span data-ttu-id="dd4dd-137">Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dd4dd-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="dd4dd-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd4dd-138">NOTES</span></span>

## <span data-ttu-id="dd4dd-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd4dd-139">RELATED LINKS</span></span>
