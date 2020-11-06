---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589168"
---
# <span data-ttu-id="7f580-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7f580-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="7f580-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f580-102">SYNOPSIS</span></span>
<span data-ttu-id="7f580-103">Azure Site Recovery çoğaltma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f580-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f580-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f580-104">SYNTAX</span></span>

### <span data-ttu-id="7f580-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f580-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f580-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="7f580-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f580-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f580-107">DESCRIPTION</span></span>
<span data-ttu-id="7f580-108">**New-AzureRmRecoveryServicesAsrPolicy** cmdlet 'ı bir Azure Site Recovery çoğaltma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f580-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="7f580-109">Çoğaltma İlkesi, çoğaltma sıklığı ve kurtarma noktaları sayısı gibi çoğaltma ayarlarını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7f580-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="7f580-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f580-110">EXAMPLES</span></span>

### <span data-ttu-id="7f580-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f580-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="7f580-112">Belirtilen parametreleri kullanarak çoğaltma ilkesi oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7f580-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7f580-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f580-113">PARAMETERS</span></span>

### <span data-ttu-id="7f580-114">-Applicationpotentın</span><span class="sxs-lookup"><span data-stu-id="7f580-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="7f580-115">Uygulamayla tutarlı kurtarma noktalarının oluşturulacağı sıklığı (saat) belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="7f580-116">-Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="7f580-116">-Authentication</span></span>
<span data-ttu-id="7f580-117">Kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="7f580-118">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="7f580-118">Valid values are:</span></span>

- <span data-ttu-id="7f580-119">Sertifika</span><span class="sxs-lookup"><span data-stu-id="7f580-119">Certificate</span></span>
-  <span data-ttu-id="7f580-120">Kerberos</span><span class="sxs-lookup"><span data-stu-id="7f580-120">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f580-121">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="7f580-121">-Compression</span></span>
<span data-ttu-id="7f580-122">Sıkıştırmanın etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-122">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f580-123">-Şifreleme</span><span class="sxs-lookup"><span data-stu-id="7f580-123">-Encryption</span></span>
<span data-ttu-id="7f580-124">Şifrelemenin etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f580-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f580-125">-Name</span></span>
<span data-ttu-id="7f580-126">ASR çoğaltma ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-126">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="7f580-127">-Numberofrecoverypointstokoru</span><span class="sxs-lookup"><span data-stu-id="7f580-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="7f580-128">Korunacak sayı kurtarma noktalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-128">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="7f580-129">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="7f580-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="7f580-130">Çoğaltma hedefinin Azure depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="7f580-131">New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet kullanılarak çoğaltmayı etkinleştirirken alternatif sağlanmadıysa, çoğaltma için hedef depolama hesabı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7f580-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f580-132">-Replicasilme</span><span class="sxs-lookup"><span data-stu-id="7f580-132">-ReplicaDeletion</span></span>
<span data-ttu-id="7f580-133">VMM yönetilen sitesinden diğerine çoğaltma devre dışı bırakılırken çoğaltma sanal makinesinin silinip silinmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f580-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="7f580-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="7f580-135">Çoğaltma sıklığı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="7f580-136">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="7f580-136">Valid values are:</span></span>

- <span data-ttu-id="7f580-137">30</span><span class="sxs-lookup"><span data-stu-id="7f580-137">30</span></span>
- <span data-ttu-id="7f580-138">300</span><span class="sxs-lookup"><span data-stu-id="7f580-138">300</span></span>
- <span data-ttu-id="7f580-139">900</span><span class="sxs-lookup"><span data-stu-id="7f580-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f580-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="7f580-140">-ReplicationMethod</span></span>
<span data-ttu-id="7f580-141">Çoğaltma yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-141">Specifies the replication method.</span></span>
<span data-ttu-id="7f580-142">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="7f580-142">Valid values are:</span></span>

- <span data-ttu-id="7f580-143">Medya</span><span class="sxs-lookup"><span data-stu-id="7f580-143">Online</span></span>
- <span data-ttu-id="7f580-144">Çalış</span><span class="sxs-lookup"><span data-stu-id="7f580-144">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f580-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="7f580-145">-ReplicationPort</span></span>
<span data-ttu-id="7f580-146">Çoğaltma için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-146">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f580-147">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="7f580-147">-ReplicationProvider</span></span>
<span data-ttu-id="7f580-148">Çoğaltma sağlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-148">Specifies the replication provider.</span></span>
<span data-ttu-id="7f580-149">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="7f580-149">Valid values are:</span></span>

- <span data-ttu-id="7f580-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="7f580-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="7f580-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="7f580-151">HyperVReplica2012</span></span>
- <span data-ttu-id="7f580-152">Hipervreplicaazure</span><span class="sxs-lookup"><span data-stu-id="7f580-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f580-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="7f580-153">-ReplicationStartTime</span></span>
<span data-ttu-id="7f580-154">Çoğaltmanın başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f580-154">Specifies the replication start time.</span></span>
<span data-ttu-id="7f580-155">İşin başında 24 saatten sonra olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f580-155">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="7f580-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f580-156">-Confirm</span></span>
<span data-ttu-id="7f580-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f580-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f580-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f580-158">-WhatIf</span></span>
<span data-ttu-id="7f580-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f580-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f580-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f580-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f580-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f580-161">CommonParameters</span></span>
<span data-ttu-id="7f580-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f580-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f580-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f580-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f580-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f580-164">INPUTS</span></span>

### <span data-ttu-id="7f580-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7f580-165">None</span></span>

## <span data-ttu-id="7f580-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f580-166">OUTPUTS</span></span>

### <span data-ttu-id="7f580-167">System. Object</span><span class="sxs-lookup"><span data-stu-id="7f580-167">System.Object</span></span>

## <span data-ttu-id="7f580-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f580-168">NOTES</span></span>

## <span data-ttu-id="7f580-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f580-169">RELATED LINKS</span></span>

[<span data-ttu-id="7f580-170">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7f580-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="7f580-171">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="7f580-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
