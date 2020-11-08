---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b8adfd7c069c4215ec8f26d259ed9d1bc39be2d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279318"
---
# <span data-ttu-id="7eb3f-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7eb3f-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="7eb3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb3f-103">Bu komut, sunucu uç noktasının ayarlanabilir parametrelerinde değişiklik yapılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="7eb3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7eb3f-104">SYNTAX</span></span>

### <span data-ttu-id="7eb3f-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7eb3f-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb3f-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7eb3f-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eb3f-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7eb3f-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb3f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7eb3f-108">DESCRIPTION</span></span>
<span data-ttu-id="7eb3f-109">Bu komut, sunucu uç noktasının ayarlanabilir parametrelerinde değişiklik yapılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="7eb3f-110">Örneğin bulut katmanlama ve bulut katmanlama ilkeleri için her zaman değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="7eb3f-111">Sunucu uç noktasının yerel yol gibi birkaç yönü, sunucu uç noktası oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="7eb3f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7eb3f-112">EXAMPLES</span></span>

### <span data-ttu-id="7eb3f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7eb3f-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="7eb3f-114">Bu örnek iki eylem gerçekleştirir, belirli bir sunucu uç noktasında, sunucunun son 30 gün içinde erişilmeyen tüm dosyaları bağlayıcıya yöneltir ve bu, oluşturulduğu sırada bu sunucu uç noktasında etkinleştirilmiş olan çevrimdışı veri aktarım modunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="7eb3f-115">Azure veri kutusu gibi toplu geçiş hizmetleriyle birlikte çalışabilirliğin bir parçası olarak çevrimdışı veri aktarımı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="7eb3f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7eb3f-116">PARAMETERS</span></span>

### <span data-ttu-id="7eb3f-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="7eb3f-117">-AsJob</span></span>
<span data-ttu-id="7eb3f-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7eb3f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7eb3f-119">-Cloudbir</span><span class="sxs-lookup"><span data-stu-id="7eb3f-119">-CloudTiering</span></span>
<span data-ttu-id="7eb3f-120">Bulut katmanlama parametresi</span><span class="sxs-lookup"><span data-stu-id="7eb3f-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="7eb3f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb3f-121">-DefaultProfile</span></span>
<span data-ttu-id="7eb3f-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7eb3f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7eb3f-123">-InputObject</span></span>
<span data-ttu-id="7eb3f-124">Normalde parametre aracılığıyla geçirilen SyncGroup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="7eb3f-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="7eb3f-125">-Name</span></span>
<span data-ttu-id="7eb3f-126">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="7eb3f-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="7eb3f-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="7eb3f-128">Bulut çekirdek verileri parametresi</span><span class="sxs-lookup"><span data-stu-id="7eb3f-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="7eb3f-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="7eb3f-129">-localCacheMode</span></span>
<span data-ttu-id="7eb3f-130">Yerel önbellek modu parametresi</span><span class="sxs-lookup"><span data-stu-id="7eb3f-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="7eb3f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb3f-131">-ResourceGroupName</span></span>
<span data-ttu-id="7eb3f-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="7eb3f-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7eb3f-133">-ResourceId</span></span>
<span data-ttu-id="7eb3f-134">ServerEndpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7eb3f-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="7eb3f-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="7eb3f-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="7eb3f-136">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="7eb3f-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb3f-137">-SyncGroupName</span></span>
<span data-ttu-id="7eb3f-138">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="7eb3f-139">-Tierfilesolderergünü</span><span class="sxs-lookup"><span data-stu-id="7eb3f-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="7eb3f-140">Days parametresinden eski katman dosyaları</span><span class="sxs-lookup"><span data-stu-id="7eb3f-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="7eb3f-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="7eb3f-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="7eb3f-142">Disk alanı yüzde parametresi</span><span class="sxs-lookup"><span data-stu-id="7eb3f-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="7eb3f-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="7eb3f-143">-Confirm</span></span>
<span data-ttu-id="7eb3f-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb3f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb3f-145">-WhatIf</span></span>
<span data-ttu-id="7eb3f-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7eb3f-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb3f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb3f-148">CommonParameters</span></span>
<span data-ttu-id="7eb3f-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7eb3f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb3f-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb3f-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb3f-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7eb3f-151">INPUTS</span></span>

### <span data-ttu-id="7eb3f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="7eb3f-152">System.String</span></span>

### <span data-ttu-id="7eb3f-153">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7eb3f-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="7eb3f-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7eb3f-154">OUTPUTS</span></span>

### <span data-ttu-id="7eb3f-155">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7eb3f-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="7eb3f-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7eb3f-156">NOTES</span></span>

## <span data-ttu-id="7eb3f-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7eb3f-157">RELATED LINKS</span></span>
