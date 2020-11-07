---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 03b4ea18bc40f8ddd3a2dc2605427013c45d7506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753948"
---
# <span data-ttu-id="27502-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="27502-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="27502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27502-102">SYNOPSIS</span></span>
<span data-ttu-id="27502-103">Bu komut, sunucu uç noktasının ayarlanabilir parametrelerinde değişiklik yapılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="27502-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="27502-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27502-104">SYNTAX</span></span>

### <span data-ttu-id="27502-105">ObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27502-105">ObjectParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27502-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="27502-106">StringParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27502-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="27502-107">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27502-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="27502-108">DESCRIPTION</span></span>
<span data-ttu-id="27502-109">Bu komut, sunucu uç noktasının ayarlanabilir parametrelerinde değişiklik yapılmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="27502-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="27502-110">Örneğin bulut katmanlama ve bulut katmanlama ilkeleri için her zaman değiştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="27502-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="27502-111">Sunucu uç noktasının yerel yol gibi birkaç yönü, sunucu uç noktası oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="27502-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="27502-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27502-112">EXAMPLES</span></span>

### <span data-ttu-id="27502-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="27502-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="27502-114">Bu örnek iki eylem gerçekleştirir, belirli bir sunucu uç noktasında, sunucunun son 30 gün içinde erişilmeyen tüm dosyaları bağlayıcıya yöneltir ve bu, oluşturulduğu sırada bu sunucu uç noktasında etkinleştirilmiş olan çevrimdışı veri aktarım modunu devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="27502-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="27502-115">Azure veri kutusu gibi toplu geçiş hizmetleriyle birlikte çalışabilirliğin bir parçası olarak çevrimdışı veri aktarımı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="27502-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="27502-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27502-116">PARAMETERS</span></span>

### <span data-ttu-id="27502-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="27502-117">-AsJob</span></span>
<span data-ttu-id="27502-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="27502-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27502-119">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="27502-119">-OfflineDataTransfer</span></span>
<span data-ttu-id="27502-120">Bulut çekirdek verileri parametresi</span><span class="sxs-lookup"><span data-stu-id="27502-120">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="27502-121">-Offlinedatatransferpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="27502-121">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="27502-122">Cloud seeded veri dosyası paylaşımı URI parametresi</span><span class="sxs-lookup"><span data-stu-id="27502-122">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="27502-123">-Cloudbir</span><span class="sxs-lookup"><span data-stu-id="27502-123">-CloudTiering</span></span>
<span data-ttu-id="27502-124">Bulut katmanlama parametresi</span><span class="sxs-lookup"><span data-stu-id="27502-124">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="27502-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27502-125">-DefaultProfile</span></span>
<span data-ttu-id="27502-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27502-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27502-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27502-127">-InputObject</span></span>
<span data-ttu-id="27502-128">Normalde parametre aracılığıyla geçirilen SyncGroup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="27502-128">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="27502-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="27502-129">-Name</span></span>
<span data-ttu-id="27502-130">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="27502-130">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="27502-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27502-131">-ResourceGroupName</span></span>
<span data-ttu-id="27502-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="27502-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="27502-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="27502-133">-ResourceId</span></span>
<span data-ttu-id="27502-134">ServerEndpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="27502-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="27502-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="27502-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="27502-136">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="27502-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="27502-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="27502-137">-SyncGroupName</span></span>
<span data-ttu-id="27502-138">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="27502-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="27502-139">-Tierfilesolderergünü</span><span class="sxs-lookup"><span data-stu-id="27502-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="27502-140">Days parametresinden eski katman dosyaları</span><span class="sxs-lookup"><span data-stu-id="27502-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="27502-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="27502-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="27502-142">Disk alanı yüzde parametresi</span><span class="sxs-lookup"><span data-stu-id="27502-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="27502-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27502-143">CommonParameters</span></span>
<span data-ttu-id="27502-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27502-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27502-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27502-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27502-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27502-146">INPUTS</span></span>

### <span data-ttu-id="27502-147">System. String</span><span class="sxs-lookup"><span data-stu-id="27502-147">System.String</span></span>

### <span data-ttu-id="27502-148">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="27502-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="27502-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27502-149">OUTPUTS</span></span>

### <span data-ttu-id="27502-150">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="27502-150">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="27502-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27502-151">NOTES</span></span>

## <span data-ttu-id="27502-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27502-152">RELATED LINKS</span></span>
