---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 88cbb5417e8a82ede25cc77274294a5dc4f64b9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265867"
---
# <span data-ttu-id="d125d-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d125d-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="d125d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d125d-102">SYNOPSIS</span></span>
<span data-ttu-id="d125d-103">VPN bağlantısındaki paket yakalama Işlemini durdurur</span><span class="sxs-lookup"><span data-stu-id="d125d-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="d125d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d125d-104">SYNTAX</span></span>

### <span data-ttu-id="d125d-105">ByVpnConnectionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d125d-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-LinkConnectionName <String>] -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d125d-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="d125d-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-LinkConnectionName <String>]
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d125d-107">Byvpnconnectionresourceıd</span><span class="sxs-lookup"><span data-stu-id="d125d-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> [-LinkConnectionName <String>] -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d125d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d125d-108">DESCRIPTION</span></span>
<span data-ttu-id="d125d-109">VPN bağlantısındaki paket yakalama Işlemini durdurur ve depolama kapsayıcısının verilen SasUrl 'sindeki sonucu karşıya yükler.</span><span class="sxs-lookup"><span data-stu-id="d125d-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="d125d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d125d-110">EXAMPLES</span></span>

### <span data-ttu-id="d125d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d125d-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="d125d-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d125d-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="d125d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d125d-113">PARAMETERS</span></span>

### <span data-ttu-id="d125d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d125d-114">-AsJob</span></span>
<span data-ttu-id="d125d-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d125d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d125d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d125d-116">-DefaultProfile</span></span>
<span data-ttu-id="d125d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d125d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d125d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d125d-118">-InputObject</span></span>
<span data-ttu-id="d125d-119">Paket yakalama 'nın başlatılması için kullanılacak VPN bağlantısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d125d-119">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="d125d-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="d125d-120">-LinkConnectionName</span></span>
<span data-ttu-id="d125d-121">SiteLinkConnection 'un adları.</span><span class="sxs-lookup"><span data-stu-id="d125d-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="d125d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d125d-122">-Name</span></span>
<span data-ttu-id="d125d-123">Paket yakalama 'nın başlatılması gerektiği VPN bağlantısı adı.</span><span class="sxs-lookup"><span data-stu-id="d125d-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d125d-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d125d-124">-ParentResourceName</span></span>
<span data-ttu-id="d125d-125">Üst kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="d125d-125">The parent resource name.</span></span>

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

### <span data-ttu-id="d125d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d125d-126">-ResourceGroupName</span></span>
<span data-ttu-id="d125d-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d125d-127">The resource group name.</span></span>

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

### <span data-ttu-id="d125d-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d125d-128">-ResourceId</span></span>
<span data-ttu-id="d125d-129">Paket yakalama 'nın başlatılması için VpnConnection 'un Azure Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d125d-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="d125d-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="d125d-130">-SasUrl</span></span>
<span data-ttu-id="d125d-131">VPN 'de paket yakalamayı durdurma için SAS URL 'Si.</span><span class="sxs-lookup"><span data-stu-id="d125d-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="d125d-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="d125d-132">-Confirm</span></span>
<span data-ttu-id="d125d-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d125d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d125d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d125d-134">-WhatIf</span></span>
<span data-ttu-id="d125d-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d125d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d125d-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d125d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d125d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d125d-137">CommonParameters</span></span>
<span data-ttu-id="d125d-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d125d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d125d-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d125d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d125d-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d125d-140">INPUTS</span></span>

### <span data-ttu-id="d125d-141">Microsoft. Azure. Commands. Network. model. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="d125d-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="d125d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d125d-142">System.String</span></span>

## <span data-ttu-id="d125d-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d125d-143">OUTPUTS</span></span>

### <span data-ttu-id="d125d-144">Microsoft. Azure. Commands. Network. modeller. PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d125d-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="d125d-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d125d-145">NOTES</span></span>

## <span data-ttu-id="d125d-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d125d-146">RELATED LINKS</span></span>

[<span data-ttu-id="d125d-147">Başlangıç-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d125d-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)