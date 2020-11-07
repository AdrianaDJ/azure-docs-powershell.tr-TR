---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764505"
---
# <span data-ttu-id="a1404-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a1404-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="a1404-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1404-102">SYNOPSIS</span></span>
<span data-ttu-id="a1404-103">Site kurtarma çoğaltma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1404-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1404-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1404-104">SYNTAX</span></span>

### <span data-ttu-id="a1404-105">EnterpriseToAzure (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1404-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1404-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a1404-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1404-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1404-107">DESCRIPTION</span></span>
<span data-ttu-id="a1404-108">**New-AzureRmSiteRecoveryPolicy** cmdlet 'ı bir Azure Site Recovery çoğaltma ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1404-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="a1404-109">Çoğaltma İlkesi, çoğaltma sıklığı ve kurtarma noktaları sayısı gibi çoğaltma ayarlarını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a1404-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="a1404-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1404-110">EXAMPLES</span></span>

## <span data-ttu-id="a1404-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1404-111">PARAMETERS</span></span>

### <span data-ttu-id="a1404-112">-Applicationpotentın</span><span class="sxs-lookup"><span data-stu-id="a1404-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="a1404-113">Uygulamayla tutarlı anlık görüntüsünün saat cinsinden sıklığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-114">-Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="a1404-114">-Authentication</span></span>
<span data-ttu-id="a1404-115">Kullanılan kimlik doğrulama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="a1404-116">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a1404-116">Valid values are:</span></span>

- <span data-ttu-id="a1404-117">Sertifika</span><span class="sxs-lookup"><span data-stu-id="a1404-117">Certificate</span></span>
-  <span data-ttu-id="a1404-118">Kerberos</span><span class="sxs-lookup"><span data-stu-id="a1404-118">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-119">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="a1404-119">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-120">-Şifreleme</span><span class="sxs-lookup"><span data-stu-id="a1404-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1404-121">-Name</span></span>
<span data-ttu-id="a1404-122">Site kurtarma çoğaltma ilkesini tanımlayan kolay bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="a1404-123">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="a1404-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a1404-124">Çoğaltma hedefinin Azure depolama hesabı KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="a1404-125">-RecoveryPoints</span></span>
<span data-ttu-id="a1404-126">Kurtarma noktalarının tutulacağı saat sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-126">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-127">-Replicasilme</span><span class="sxs-lookup"><span data-stu-id="a1404-127">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="a1404-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="a1404-129">Çoğaltma sıklığı aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="a1404-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a1404-130">Valid values are:</span></span>

- <span data-ttu-id="a1404-131">30</span><span class="sxs-lookup"><span data-stu-id="a1404-131">30</span></span>
- <span data-ttu-id="a1404-132">300</span><span class="sxs-lookup"><span data-stu-id="a1404-132">300</span></span>
- <span data-ttu-id="a1404-133">900</span><span class="sxs-lookup"><span data-stu-id="a1404-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="a1404-134">-ReplicationMethod</span></span>
<span data-ttu-id="a1404-135">Çoğaltma yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-135">Specifies the replication method.</span></span>
<span data-ttu-id="a1404-136">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a1404-136">Valid values are:</span></span>

- <span data-ttu-id="a1404-137">Medya</span><span class="sxs-lookup"><span data-stu-id="a1404-137">Online</span></span>
- <span data-ttu-id="a1404-138">Çalış</span><span class="sxs-lookup"><span data-stu-id="a1404-138">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="a1404-139">-ReplicationPort</span></span>
<span data-ttu-id="a1404-140">Çoğaltma için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-140">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-141">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="a1404-141">-ReplicationProvider</span></span>
<span data-ttu-id="a1404-142">Çoğaltma sağlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-142">Specifies the replication provider.</span></span>
<span data-ttu-id="a1404-143">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="a1404-143">Valid values are:</span></span>

- <span data-ttu-id="a1404-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="a1404-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="a1404-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="a1404-145">HyperVReplica2012</span></span>
- <span data-ttu-id="a1404-146">Hipervreplicaazure</span><span class="sxs-lookup"><span data-stu-id="a1404-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="a1404-147">-ReplicationStartTime</span></span>
<span data-ttu-id="a1404-148">Çoğaltmanın başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1404-148">Specifies the replication start time.</span></span>
<span data-ttu-id="a1404-149">İşin başında 24 saatten sonra olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a1404-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1404-150">-DefaultProfile</span></span>
<span data-ttu-id="a1404-151">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1404-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1404-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1404-152">CommonParameters</span></span>
<span data-ttu-id="a1404-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1404-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1404-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1404-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1404-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1404-155">INPUTS</span></span>

## <span data-ttu-id="a1404-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1404-156">OUTPUTS</span></span>

## <span data-ttu-id="a1404-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1404-157">NOTES</span></span>

## <span data-ttu-id="a1404-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1404-158">RELATED LINKS</span></span>

[<span data-ttu-id="a1404-159">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a1404-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="a1404-160">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="a1404-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
