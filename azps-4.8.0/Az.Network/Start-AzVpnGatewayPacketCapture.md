---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265880"
---
# <span data-ttu-id="16347-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16347-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="16347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16347-102">SYNOPSIS</span></span>
<span data-ttu-id="16347-103">VPN ağ geçidinde paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="16347-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="16347-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16347-104">SYNTAX</span></span>

### <span data-ttu-id="16347-105">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16347-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16347-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="16347-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16347-107">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="16347-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16347-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="16347-108">DESCRIPTION</span></span>
<span data-ttu-id="16347-109">VPN ağ geçidinde paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="16347-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="16347-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16347-110">EXAMPLES</span></span>

### <span data-ttu-id="16347-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="16347-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
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

### <span data-ttu-id="16347-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="16347-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
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

## <span data-ttu-id="16347-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16347-113">PARAMETERS</span></span>

### <span data-ttu-id="16347-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="16347-114">-AsJob</span></span>
<span data-ttu-id="16347-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="16347-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16347-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16347-116">-DefaultProfile</span></span>
<span data-ttu-id="16347-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16347-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16347-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="16347-118">-FilterData</span></span>
<span data-ttu-id="16347-119">VPN ağ geçidinde start Packet Capture için filtreleme seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="16347-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="16347-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16347-120">-InputObject</span></span>
<span data-ttu-id="16347-121">Paket yakalama 'nın başlatılması için kullanılacak VPN ağ geçidi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="16347-121">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16347-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="16347-122">-Name</span></span>
<span data-ttu-id="16347-123">Paket yakalama 'nın başlatılması gerektiği VPN ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="16347-123">The Vpn Gateway name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16347-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16347-124">-ResourceGroupName</span></span>
<span data-ttu-id="16347-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="16347-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16347-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="16347-126">-ResourceId</span></span>
<span data-ttu-id="16347-127">Paket yakalama 'nın başlatılması için Vpnağ geçidinin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="16347-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16347-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="16347-128">-Confirm</span></span>
<span data-ttu-id="16347-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16347-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16347-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16347-130">-WhatIf</span></span>
<span data-ttu-id="16347-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16347-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16347-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16347-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16347-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16347-133">CommonParameters</span></span>
<span data-ttu-id="16347-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16347-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16347-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="16347-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16347-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16347-136">INPUTS</span></span>

### <span data-ttu-id="16347-137">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="16347-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="16347-138">System. String</span><span class="sxs-lookup"><span data-stu-id="16347-138">System.String</span></span>

## <span data-ttu-id="16347-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16347-139">OUTPUTS</span></span>

### <span data-ttu-id="16347-140">Microsoft. Azure. Commands. Network. modeller. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="16347-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="16347-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16347-141">NOTES</span></span>

## <span data-ttu-id="16347-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16347-142">RELATED LINKS</span></span>

[<span data-ttu-id="16347-143">Dur-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16347-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)