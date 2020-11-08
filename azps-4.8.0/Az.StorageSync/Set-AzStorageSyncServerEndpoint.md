---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110154"
---
# <span data-ttu-id="2ca81-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ca81-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="2ca81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ca81-102">SYNOPSIS</span></span>
<span data-ttu-id="2ca81-103">Bu komut, sunucu uç noktasının ayarlanabilir parametrelerinde değişiklik yapılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2ca81-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="2ca81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ca81-104">SYNTAX</span></span>

### <span data-ttu-id="2ca81-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ca81-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca81-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2ca81-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ca81-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ca81-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ca81-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ca81-108">DESCRIPTION</span></span>
<span data-ttu-id="2ca81-109">Bu komut, sunucu uç noktasının ayarlanabilir parametrelerinde değişiklik yapılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2ca81-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="2ca81-110">Örneğin bulut katmanlama ve bulut katmanlama ilkeleri için her zaman değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="2ca81-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="2ca81-111">Sunucu uç noktasının yerel yol gibi birkaç yönü, sunucu uç noktası oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="2ca81-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="2ca81-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ca81-112">EXAMPLES</span></span>

### <span data-ttu-id="2ca81-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ca81-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="2ca81-114">Bu örnek iki eylem gerçekleştirir, belirli bir sunucu uç noktasında, sunucunun son 30 gün içinde erişilmeyen tüm dosyaları bağlayıcıya yöneltir ve bu, oluşturulduğu sırada bu sunucu uç noktasında etkinleştirilmiş olan çevrimdışı veri aktarım modunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="2ca81-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="2ca81-115">Azure veri kutusu gibi toplu geçiş hizmetleriyle birlikte çalışabilirliğin bir parçası olarak çevrimdışı veri aktarımı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2ca81-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="2ca81-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ca81-116">PARAMETERS</span></span>

### <span data-ttu-id="2ca81-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="2ca81-117">-AsJob</span></span>
<span data-ttu-id="2ca81-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2ca81-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ca81-119">-Cloudbir</span><span class="sxs-lookup"><span data-stu-id="2ca81-119">-CloudTiering</span></span>
<span data-ttu-id="2ca81-120">Bulut katmanlama parametresi</span><span class="sxs-lookup"><span data-stu-id="2ca81-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="2ca81-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ca81-121">-DefaultProfile</span></span>
<span data-ttu-id="2ca81-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ca81-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ca81-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ca81-123">-InputObject</span></span>
<span data-ttu-id="2ca81-124">Normalde parametre aracılığıyla geçirilen SyncGroup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2ca81-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca81-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ca81-125">-Name</span></span>
<span data-ttu-id="2ca81-126">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="2ca81-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca81-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="2ca81-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="2ca81-128">Bulut çekirdek verileri parametresi</span><span class="sxs-lookup"><span data-stu-id="2ca81-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="2ca81-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="2ca81-129">-localCacheMode</span></span>
<span data-ttu-id="2ca81-130">Yerel önbellek modu parametresi</span><span class="sxs-lookup"><span data-stu-id="2ca81-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="2ca81-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca81-131">-ResourceGroupName</span></span>
<span data-ttu-id="2ca81-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2ca81-132">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca81-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2ca81-133">-ResourceId</span></span>
<span data-ttu-id="2ca81-134">ServerEndpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="2ca81-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ca81-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="2ca81-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="2ca81-136">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="2ca81-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca81-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="2ca81-137">-SyncGroupName</span></span>
<span data-ttu-id="2ca81-138">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="2ca81-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca81-139">-Tierfilesolderergünü</span><span class="sxs-lookup"><span data-stu-id="2ca81-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="2ca81-140">Days parametresinden eski katman dosyaları</span><span class="sxs-lookup"><span data-stu-id="2ca81-140">Tier Files Older Than Days Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca81-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="2ca81-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="2ca81-142">Disk alanı yüzde parametresi</span><span class="sxs-lookup"><span data-stu-id="2ca81-142">Volume Free Space Percent Parameter</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ca81-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ca81-143">-Confirm</span></span>
<span data-ttu-id="2ca81-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ca81-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ca81-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ca81-145">-WhatIf</span></span>
<span data-ttu-id="2ca81-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ca81-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ca81-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ca81-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ca81-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ca81-148">CommonParameters</span></span>
<span data-ttu-id="2ca81-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ca81-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ca81-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ca81-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ca81-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ca81-151">INPUTS</span></span>

### <span data-ttu-id="2ca81-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2ca81-152">System.String</span></span>

### <span data-ttu-id="2ca81-153">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ca81-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="2ca81-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ca81-154">OUTPUTS</span></span>

### <span data-ttu-id="2ca81-155">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ca81-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="2ca81-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ca81-156">NOTES</span></span>

## <span data-ttu-id="2ca81-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ca81-157">RELATED LINKS</span></span>
