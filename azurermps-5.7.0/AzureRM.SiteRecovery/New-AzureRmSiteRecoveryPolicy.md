---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 65e5e507259198cdacc69ff0764b4f4f18bf9077
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763967"
---
# <span data-ttu-id="287fc-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="287fc-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="287fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="287fc-102">SYNOPSIS</span></span>
<span data-ttu-id="287fc-103">Site kurtarma çoğaltma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="287fc-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="287fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="287fc-104">SYNTAX</span></span>

### <span data-ttu-id="287fc-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="287fc-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="287fc-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="287fc-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="287fc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="287fc-107">DESCRIPTION</span></span>
<span data-ttu-id="287fc-108">**New-AzureRmSiteRecoveryPolicy** cmdlet 'ı bir Azure Site Recovery çoğaltma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="287fc-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="287fc-109">Çoğaltma İlkesi, çoğaltma sıklığı ve kurtarma noktaları sayısı gibi çoğaltma ayarlarını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="287fc-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="287fc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="287fc-110">EXAMPLES</span></span>

## <span data-ttu-id="287fc-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="287fc-111">PARAMETERS</span></span>

### <span data-ttu-id="287fc-112">-Applicationpotentın</span><span class="sxs-lookup"><span data-stu-id="287fc-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="287fc-113">Uygulamayla tutarlı anlık görüntüsünün saat cinsinden sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

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

### <span data-ttu-id="287fc-114">-Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="287fc-114">-Authentication</span></span>
<span data-ttu-id="287fc-115">Kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="287fc-116">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="287fc-116">Valid values are:</span></span>

- <span data-ttu-id="287fc-117">Sertifika</span><span class="sxs-lookup"><span data-stu-id="287fc-117">Certificate</span></span>
-  <span data-ttu-id="287fc-118">Kerberos</span><span class="sxs-lookup"><span data-stu-id="287fc-118">Kerberos</span></span>

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

### <span data-ttu-id="287fc-119">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="287fc-119">-Compression</span></span>
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

### <span data-ttu-id="287fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287fc-120">-DefaultProfile</span></span>
<span data-ttu-id="287fc-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="287fc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="287fc-122">-Şifreleme</span><span class="sxs-lookup"><span data-stu-id="287fc-122">-Encryption</span></span>
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

### <span data-ttu-id="287fc-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="287fc-123">-Name</span></span>
<span data-ttu-id="287fc-124">Site kurtarma çoğaltma ilkesini tanımlayan kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-124">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="287fc-125">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="287fc-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="287fc-126">Çoğaltma hedefinin Azure depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-126">Specifies the Azure storage account ID of the replication target.</span></span>

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

### <span data-ttu-id="287fc-127">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="287fc-127">-RecoveryPoints</span></span>
<span data-ttu-id="287fc-128">Kurtarma noktalarının tutulacağı saat sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-128">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="287fc-129">-Replicasilme</span><span class="sxs-lookup"><span data-stu-id="287fc-129">-ReplicaDeletion</span></span>
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

### <span data-ttu-id="287fc-130">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="287fc-130">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="287fc-131">Çoğaltma sıklığı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-131">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="287fc-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="287fc-132">Valid values are:</span></span>

- <span data-ttu-id="287fc-133">30</span><span class="sxs-lookup"><span data-stu-id="287fc-133">30</span></span>
- <span data-ttu-id="287fc-134">300</span><span class="sxs-lookup"><span data-stu-id="287fc-134">300</span></span>
- <span data-ttu-id="287fc-135">900</span><span class="sxs-lookup"><span data-stu-id="287fc-135">900</span></span>

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

### <span data-ttu-id="287fc-136">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="287fc-136">-ReplicationMethod</span></span>
<span data-ttu-id="287fc-137">Çoğaltma yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-137">Specifies the replication method.</span></span>
<span data-ttu-id="287fc-138">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="287fc-138">Valid values are:</span></span>

- <span data-ttu-id="287fc-139">Medya</span><span class="sxs-lookup"><span data-stu-id="287fc-139">Online</span></span>
- <span data-ttu-id="287fc-140">Çalış</span><span class="sxs-lookup"><span data-stu-id="287fc-140">Offline</span></span>

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

### <span data-ttu-id="287fc-141">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="287fc-141">-ReplicationPort</span></span>
<span data-ttu-id="287fc-142">Çoğaltma için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-142">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="287fc-143">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="287fc-143">-ReplicationProvider</span></span>
<span data-ttu-id="287fc-144">Çoğaltma sağlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-144">Specifies the replication provider.</span></span>
<span data-ttu-id="287fc-145">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="287fc-145">Valid values are:</span></span>

- <span data-ttu-id="287fc-146">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="287fc-146">HyperVReplica2012R2</span></span>
- <span data-ttu-id="287fc-147">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="287fc-147">HyperVReplica2012</span></span>
- <span data-ttu-id="287fc-148">Hipervreplicaazure</span><span class="sxs-lookup"><span data-stu-id="287fc-148">HyperVReplicaAzure</span></span>

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

### <span data-ttu-id="287fc-149">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="287fc-149">-ReplicationStartTime</span></span>
<span data-ttu-id="287fc-150">Çoğaltmanın başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="287fc-150">Specifies the replication start time.</span></span>
<span data-ttu-id="287fc-151">İşin başında 24 saatten sonra olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="287fc-151">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="287fc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287fc-152">CommonParameters</span></span>
<span data-ttu-id="287fc-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="287fc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287fc-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="287fc-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287fc-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="287fc-155">INPUTS</span></span>

### <span data-ttu-id="287fc-156">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="287fc-156">None</span></span>
<span data-ttu-id="287fc-157">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="287fc-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="287fc-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="287fc-158">OUTPUTS</span></span>

## <span data-ttu-id="287fc-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="287fc-159">NOTES</span></span>

## <span data-ttu-id="287fc-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="287fc-160">RELATED LINKS</span></span>

[<span data-ttu-id="287fc-161">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="287fc-161">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="287fc-162">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="287fc-162">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
