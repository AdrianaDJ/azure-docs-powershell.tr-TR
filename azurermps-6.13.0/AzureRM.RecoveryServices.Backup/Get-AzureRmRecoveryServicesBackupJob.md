---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 0ed0ed82c1f2c030ab10fc6a96d1582fdb34b7d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593192"
---
# <span data-ttu-id="bb65e-101">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="bb65e-101">Get-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="bb65e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb65e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb65e-103">Yedekleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="bb65e-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb65e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb65e-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb65e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb65e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb65e-106">**Get-AzureRmRecoveryServicesBackupJob** cmdlet 'i, belirli bir kasa Için Azure yedekleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="bb65e-106">The **Get-AzureRmRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="bb65e-107">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bb65e-107">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bb65e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb65e-108">EXAMPLES</span></span>

### <span data-ttu-id="bb65e-109">Örnek 1: devam eden tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="bb65e-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzureRMRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="bb65e-110">İlk komut bir ilerleme durumu işinin durumunu dizi olarak alır ve sonra bunu $Joblist değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="bb65e-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="bb65e-111">İkinci komut $Joblist dizisindeki ilk öğeyi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="bb65e-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="bb65e-112">Örnek 2: son 7 gündeki tüm başarısız işleri alma</span><span class="sxs-lookup"><span data-stu-id="bb65e-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="bb65e-113">Bu komut, kasadaki geçen haftanın başarısız işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="bb65e-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="bb65e-114">*From* parametresi, geçmişte UTC 'de belirtilen saat yedi gün içinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="bb65e-115">Komut *to* parametresi için bir değer belirtmiyor.</span><span class="sxs-lookup"><span data-stu-id="bb65e-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="bb65e-116">Bu nedenle, geçerli zamanın varsayılan değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="bb65e-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="bb65e-117">Örnek 3: devam eden bir iş edinme ve tamamlanma işlemini bekleme</span><span class="sxs-lookup"><span data-stu-id="bb65e-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="bb65e-118">Bu komut dosyası, iş tamamlanana kadar devam eden ilk işi yoklar.</span><span class="sxs-lookup"><span data-stu-id="bb65e-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="bb65e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb65e-119">PARAMETERS</span></span>

### <span data-ttu-id="bb65e-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="bb65e-120">-BackupManagementType</span></span>
<span data-ttu-id="bb65e-121">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="bb65e-122">Şu anda, yalnızca AzureVM, AzureStorage destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="bb65e-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb65e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb65e-123">-DefaultProfile</span></span>
<span data-ttu-id="bb65e-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb65e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb65e-125">'Den</span><span class="sxs-lookup"><span data-stu-id="bb65e-125">-From</span></span>
<span data-ttu-id="bb65e-126">Bu cmdlet 'in aldığı işler için zaman aralığının başlangıç, **DateTime** nesnesi olarak başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="bb65e-127">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb65e-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="bb65e-128">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="bb65e-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="bb65e-129">Tarihler için UTC biçimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb65e-129">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb65e-130">-Job</span><span class="sxs-lookup"><span data-stu-id="bb65e-130">-Job</span></span>
<span data-ttu-id="bb65e-131">Alınacak yedekleme işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-131">Specifies the name of the Backup job to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb65e-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="bb65e-132">-JobId</span></span>
<span data-ttu-id="bb65e-133">Bu cmdlet 'in aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="bb65e-134">ID, **Azurermrecoveryservicesbackupjob** nesnesinin InstanceId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="bb65e-135">**Azurermrecoveryservicesbackupjob** nesnesi almak için Get-AzureRmRecoveryServicesBackupJob seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb65e-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb65e-136">-İşlem</span><span class="sxs-lookup"><span data-stu-id="bb65e-136">-Operation</span></span>
<span data-ttu-id="bb65e-137">Bu cmdlet 'in aldığı işlerin bir işlemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="bb65e-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bb65e-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb65e-139">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="bb65e-139">Backup</span></span>
- <span data-ttu-id="bb65e-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="bb65e-140">ConfigureBackup</span></span>
- <span data-ttu-id="bb65e-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="bb65e-141">DeleteBackupData</span></span>
- <span data-ttu-id="bb65e-142">Kaydettiremedi</span><span class="sxs-lookup"><span data-stu-id="bb65e-142">Register</span></span>
- <span data-ttu-id="bb65e-143">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="bb65e-143">Restore</span></span>
- <span data-ttu-id="bb65e-144">Sayfa korumasını kaldır</span><span class="sxs-lookup"><span data-stu-id="bb65e-144">UnProtect</span></span>
- <span data-ttu-id="bb65e-145">Kaldırabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bb65e-145">Unregister</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb65e-146">-Durum</span><span class="sxs-lookup"><span data-stu-id="bb65e-146">-Status</span></span>
<span data-ttu-id="bb65e-147">Bu cmdlet 'in aldığı işlerin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="bb65e-148">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bb65e-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bb65e-149">Progress</span><span class="sxs-lookup"><span data-stu-id="bb65e-149">InProgress</span></span>
- <span data-ttu-id="bb65e-150">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="bb65e-150">Failed</span></span>
- <span data-ttu-id="bb65e-151">İptal</span><span class="sxs-lookup"><span data-stu-id="bb65e-151">Cancelled</span></span>
- <span data-ttu-id="bb65e-152">Edilirse</span><span class="sxs-lookup"><span data-stu-id="bb65e-152">Cancelling</span></span>
- <span data-ttu-id="bb65e-153">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="bb65e-153">Completed</span></span>
- <span data-ttu-id="bb65e-154">Completeduyarıları</span><span class="sxs-lookup"><span data-stu-id="bb65e-154">CompletedWithWarnings</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb65e-155">-To</span><span class="sxs-lookup"><span data-stu-id="bb65e-155">-To</span></span>
<span data-ttu-id="bb65e-156">Bu cmdlet 'in aldığı işler için zaman aralığının sonunu bir **Tarih saat** olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="bb65e-157">Varsayılan değer geçerli sistem saatinin değeridir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-157">The default value is the current system time.</span></span>
<span data-ttu-id="bb65e-158">Bu parametreyi belirtirseniz, *from* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb65e-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="bb65e-159">Tarihler için UTC biçimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bb65e-159">Use UTC format for dates.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb65e-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bb65e-160">-VaultId</span></span>
<span data-ttu-id="bb65e-161">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bb65e-161">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb65e-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb65e-162">CommonParameters</span></span>
<span data-ttu-id="bb65e-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb65e-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb65e-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb65e-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb65e-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb65e-165">INPUTS</span></span>

### <span data-ttu-id="bb65e-166">System. String</span><span class="sxs-lookup"><span data-stu-id="bb65e-166">System.String</span></span>
<span data-ttu-id="bb65e-167">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bb65e-167">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="bb65e-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb65e-168">OUTPUTS</span></span>

### <span data-ttu-id="bb65e-169">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="bb65e-169">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="bb65e-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb65e-170">NOTES</span></span>

## <span data-ttu-id="bb65e-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb65e-171">RELATED LINKS</span></span>

[<span data-ttu-id="bb65e-172">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="bb65e-172">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>](./Get-AzureRmRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="bb65e-173">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="bb65e-173">Stop-AzureRmRecoveryServicesBackupJob</span></span>](./Stop-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="bb65e-174">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="bb65e-174">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


