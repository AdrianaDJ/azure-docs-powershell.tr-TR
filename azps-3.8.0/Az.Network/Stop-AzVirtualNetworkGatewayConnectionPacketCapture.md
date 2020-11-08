---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 1303f8c8d2bb7b1de4401072ce1e968373aed28b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096126"
---
# <span data-ttu-id="f20a8-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f20a8-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="f20a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f20a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f20a8-103">Sanal ağ geçidi bağlantısında paket yakalama Işlemini durdurur</span><span class="sxs-lookup"><span data-stu-id="f20a8-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="f20a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f20a8-104">SYNTAX</span></span>

### <span data-ttu-id="f20a8-105">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f20a8-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20a8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f20a8-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20a8-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f20a8-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f20a8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f20a8-108">DESCRIPTION</span></span>
<span data-ttu-id="f20a8-109">Sanal ağ geçidi bağlantısında paket yakalama Işlemini durdurur ve depolama kapsayıcısının verilen SasUrl 'sindeki sonucu karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="f20a8-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="f20a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f20a8-110">EXAMPLES</span></span>

### <span data-ttu-id="f20a8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f20a8-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="f20a8-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f20a8-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="f20a8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f20a8-113">PARAMETERS</span></span>

### <span data-ttu-id="f20a8-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="f20a8-114">-AsJob</span></span>
<span data-ttu-id="f20a8-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f20a8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f20a8-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="f20a8-116">-Confirm</span></span>
<span data-ttu-id="f20a8-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f20a8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f20a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20a8-118">-DefaultProfile</span></span>
<span data-ttu-id="f20a8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f20a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f20a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f20a8-120">-InputObject</span></span>
<span data-ttu-id="f20a8-121">Paket yakalama 'nın başlatılması için kullanılacak sanal ağ geçidi bağlantı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f20a8-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="f20a8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f20a8-122">-Name</span></span>
<span data-ttu-id="f20a8-123">Paket yakalama 'nın başlatılması gerektiği sanal ağ geçidi bağlantı adı.</span><span class="sxs-lookup"><span data-stu-id="f20a8-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f20a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f20a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="f20a8-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f20a8-125">The resource group name.</span></span>

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

### <span data-ttu-id="f20a8-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f20a8-126">-ResourceId</span></span>
<span data-ttu-id="f20a8-127">Paket yakalama 'nın başlatılması için VirtualNetworkGatewayConnection 'un Azure Resource ID 'si.</span><span class="sxs-lookup"><span data-stu-id="f20a8-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="f20a8-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="f20a8-128">-SasUrl</span></span>
<span data-ttu-id="f20a8-129">Sanal ağ geçidinde paket yakalamayı durdurma için SAS URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="f20a8-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="f20a8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f20a8-130">-WhatIf</span></span>
<span data-ttu-id="f20a8-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f20a8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f20a8-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f20a8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f20a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20a8-133">CommonParameters</span></span>
<span data-ttu-id="f20a8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f20a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20a8-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f20a8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20a8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f20a8-136">INPUTS</span></span>

### <span data-ttu-id="f20a8-137">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f20a8-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="f20a8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f20a8-138">System.String</span></span>

## <span data-ttu-id="f20a8-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f20a8-139">OUTPUTS</span></span>

### <span data-ttu-id="f20a8-140">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="f20a8-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="f20a8-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f20a8-141">NOTES</span></span>

## <span data-ttu-id="f20a8-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f20a8-142">RELATED LINKS</span></span>
[<span data-ttu-id="f20a8-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f20a8-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)