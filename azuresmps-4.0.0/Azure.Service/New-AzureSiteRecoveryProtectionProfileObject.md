---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105891"
---
# <span data-ttu-id="0c215-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="0c215-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="0c215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c215-102">SYNOPSIS</span></span>
<span data-ttu-id="0c215-103">Site kurtarma koruma profili nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c215-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="0c215-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c215-104">SYNTAX</span></span>

### <span data-ttu-id="0c215-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c215-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0c215-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="0c215-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0c215-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c215-107">DESCRIPTION</span></span>
<span data-ttu-id="0c215-108">**New-AzureSiteRecoveryProtectionProfileObject** cmdlet 'ı bir Azure Site Recovery Protection profili nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c215-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="0c215-109">Bu cmdlet diğer cmdlet 'ler ile kullanmak için bir **Asrprotectionprofile** nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c215-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="0c215-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c215-110">EXAMPLES</span></span>

### <span data-ttu-id="0c215-111">Örnek 1: koruma profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c215-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="0c215-112">Bu komut, bir koruma profili nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c215-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="0c215-113">Örnek 2: Hipervreplicaazure sağlayıcısı için bir koruma profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="0c215-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="0c215-114">Bu komut, HyperVReplicaAzure sağlayıcısı için bir koruma profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0c215-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="0c215-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c215-115">PARAMETERS</span></span>

### <span data-ttu-id="0c215-116">-Allowreplicasilme</span><span class="sxs-lookup"><span data-stu-id="0c215-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="0c215-117">Koruma profilinin çoğaltma varlıklarının silinmesini etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c215-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c215-118">-Applicationpotentın</span><span class="sxs-lookup"><span data-stu-id="0c215-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="0c215-119">Uygulamayla tutarlı anlık görüntüler için saat cinsinden sıklığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="0c215-120">-Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="0c215-120">-Authentication</span></span>
<span data-ttu-id="0c215-121">Kullanılacak kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="0c215-122">Bu parametre için kabul edilebilir değerler: sertifika ve Kerberos.</span><span class="sxs-lookup"><span data-stu-id="0c215-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c215-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="0c215-123">-CompressionEnabled</span></span>
<span data-ttu-id="0c215-124">Koruma profilinin sıkıştırmayı etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c215-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c215-125">-Force</span><span class="sxs-lookup"><span data-stu-id="0c215-125">-Force</span></span>
<span data-ttu-id="0c215-126">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0c215-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c215-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c215-127">-Name</span></span>
<span data-ttu-id="0c215-128">Koruma profili için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="0c215-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="0c215-129">-Profile</span></span>
<span data-ttu-id="0c215-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c215-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0c215-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c215-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0c215-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="0c215-133">Azure çoğaltma varlığının depolanacağı Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c215-134">-Kurtarılan betikte</span><span class="sxs-lookup"><span data-stu-id="0c215-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="0c215-135">Bir depolama hesabı için Azure aboneliğinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="0c215-136">Bu parametre, Azure çoğaltma varlığının depolanacağı hesaba başvurur.</span><span class="sxs-lookup"><span data-stu-id="0c215-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c215-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="0c215-137">-RecoveryPoints</span></span>
<span data-ttu-id="0c215-138">Kurtarma noktalarının tutulacağı saat sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="0c215-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="0c215-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="0c215-140">Yineleme için sıklık aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="0c215-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0c215-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c215-142">30</span><span class="sxs-lookup"><span data-stu-id="0c215-142">30</span></span> 
- <span data-ttu-id="0c215-143">300</span><span class="sxs-lookup"><span data-stu-id="0c215-143">300</span></span> 
- <span data-ttu-id="0c215-144">900</span><span class="sxs-lookup"><span data-stu-id="0c215-144">900</span></span>

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

### <span data-ttu-id="0c215-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="0c215-145">-ReplicationMethod</span></span>
<span data-ttu-id="0c215-146">Çoğaltma yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-146">Specifies the replication method.</span></span> <span data-ttu-id="0c215-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0c215-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0c215-148">Medya.</span><span class="sxs-lookup"><span data-stu-id="0c215-148">Online.</span></span>
<span data-ttu-id="0c215-149">Ağ üzerinden çoğaltma.</span><span class="sxs-lookup"><span data-stu-id="0c215-149">Replication over the network.</span></span>
- <span data-ttu-id="0c215-150">Çalış.</span><span class="sxs-lookup"><span data-stu-id="0c215-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c215-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="0c215-151">-ReplicationPort</span></span>
<span data-ttu-id="0c215-152">Çoğaltmanın gerçekleştiği bağlantı noktası numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="0c215-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="0c215-153">-ReplicationProvider</span></span>
<span data-ttu-id="0c215-154">Çoğaltma sağlayıcısının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="0c215-155">Bu parametre için kabul edilebilir değerler: Hipervreplica ve HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="0c215-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="0c215-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="0c215-156">-ReplicationStartTime</span></span>
<span data-ttu-id="0c215-157">Çoğaltmanın başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c215-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="0c215-158">İşi başlattıktan sonra 24 saat içinde bir süre belirtin.</span><span class="sxs-lookup"><span data-stu-id="0c215-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="0c215-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c215-159">CommonParameters</span></span>
<span data-ttu-id="0c215-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c215-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c215-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c215-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c215-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c215-162">INPUTS</span></span>

## <span data-ttu-id="0c215-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c215-163">OUTPUTS</span></span>

## <span data-ttu-id="0c215-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c215-164">NOTES</span></span>

## <span data-ttu-id="0c215-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c215-165">RELATED LINKS</span></span>

[<span data-ttu-id="0c215-166">Azure Site Recovery Hizmetleri cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="0c215-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


