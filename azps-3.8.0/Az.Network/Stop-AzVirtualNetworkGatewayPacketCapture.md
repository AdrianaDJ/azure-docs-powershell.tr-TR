---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 46d097d2985b39e1d757e2d530e67775c1b8a28d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096125"
---
# <span data-ttu-id="a16a8-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a16a8-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="a16a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a16a8-102">SYNOPSIS</span></span>
<span data-ttu-id="a16a8-103">Sanal ağ geçidinde paket yakalama Işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="a16a8-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="a16a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a16a8-104">SYNTAX</span></span>

### <span data-ttu-id="a16a8-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a16a8-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16a8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a16a8-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16a8-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="a16a8-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a16a8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a16a8-108">DESCRIPTION</span></span>
<span data-ttu-id="a16a8-109">Sanal ağ geçidinde paket yakalama Işlemini durdurur ve depolama kapsayıcısının verilen SasUrl 'sindeki sonucu karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="a16a8-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="a16a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a16a8-110">EXAMPLES</span></span>

### <span data-ttu-id="a16a8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a16a8-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="a16a8-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a16a8-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="a16a8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a16a8-113">PARAMETERS</span></span>

### <span data-ttu-id="a16a8-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="a16a8-114">-AsJob</span></span>
<span data-ttu-id="a16a8-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a16a8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a16a8-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="a16a8-116">-Confirm</span></span>
<span data-ttu-id="a16a8-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a16a8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a16a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16a8-118">-DefaultProfile</span></span>
<span data-ttu-id="a16a8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a16a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a16a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a16a8-120">-InputObject</span></span>
<span data-ttu-id="a16a8-121">Paket yakalama 'nın başlatılması için kullanılacak sanal ağ geçidi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a16a8-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="a16a8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a16a8-122">-Name</span></span>
<span data-ttu-id="a16a8-123">Paketin yakalanması için sanal ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="a16a8-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="a16a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a16a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="a16a8-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a16a8-125">The resource group name.</span></span>

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

### <span data-ttu-id="a16a8-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a16a8-126">-ResourceId</span></span>
<span data-ttu-id="a16a8-127">Paket yakalamanın başlatılması için VirtualNetworkGateway 'in Azure Resource ID 'si.</span><span class="sxs-lookup"><span data-stu-id="a16a8-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="a16a8-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="a16a8-128">-SasUrl</span></span>
<span data-ttu-id="a16a8-129">Sanal ağ geçidinde SAS URL paketi yakalama.</span><span class="sxs-lookup"><span data-stu-id="a16a8-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="a16a8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a16a8-130">-WhatIf</span></span>
<span data-ttu-id="a16a8-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a16a8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a16a8-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a16a8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a16a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16a8-133">CommonParameters</span></span>
<span data-ttu-id="a16a8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a16a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16a8-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a16a8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16a8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a16a8-136">INPUTS</span></span>

### <span data-ttu-id="a16a8-137">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="a16a8-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="a16a8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a16a8-138">System.String</span></span>

## <span data-ttu-id="a16a8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a16a8-139">OUTPUTS</span></span>

### <span data-ttu-id="a16a8-140">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a16a8-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="a16a8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a16a8-141">NOTES</span></span>

## <span data-ttu-id="a16a8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a16a8-142">RELATED LINKS</span></span>
[<span data-ttu-id="a16a8-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a16a8-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
