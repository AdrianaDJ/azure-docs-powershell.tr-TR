---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325699"
---
# <span data-ttu-id="2c18f-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c18f-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="2c18f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c18f-102">SYNOPSIS</span></span>
<span data-ttu-id="2c18f-103">Sanal ağ geçidinde paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="2c18f-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="2c18f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c18f-104">SYNTAX</span></span>

### <span data-ttu-id="2c18f-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2c18f-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c18f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2c18f-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c18f-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2c18f-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c18f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c18f-108">DESCRIPTION</span></span>
<span data-ttu-id="2c18f-109">Sanal ağ geçidinde paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="2c18f-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="2c18f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c18f-110">EXAMPLES</span></span>

### <span data-ttu-id="2c18f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2c18f-111">Example 1</span></span>
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
### <span data-ttu-id="2c18f-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2c18f-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
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
### <span data-ttu-id="2c18f-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2c18f-113">Example 3</span></span>
<span data-ttu-id="2c18f-114">Tüm iç ve dış paketlerin yakalanması için paket yakalama örneği</span><span class="sxs-lookup"><span data-stu-id="2c18f-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
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

## <span data-ttu-id="2c18f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c18f-115">PARAMETERS</span></span>

### <span data-ttu-id="2c18f-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="2c18f-116">-AsJob</span></span>
<span data-ttu-id="2c18f-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2c18f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c18f-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="2c18f-118">-Confirm</span></span>
<span data-ttu-id="2c18f-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2c18f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c18f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c18f-120">-DefaultProfile</span></span>
<span data-ttu-id="2c18f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2c18f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c18f-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="2c18f-122">-FilterData</span></span>
<span data-ttu-id="2c18f-123">Sanal ağ geçidinde Başlat paketi yakalaması için filtreleme seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="2c18f-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="2c18f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c18f-124">-InputObject</span></span>
<span data-ttu-id="2c18f-125">Paket yakalama 'nın başlatılması için kullanılacak sanal ağ geçidi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2c18f-125">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="2c18f-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2c18f-126">-Name</span></span>
<span data-ttu-id="2c18f-127">Paket yakalama 'nın başlatılması gerektiği sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="2c18f-127">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="2c18f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c18f-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c18f-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2c18f-129">The resource group name.</span></span>

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

### <span data-ttu-id="2c18f-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2c18f-130">-ResourceId</span></span>
<span data-ttu-id="2c18f-131">Paket yakalamanın başlatılması için VirtualNetworkGateway 'in Azure Resource ID 'si.</span><span class="sxs-lookup"><span data-stu-id="2c18f-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="2c18f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c18f-132">-WhatIf</span></span>
<span data-ttu-id="2c18f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2c18f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c18f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2c18f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c18f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c18f-135">CommonParameters</span></span>
<span data-ttu-id="2c18f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c18f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c18f-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2c18f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c18f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c18f-138">INPUTS</span></span>

### <span data-ttu-id="2c18f-139">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c18f-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="2c18f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2c18f-140">System.String</span></span>

## <span data-ttu-id="2c18f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c18f-141">OUTPUTS</span></span>

### <span data-ttu-id="2c18f-142">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="2c18f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="2c18f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c18f-143">NOTES</span></span>

## <span data-ttu-id="2c18f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c18f-144">RELATED LINKS</span></span>
[<span data-ttu-id="2c18f-145">Dur-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2c18f-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)