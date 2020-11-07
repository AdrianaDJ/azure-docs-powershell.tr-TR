---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: f1d5ac87cc237e5a8ec92262255e996741346613
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940056"
---
# <span data-ttu-id="969f6-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="969f6-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="969f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="969f6-102">SYNOPSIS</span></span>
<span data-ttu-id="969f6-103">Bir yük dengeleyici için yoklama yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="969f6-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="969f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="969f6-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="969f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="969f6-105">DESCRIPTION</span></span>
<span data-ttu-id="969f6-106">**Yeni-AzureRmLoadBalancerProbeConfig** cmdlet 'i, bir Azure yük dengeleyicisi için bir yoklama yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="969f6-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="969f6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="969f6-107">EXAMPLES</span></span>

### <span data-ttu-id="969f6-108">Örnek 1: yoklama yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="969f6-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="969f6-109">Bu komut, HTTP protokolünü kullanarak Myaraştırması adlı bir yoklama yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="969f6-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="969f6-110">Yeni yoklama, bağlantı noktası 80 ' da yük dengeli bir hizmete bağlanır.</span><span class="sxs-lookup"><span data-stu-id="969f6-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="969f6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="969f6-111">PARAMETERS</span></span>

### <span data-ttu-id="969f6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969f6-112">-DefaultProfile</span></span>
<span data-ttu-id="969f6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="969f6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969f6-114">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="969f6-114">-IntervalInSeconds</span></span>
<span data-ttu-id="969f6-115">Yük dengeli bir hizmetin her örneğindeki yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="969f6-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969f6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="969f6-116">-Name</span></span>
<span data-ttu-id="969f6-117">Oluşturulacak yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="969f6-117">Specifies the name of the probe configuration to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969f6-118">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="969f6-118">-Port</span></span>
<span data-ttu-id="969f6-119">Yeni araştırın yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="969f6-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969f6-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="969f6-120">-ProbeCount</span></span>
<span data-ttu-id="969f6-121">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="969f6-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969f6-122">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="969f6-122">-Protocol</span></span>
<span data-ttu-id="969f6-123">Araştırma yapılandırması için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="969f6-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="969f6-124">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="969f6-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969f6-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="969f6-125">-RequestPath</span></span>
<span data-ttu-id="969f6-126">Sistem durumunu belirlemek için yük dengeli bir hizmetin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="969f6-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="969f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969f6-127">CommonParameters</span></span>
<span data-ttu-id="969f6-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="969f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969f6-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="969f6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969f6-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="969f6-130">INPUTS</span></span>

## <span data-ttu-id="969f6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="969f6-131">OUTPUTS</span></span>

### <span data-ttu-id="969f6-132">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="969f6-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="969f6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="969f6-133">NOTES</span></span>

## <span data-ttu-id="969f6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="969f6-134">RELATED LINKS</span></span>

[<span data-ttu-id="969f6-135">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="969f6-135">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="969f6-136">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="969f6-136">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="969f6-137">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="969f6-137">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="969f6-138">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="969f6-138">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


