---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 53da56d932d3e2b57c2b2bbf17107918c9c1226d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324880"
---
# <span data-ttu-id="06402-101">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06402-101">New-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="06402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06402-102">SYNOPSIS</span></span>
<span data-ttu-id="06402-103">Bu komut, kaydedilmiş bir sunucuda yeni bir sunucu uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06402-103">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="06402-104">Bu, sunucudaki belirtilen yolun eşitleme grubundaki diğer uç noktalarla birlikte dosyaları eşitlemeye başlamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="06402-104">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

## <span data-ttu-id="06402-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06402-105">SYNTAX</span></span>

### <span data-ttu-id="06402-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06402-106">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06402-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06402-107">ObjectParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06402-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="06402-108">ParentStringParameterSet</span></span>
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [InitialDownloadPolicy] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06402-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="06402-109">DESCRIPTION</span></span>
<span data-ttu-id="06402-110">Bu komut, kaydedilmiş bir sunucuda yeni bir sunucu uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06402-110">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="06402-111">Bu, sunucudaki belirtilen yolun eşitleme grubundaki diğer uç noktalarla birlikte dosyaları eşitlemeye başlamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="06402-111">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span> <span data-ttu-id="06402-112">Eşitleme grubundaki diğer uç noktalarda dosyalar varsa ve bu yeni eklenen konum da dosya içeriyorsa, bir mutabakat süreci, dosyaların aslında diğer uç noktalardan aynı klasörlerde olduğunu belirlemeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="06402-112">If there are already files on other endpoints in the sync group and this newly added location also contains files, a reconciliation process will attempt to determine if files are in fact the same ones in the same folders as on other endpoints.</span></span> <span data-ttu-id="06402-113">Ad alanları, çakışma dosyalarını birleştirip Uzlaşmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="06402-113">The namespaces will merge and reconciliation helps to prevent conflict files.</span></span> <span data-ttu-id="06402-114">Diğer sunucu uç noktalarında dosyalar varsa, bu sunucudaki dosyaların boş bir konumla başlaması genellikle daha iyi olur, böylece bulut dosyaları, hızlı çökme kurtarması adlı otomatik bir işlemde sunucuya geliyor.</span><span class="sxs-lookup"><span data-stu-id="06402-114">If there are files on other server endpoints it is often better to start with an empty location on this server, so that the files from the cloud come down to the server in an automatic process called fast disaster recovery.</span></span> <span data-ttu-id="06402-115">Ad alanı meta verileri ilk olarak eşitlenir, ardından her dosyanın veri akışı indirilir.</span><span class="sxs-lookup"><span data-stu-id="06402-115">Namespace metadata will be synced down first, then the data stream of each file is downloaded.</span></span> <span data-ttu-id="06402-116">Bir dosya Kullanıcı veya uygulama tarafından indirme sırasında isteniyorsa, bu dosya erişim isteğini karşılamak için öncelik ile geri yüklenir.</span><span class="sxs-lookup"><span data-stu-id="06402-116">If a file is requested by a user or application out of download order, that file will be recalled with priority to satisfy the access request.</span></span> <span data-ttu-id="06402-117">Bu uç noktanın buluttan tüm dosya kümesi önbelleklerinde bulunup bulunmadığını belirlemek için isteğe bağlı olarak bu sunucu uç noktasında bulut kullanımı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="06402-117">You can optionally use cloud tiering on this server endpoint to determine if this endpoint is supposed to become a cache of the complete set of files from the cloud.</span></span> <span data-ttu-id="06402-118">Bulut katmanlarını kullandıysanız, dosya içeriği indirmesi, ayarlayabileceğiniz bulut katmanlama ilkeleriyle tanımlanan noktada durur.</span><span class="sxs-lookup"><span data-stu-id="06402-118">If cloud tiering is used, then the file content download will stop at the point defined by the cloud tiering policies you can set.</span></span>

## <span data-ttu-id="06402-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06402-119">EXAMPLES</span></span>

### <span data-ttu-id="06402-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06402-120">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

<span data-ttu-id="06402-121">Bu komut, kaydedilmiş bir sunucuda yeni bir sunucu uç noktası oluşturur ve bunu bir eşitleme grubuna ekler.</span><span class="sxs-lookup"><span data-stu-id="06402-121">This command creates a new server endpoint on a registered server and inserts it into a sync group.</span></span> <span data-ttu-id="06402-122">Bu şekilde, diğer uç noktaları ve dosya meta verileri topolojisinin bir parçası vardır ve içerik, eşitleme grubunda son nokta olarak başvurulan tüm konumlar arasında hemen eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="06402-122">THis way it is part of a topology of other endpoints and file metadata and content will immediately start to sync between all locations referenced as endpoints in the sync group.</span></span>

## <span data-ttu-id="06402-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06402-123">PARAMETERS</span></span>

### <span data-ttu-id="06402-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="06402-124">-AsJob</span></span>
<span data-ttu-id="06402-125">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="06402-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="06402-126">-Cloudbir</span><span class="sxs-lookup"><span data-stu-id="06402-126">-CloudTiering</span></span>
<span data-ttu-id="06402-127">Bulut katmanlama parametresi</span><span class="sxs-lookup"><span data-stu-id="06402-127">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="06402-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06402-128">-DefaultProfile</span></span>
<span data-ttu-id="06402-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06402-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06402-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="06402-130">-Name</span></span>
<span data-ttu-id="06402-131">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="06402-131">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="06402-132">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="06402-132">-OfflineDataTransfer</span></span>
<span data-ttu-id="06402-133">Bulut çekirdek verileri parametresi</span><span class="sxs-lookup"><span data-stu-id="06402-133">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="06402-134">-Offlinedatatransferpaylaşımadı</span><span class="sxs-lookup"><span data-stu-id="06402-134">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="06402-135">Cloud seeded veri dosyası paylaşımı URI parametresi</span><span class="sxs-lookup"><span data-stu-id="06402-135">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="06402-136">-ınitialdownloadpolicy</span><span class="sxs-lookup"><span data-stu-id="06402-136">-initialDownloadPolicy</span></span>
<span data-ttu-id="06402-137">Yerel önbellek modu parametresi</span><span class="sxs-lookup"><span data-stu-id="06402-137">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="06402-138">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="06402-138">-localCacheMode</span></span>
<span data-ttu-id="06402-139">Yerel önbellek modu parametresi</span><span class="sxs-lookup"><span data-stu-id="06402-139">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="06402-140">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="06402-140">-ParentObject</span></span>
<span data-ttu-id="06402-141">Normalde parametre aracılığıyla geçirilen SyncGroup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="06402-141">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="06402-142">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="06402-142">-ParentResourceId</span></span>
<span data-ttu-id="06402-143">SyncGroup üst kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="06402-143">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="06402-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06402-144">-ResourceGroupName</span></span>
<span data-ttu-id="06402-145">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="06402-145">Resource Group Name.</span></span>

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

### <span data-ttu-id="06402-146">-ServerLocalPath</span><span class="sxs-lookup"><span data-stu-id="06402-146">-ServerLocalPath</span></span>
<span data-ttu-id="06402-147">Sunucu yerel yol parametresi</span><span class="sxs-lookup"><span data-stu-id="06402-147">Server Local Path Parameter</span></span>

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

### <span data-ttu-id="06402-148">-Serverresourceıd</span><span class="sxs-lookup"><span data-stu-id="06402-148">-ServerResourceId</span></span>
<span data-ttu-id="06402-149">RegisteredServer kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="06402-149">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="06402-150">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="06402-150">-StorageSyncServiceName</span></span>
<span data-ttu-id="06402-151">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="06402-151">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="06402-152">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="06402-152">-SyncGroupName</span></span>
<span data-ttu-id="06402-153">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="06402-153">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="06402-154">-Tierfilesolderergünü</span><span class="sxs-lookup"><span data-stu-id="06402-154">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="06402-155">Days parametresinden eski katman dosyaları</span><span class="sxs-lookup"><span data-stu-id="06402-155">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="06402-156">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="06402-156">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="06402-157">Disk alanı yüzde parametresi</span><span class="sxs-lookup"><span data-stu-id="06402-157">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="06402-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="06402-158">-Confirm</span></span>
<span data-ttu-id="06402-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06402-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06402-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06402-160">-WhatIf</span></span>
<span data-ttu-id="06402-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06402-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06402-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06402-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06402-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06402-163">CommonParameters</span></span>
<span data-ttu-id="06402-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06402-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06402-165">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06402-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06402-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06402-166">INPUTS</span></span>

### <span data-ttu-id="06402-167">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="06402-167">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="06402-168">System. String</span><span class="sxs-lookup"><span data-stu-id="06402-168">System.String</span></span>

## <span data-ttu-id="06402-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06402-169">OUTPUTS</span></span>

### <span data-ttu-id="06402-170">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="06402-170">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="06402-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06402-171">NOTES</span></span>

## <span data-ttu-id="06402-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06402-172">RELATED LINKS</span></span>
