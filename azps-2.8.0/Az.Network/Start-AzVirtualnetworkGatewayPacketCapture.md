---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 1f0b539e2f5a6e2c387738558fb6db8cbe647457
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932710"
---
# <span data-ttu-id="556c7-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="556c7-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="556c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="556c7-102">SYNOPSIS</span></span>
<span data-ttu-id="556c7-103">Sanal ağ geçidinde paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="556c7-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="556c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="556c7-104">SYNTAX</span></span>

### <span data-ttu-id="556c7-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="556c7-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="556c7-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="556c7-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="556c7-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="556c7-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="556c7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="556c7-108">DESCRIPTION</span></span>
<span data-ttu-id="556c7-109">Sanal ağ geçidinde paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="556c7-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="556c7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="556c7-110">EXAMPLES</span></span>

### <span data-ttu-id="556c7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="556c7-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="556c7-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="556c7-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="556c7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="556c7-113">PARAMETERS</span></span>

### <span data-ttu-id="556c7-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="556c7-114">-AsJob</span></span>
<span data-ttu-id="556c7-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="556c7-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556c7-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="556c7-116">-Confirm</span></span>
<span data-ttu-id="556c7-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="556c7-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556c7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="556c7-118">-DefaultProfile</span></span>
<span data-ttu-id="556c7-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="556c7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556c7-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="556c7-120">-FilterData</span></span>
<span data-ttu-id="556c7-121">Sanal ağ geçidinde Başlat paketi yakalaması için filtreleme seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="556c7-121">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="556c7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="556c7-122">-InputObject</span></span>
<span data-ttu-id="556c7-123">Paket yakalama 'nın başlatılması için kullanılacak sanal ağ geçidi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="556c7-123">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="556c7-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="556c7-124">-Name</span></span>
<span data-ttu-id="556c7-125">Paket yakalama 'nın başlatılması gerektiği sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="556c7-125">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556c7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="556c7-126">-ResourceGroupName</span></span>
<span data-ttu-id="556c7-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="556c7-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556c7-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="556c7-128">-ResourceId</span></span>
<span data-ttu-id="556c7-129">Paket yakalamanın başlatılması için VirtualNetworkGateway 'in Azure Resource ID 'si.</span><span class="sxs-lookup"><span data-stu-id="556c7-129">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="556c7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="556c7-130">-WhatIf</span></span>
<span data-ttu-id="556c7-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="556c7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="556c7-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="556c7-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556c7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="556c7-133">CommonParameters</span></span>
<span data-ttu-id="556c7-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="556c7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="556c7-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="556c7-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="556c7-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="556c7-136">INPUTS</span></span>

### <span data-ttu-id="556c7-137">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="556c7-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="556c7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="556c7-138">System.String</span></span>

## <span data-ttu-id="556c7-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="556c7-139">OUTPUTS</span></span>

### <span data-ttu-id="556c7-140">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="556c7-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="556c7-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="556c7-141">NOTES</span></span>

## <span data-ttu-id="556c7-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="556c7-142">RELATED LINKS</span></span>
[<span data-ttu-id="556c7-143">Dur-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="556c7-143">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)