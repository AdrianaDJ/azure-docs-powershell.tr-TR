---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 8efb8c331ffb7dd7be664c1d127d8cbe980b1570
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265881"
---
# <span data-ttu-id="46cb6-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46cb6-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="46cb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="46cb6-103">VPN bağlantısında paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="46cb6-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="46cb6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46cb6-104">SYNTAX</span></span>

### <span data-ttu-id="46cb6-105">ByVpnConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="46cb6-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] [-LinkConnectionName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46cb6-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="46cb6-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 [-LinkConnectionName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46cb6-107">Byvpnconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="46cb6-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-LinkConnectionName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46cb6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="46cb6-108">DESCRIPTION</span></span>
<span data-ttu-id="46cb6-109">VPN bağlantısında paket yakalama Işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="46cb6-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="46cb6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46cb6-110">EXAMPLES</span></span>

### <span data-ttu-id="46cb6-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="46cb6-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
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

### <span data-ttu-id="46cb6-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="46cb6-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
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

## <span data-ttu-id="46cb6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46cb6-113">PARAMETERS</span></span>

### <span data-ttu-id="46cb6-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="46cb6-114">-AsJob</span></span>
<span data-ttu-id="46cb6-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="46cb6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46cb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46cb6-116">-DefaultProfile</span></span>
<span data-ttu-id="46cb6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46cb6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46cb6-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="46cb6-118">-FilterData</span></span>
<span data-ttu-id="46cb6-119">VPN bağlantısında başlangıç paketi yakalamayı filtreleme seçenekleri.</span><span class="sxs-lookup"><span data-stu-id="46cb6-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="46cb6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46cb6-120">-InputObject</span></span>
<span data-ttu-id="46cb6-121">Paket yakalama 'nın başlatılması için kullanılacak VPN bağlantısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="46cb6-121">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46cb6-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="46cb6-122">-LinkConnectionName</span></span>
<span data-ttu-id="46cb6-123">SiteLinkConnection 'un adları.</span><span class="sxs-lookup"><span data-stu-id="46cb6-123">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="46cb6-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="46cb6-124">-Name</span></span>
<span data-ttu-id="46cb6-125">Paketin yakalanması için kullanılacak VPN bağlantısı adı.</span><span class="sxs-lookup"><span data-stu-id="46cb6-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46cb6-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="46cb6-126">-ParentResourceName</span></span>
<span data-ttu-id="46cb6-127">Üst Vpngateway 'in adı.</span><span class="sxs-lookup"><span data-stu-id="46cb6-127">The name of the Parent Vpngateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46cb6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46cb6-128">-ResourceGroupName</span></span>
<span data-ttu-id="46cb6-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="46cb6-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46cb6-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="46cb6-130">-ResourceId</span></span>
<span data-ttu-id="46cb6-131">Paket yakalama 'nın başlatılması için VpnConnection 'un Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="46cb6-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46cb6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="46cb6-132">-Confirm</span></span>
<span data-ttu-id="46cb6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46cb6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46cb6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46cb6-134">-WhatIf</span></span>
<span data-ttu-id="46cb6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46cb6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46cb6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46cb6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46cb6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46cb6-137">CommonParameters</span></span>
<span data-ttu-id="46cb6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46cb6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46cb6-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46cb6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46cb6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46cb6-140">INPUTS</span></span>

### <span data-ttu-id="46cb6-141">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="46cb6-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="46cb6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="46cb6-142">System.String</span></span>

## <span data-ttu-id="46cb6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46cb6-143">OUTPUTS</span></span>

### <span data-ttu-id="46cb6-144">Microsoft. Azure. Commands. Network. modeller. PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="46cb6-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="46cb6-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46cb6-145">NOTES</span></span>

## <span data-ttu-id="46cb6-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46cb6-146">RELATED LINKS</span></span>

[<span data-ttu-id="46cb6-147">Dur-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="46cb6-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)