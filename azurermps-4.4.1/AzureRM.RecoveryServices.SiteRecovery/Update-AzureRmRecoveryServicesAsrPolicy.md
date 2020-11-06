---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593033"
---
# <span data-ttu-id="e6ba8-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e6ba8-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="e6ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ba8-103">Azure Site Recovery çoğaltma ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6ba8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6ba8-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ba8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="e6ba8-106">**Update-AzureRmRecoveryServicesAsrPolicy** cmdlet 'ı belirtilen Azure Site Recovery çoğaltma ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="e6ba8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6ba8-107">EXAMPLES</span></span>

### <span data-ttu-id="e6ba8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e6ba8-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="e6ba8-109">Belirtilen parametreleri kullanarak çoğaltmayı Güncelleştir ilkesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e6ba8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6ba8-110">PARAMETERS</span></span>

### <span data-ttu-id="e6ba8-111">-Applicationpotentın</span><span class="sxs-lookup"><span data-stu-id="e6ba8-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="e6ba8-112">Uygulamayla tutarlı kurtarma noktalarının oluşturulacağı sıklığı (saat) belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-113">-Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="e6ba8-113">-Authentication</span></span>
<span data-ttu-id="e6ba8-114">Kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="e6ba8-115">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-115">Valid values are:</span></span>

- <span data-ttu-id="e6ba8-116">Sertifika</span><span class="sxs-lookup"><span data-stu-id="e6ba8-116">Certificate</span></span>
-  <span data-ttu-id="e6ba8-117">Kerberos</span><span class="sxs-lookup"><span data-stu-id="e6ba8-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-118">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="e6ba8-118">-Compression</span></span>
<span data-ttu-id="e6ba8-119">Sıkıştırmanın etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-120">-Şifreleme</span><span class="sxs-lookup"><span data-stu-id="e6ba8-120">-Encryption</span></span>
<span data-ttu-id="e6ba8-121">Şifrelemenin etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6ba8-122">-InputObject</span></span>
<span data-ttu-id="e6ba8-123">Cmdlet için giriş nesnesi: güncelleştirilecek çoğaltma ilkesine karşılık gelen ASR çoğaltma ilkesi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-124">-Numberofrecoverypointstokoru</span><span class="sxs-lookup"><span data-stu-id="e6ba8-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="e6ba8-125">Korunacak sayı kurtarma noktalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-125">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-126">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="e6ba8-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="e6ba8-127">Çoğaltma hedefinin Azure depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="e6ba8-128">New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet kullanılarak çoğaltmayı etkinleştirirken alternatif sağlanmadıysa, çoğaltma için hedef depolama hesabı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-129">-Replicasilme</span><span class="sxs-lookup"><span data-stu-id="e6ba8-129">-ReplicaDeletion</span></span>
<span data-ttu-id="e6ba8-130">VMM yönetilen sitesinden diğerine çoğaltma devre dışı bırakılırken çoğaltma sanal makinesinin silinip silinmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="e6ba8-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="e6ba8-132">Çoğaltma sıklığı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="e6ba8-133">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-133">Valid values are:</span></span>

- <span data-ttu-id="e6ba8-134">30</span><span class="sxs-lookup"><span data-stu-id="e6ba8-134">30</span></span>
- <span data-ttu-id="e6ba8-135">300</span><span class="sxs-lookup"><span data-stu-id="e6ba8-135">300</span></span>
- <span data-ttu-id="e6ba8-136">900</span><span class="sxs-lookup"><span data-stu-id="e6ba8-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="e6ba8-137">-ReplicationMethod</span></span>
<span data-ttu-id="e6ba8-138">Çoğaltma yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-138">Specifies the replication method.</span></span>
<span data-ttu-id="e6ba8-139">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="e6ba8-139">Valid values are:</span></span>

- <span data-ttu-id="e6ba8-140">Medya</span><span class="sxs-lookup"><span data-stu-id="e6ba8-140">Online</span></span>
- <span data-ttu-id="e6ba8-141">Çalış</span><span class="sxs-lookup"><span data-stu-id="e6ba8-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="e6ba8-142">-ReplicationPort</span></span>
<span data-ttu-id="e6ba8-143">Çoğaltma için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="e6ba8-144">-ReplicationStartTime</span></span>
<span data-ttu-id="e6ba8-145">Çoğaltmanın başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-145">Specifies the replication start time.</span></span>
<span data-ttu-id="e6ba8-146">İşin başında 24 saatten sonra olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-146">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ba8-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="e6ba8-147">-Confirm</span></span>
<span data-ttu-id="e6ba8-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6ba8-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ba8-149">-WhatIf</span></span>
<span data-ttu-id="e6ba8-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6ba8-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6ba8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ba8-152">CommonParameters</span></span>
<span data-ttu-id="e6ba8-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6ba8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ba8-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ba8-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ba8-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6ba8-155">INPUTS</span></span>

### <span data-ttu-id="e6ba8-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="e6ba8-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="e6ba8-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6ba8-157">OUTPUTS</span></span>

### <span data-ttu-id="e6ba8-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="e6ba8-158">System.Object</span></span>

## <span data-ttu-id="e6ba8-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6ba8-159">NOTES</span></span>

## <span data-ttu-id="e6ba8-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6ba8-160">RELATED LINKS</span></span>

