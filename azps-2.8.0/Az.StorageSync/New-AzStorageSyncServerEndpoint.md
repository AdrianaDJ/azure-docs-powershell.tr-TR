---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 524e9334b3e706dc51a2dfd4efc5d6f3cce710c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934312"
---
# <span data-ttu-id="0afc2-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0afc2-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="0afc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0afc2-102">SYNOPSIS</span></span>
<span data-ttu-id="0afc2-103">Bu komut, kaydedilmiş bir sunucuda yeni bir sunucu uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0afc2-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="0afc2-104">Bu, sunucudaki belirtilen yolun eşitleme grubundaki diğer uç noktalarla birlikte dosyaları eşitlemeye başlamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="0afc2-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="0afc2-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0afc2-105">SYNTAX</span></span>

### <span data-ttu-id="0afc2-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0afc2-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afc2-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0afc2-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0afc2-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0afc2-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0afc2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0afc2-109">DESCRIPTION</span></span>
<span data-ttu-id="0afc2-110">Bu komut, kaydedilmiş bir sunucuda yeni bir sunucu uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0afc2-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="0afc2-111">Bu, sunucudaki belirtilen yolun eşitleme grubundaki diğer uç noktalarla birlikte dosyaları eşitlemeye başlamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="0afc2-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="0afc2-112">Eşitleme grubundaki diğer uç noktalarda dosyalar varsa ve bu yeni eklenen konum da dosya içeriyorsa, bir mutabakat süreci, dosyaların aslında diğer uç noktalardan aynı klasörlerde olduğunu belirlemeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="0afc2-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="0afc2-113">Ad alanları, çakışma dosyalarını birleştirip Uzlaşmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="0afc2-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="0afc2-114">Diğer sunucu uç noktalarında dosyalar varsa, bu sunucudaki dosyaların boş bir konumla başlaması genellikle daha iyi olur, böylece bulut dosyaları, hızlı çökme kurtarması adlı otomatik bir işlemde sunucuya geliyor.</span><span class="sxs-lookup"><span data-stu-id="0afc2-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="0afc2-115">Ad alanı meta verileri ilk olarak eşitlenir, ardından her dosyanın veri akışı indirilir.</span><span class="sxs-lookup"><span data-stu-id="0afc2-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="0afc2-116">Bir dosya Kullanıcı veya uygulama tarafından indirme sırasında isteniyorsa, bu dosya erişim isteğini karşılamak için öncelik ile geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="0afc2-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="0afc2-117">Bu uç noktanın buluttan tüm dosya kümesi önbelleklerinde bulunup bulunmadığını belirlemek için isteğe bağlı olarak bu sunucu uç noktasında bulut kullanımı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0afc2-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="0afc2-118">Bulut katmanlarını kullandıysanız, dosya içeriği indirmesi, ayarlayabileceğiniz bulut katmanlama ilkeleriyle tanımlanan noktada durur.</span><span class="sxs-lookup"><span data-stu-id="0afc2-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="0afc2-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0afc2-119">EXAMPLES</span></span>

### <span data-ttu-id="0afc2-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0afc2-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="0afc2-121">Bu komut, kaydedilmiş bir sunucuda yeni bir sunucu uç noktası oluşturur ve bunu bir eşitleme grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="0afc2-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="0afc2-122">Bu şekilde, diğer uç noktaları ve dosya meta verileri topolojisinin bir parçası vardır ve içerik, eşitleme grubunda son nokta olarak başvurulan tüm konumlar arasında hemen eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="0afc2-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="0afc2-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0afc2-123">PARAMETERS</span></span>

### <span data-ttu-id="0afc2-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="0afc2-124">-AsJob</span></span>
<span data-ttu-id="0afc2-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0afc2-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0afc2-126">-Cloudbir</span><span class="sxs-lookup"><span data-stu-id="0afc2-126">-CloudTiering</span></span>
<span data-ttu-id="0afc2-127">Bulut katmanlama parametresi</span><span class="sxs-lookup"><span data-stu-id="0afc2-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="0afc2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0afc2-128">-DefaultProfile</span></span>
<span data-ttu-id="0afc2-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0afc2-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0afc2-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="0afc2-130">-Name</span></span>
<span data-ttu-id="0afc2-131">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="0afc2-131">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0afc2-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="0afc2-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="0afc2-133">Bulut çekirdek verileri parametresi</span><span class="sxs-lookup"><span data-stu-id="0afc2-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="0afc2-134">-Offlinedatatransferpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="0afc2-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="0afc2-135">Cloud seeded veri dosyası paylaşımı URI parametresi</span><span class="sxs-lookup"><span data-stu-id="0afc2-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="0afc2-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0afc2-136">-ParentObject</span></span>
<span data-ttu-id="0afc2-137">Normalde parametre aracılığıyla geçirilen SyncGroup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0afc2-137">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0afc2-138">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="0afc2-138">-ParentResourceId</span></span>
<span data-ttu-id="0afc2-139">SyncGroup üst kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0afc2-139">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0afc2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0afc2-140">-ResourceGroupName</span></span>
<span data-ttu-id="0afc2-141">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0afc2-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="0afc2-142">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="0afc2-142">-ServerLocalPath</span></span>
<span data-ttu-id="0afc2-143">Sunucu yerel yol parametresi</span><span class="sxs-lookup"><span data-stu-id="0afc2-143">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="0afc2-144">-Serverresourceıd</span><span class="sxs-lookup"><span data-stu-id="0afc2-144">-ServerResourceId</span></span>
<span data-ttu-id="0afc2-145">RegisteredServer kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="0afc2-145">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="0afc2-146">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0afc2-146">-StorageSyncServiceName</span></span>
<span data-ttu-id="0afc2-147">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="0afc2-147">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0afc2-148">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0afc2-148">-SyncGroupName</span></span>
<span data-ttu-id="0afc2-149">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="0afc2-149">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="0afc2-150">-Tierfilesolderergünü</span><span class="sxs-lookup"><span data-stu-id="0afc2-150">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="0afc2-151">Days parametresinden eski katman dosyaları</span><span class="sxs-lookup"><span data-stu-id="0afc2-151">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="0afc2-152">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="0afc2-152">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="0afc2-153">Disk alanı yüzde parametresi</span><span class="sxs-lookup"><span data-stu-id="0afc2-153">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="0afc2-154">-Onay</span><span class="sxs-lookup"><span data-stu-id="0afc2-154">-Confirm</span></span>
<span data-ttu-id="0afc2-155">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0afc2-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0afc2-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0afc2-156">-WhatIf</span></span>
<span data-ttu-id="0afc2-157">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0afc2-157">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0afc2-158">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0afc2-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0afc2-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0afc2-159">CommonParameters</span></span>
<span data-ttu-id="0afc2-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0afc2-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0afc2-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0afc2-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0afc2-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0afc2-162">INPUTS</span></span>

### <span data-ttu-id="0afc2-163">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0afc2-163">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="0afc2-164">System. String</span><span class="sxs-lookup"><span data-stu-id="0afc2-164">System.String</span></span>

## <span data-ttu-id="0afc2-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0afc2-165">OUTPUTS</span></span>

### <span data-ttu-id="0afc2-166">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0afc2-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="0afc2-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0afc2-167">NOTES</span></span>

## <span data-ttu-id="0afc2-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0afc2-168">RELATED LINKS</span></span>