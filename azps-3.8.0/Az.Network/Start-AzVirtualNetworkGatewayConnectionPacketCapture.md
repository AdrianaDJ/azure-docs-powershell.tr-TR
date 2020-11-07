---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937420"
---
# <span data-ttu-id="67963-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67963-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="67963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67963-102">SYNOPSIS</span></span>
<span data-ttu-id="67963-103">Sanal ağ geçidi bağlantısında paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="67963-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="67963-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67963-104">SYNTAX</span></span>

### <span data-ttu-id="67963-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="67963-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67963-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67963-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67963-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="67963-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67963-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="67963-108">DESCRIPTION</span></span>
<span data-ttu-id="67963-109">Sanal ağ geçidi bağlantısında paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="67963-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="67963-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67963-110">EXAMPLES</span></span>

### <span data-ttu-id="67963-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="67963-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="67963-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="67963-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="67963-113">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="67963-113">Example 3</span></span>
<span data-ttu-id="67963-114">Tüm iç ve dış paketlerin yakalanması için paket yakalama örneği</span><span class="sxs-lookup"><span data-stu-id="67963-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="67963-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67963-115">PARAMETERS</span></span>

### <span data-ttu-id="67963-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="67963-116">-AsJob</span></span>
<span data-ttu-id="67963-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="67963-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="67963-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="67963-118">-Confirm</span></span>
<span data-ttu-id="67963-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67963-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67963-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67963-120">-DefaultProfile</span></span>
<span data-ttu-id="67963-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67963-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67963-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="67963-122">-FilterData</span></span>
<span data-ttu-id="67963-123">Sanal ağ geçidi bağlantısında başlangıç paketi yakalama için filtre seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="67963-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="67963-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67963-124">-InputObject</span></span>
<span data-ttu-id="67963-125">Paket yakalama 'nın başlatılması için kullanılacak sanal ağ geçidi bağlantı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="67963-125">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67963-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="67963-126">-Name</span></span>
<span data-ttu-id="67963-127">Paketin yakalanması için sanal ağ geçidi bağlantı adı.</span><span class="sxs-lookup"><span data-stu-id="67963-127">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67963-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67963-128">-ResourceGroupName</span></span>
<span data-ttu-id="67963-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="67963-129">The resource group name.</span></span>

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

### <span data-ttu-id="67963-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="67963-130">-ResourceId</span></span>
<span data-ttu-id="67963-131">Paket yakalama 'nın başlatılması için VirtualNetworkGatewayConnection 'un Azure Resource ID 'si.</span><span class="sxs-lookup"><span data-stu-id="67963-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="67963-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67963-132">-WhatIf</span></span>
<span data-ttu-id="67963-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67963-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67963-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67963-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67963-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67963-135">CommonParameters</span></span>
<span data-ttu-id="67963-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67963-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67963-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="67963-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67963-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67963-138">INPUTS</span></span>

### <span data-ttu-id="67963-139">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="67963-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="67963-140">System. String</span><span class="sxs-lookup"><span data-stu-id="67963-140">System.String</span></span>

## <span data-ttu-id="67963-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67963-141">OUTPUTS</span></span>

### <span data-ttu-id="67963-142">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="67963-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="67963-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67963-143">NOTES</span></span>

## <span data-ttu-id="67963-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67963-144">RELATED LINKS</span></span>
[<span data-ttu-id="67963-145">Dur-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="67963-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)