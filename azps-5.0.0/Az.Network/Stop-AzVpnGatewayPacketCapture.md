---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: e5f753d822911abd79e339412741657dae36628f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325207"
---
# <span data-ttu-id="0c373-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c373-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="0c373-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c373-102">SYNOPSIS</span></span>
<span data-ttu-id="0c373-103">VPN ağ geçidinde paket yakalama Işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="0c373-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="0c373-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c373-104">SYNTAX</span></span>

### <span data-ttu-id="0c373-105">ByVpnGatewayName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c373-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c373-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="0c373-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c373-107">Byvpngatewayresourceıd</span><span class="sxs-lookup"><span data-stu-id="0c373-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c373-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c373-108">DESCRIPTION</span></span>
<span data-ttu-id="0c373-109">VPN ağ geçidinde paket yakalama Işlemini durdurur ve depolama kapsayıcısının verilen SasUrl 'sindeki sonucu karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="0c373-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="0c373-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c373-110">EXAMPLES</span></span>

### <span data-ttu-id="0c373-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c373-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
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

### <span data-ttu-id="0c373-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0c373-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
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

## <span data-ttu-id="0c373-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c373-113">PARAMETERS</span></span>

### <span data-ttu-id="0c373-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="0c373-114">-AsJob</span></span>
<span data-ttu-id="0c373-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0c373-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c373-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c373-116">-DefaultProfile</span></span>
<span data-ttu-id="0c373-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c373-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c373-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c373-118">-InputObject</span></span>
<span data-ttu-id="0c373-119">Paket yakalama 'nın başlatılması için kullanılacak VPN ağ geçidi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0c373-119">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="0c373-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c373-120">-Name</span></span>
<span data-ttu-id="0c373-121">Paket yakalama 'nın başlatılması için VPN ağ geçidi adı.</span><span class="sxs-lookup"><span data-stu-id="0c373-121">The Vpn Gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="0c373-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c373-122">-ResourceGroupName</span></span>
<span data-ttu-id="0c373-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0c373-123">The resource group name.</span></span>

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

### <span data-ttu-id="0c373-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0c373-124">-ResourceId</span></span>
<span data-ttu-id="0c373-125">Paket yakalama 'nın başlatılması için Vpnağ geçidinin Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0c373-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="0c373-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="0c373-126">-SasUrl</span></span>
<span data-ttu-id="0c373-127">VPN ağ geçidinde SAS URL paketi yakalama.</span><span class="sxs-lookup"><span data-stu-id="0c373-127">SAS URL packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="0c373-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c373-128">-Confirm</span></span>
<span data-ttu-id="0c373-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c373-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c373-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c373-130">-WhatIf</span></span>
<span data-ttu-id="0c373-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c373-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c373-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c373-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c373-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c373-133">CommonParameters</span></span>
<span data-ttu-id="0c373-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c373-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c373-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0c373-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c373-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c373-136">INPUTS</span></span>

### <span data-ttu-id="0c373-137">Microsoft. Azure. Commands. Network. model. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="0c373-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="0c373-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0c373-138">System.String</span></span>

## <span data-ttu-id="0c373-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c373-139">OUTPUTS</span></span>

### <span data-ttu-id="0c373-140">Microsoft. Azure. Commands. Network. modeller. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="0c373-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="0c373-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c373-141">NOTES</span></span>

## <span data-ttu-id="0c373-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c373-142">RELATED LINKS</span></span>

[<span data-ttu-id="0c373-143">Başlangıç-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0c373-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)