---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 21498e13490b22b58621e2100dcc885442db7607
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759706"
---
# <span data-ttu-id="45999-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="45999-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="45999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45999-102">SYNOPSIS</span></span>
<span data-ttu-id="45999-103">Yedekleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="45999-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="45999-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45999-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45999-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45999-105">DESCRIPTION</span></span>
<span data-ttu-id="45999-106">**Get-AzRecoveryServicesBackupJob** cmdlet 'i, belirli bir kasa Için Azure yedekleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="45999-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="45999-107">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45999-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="45999-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45999-108">EXAMPLES</span></span>

### <span data-ttu-id="45999-109">Örnek 1: devam eden tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="45999-109">Example 1: Get all in-progress jobs</span></span>
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="45999-110">İlk komut bir ilerleme durumu işinin durumunu dizi olarak alır ve sonra bunu $Joblist değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="45999-110">The first command gets status of an in-progress job as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="45999-111">İkinci komut $Joblist dizisindeki ilk öğeyi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="45999-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="45999-112">Örnek 2: son 7 gündeki tüm başarısız işleri alma</span><span class="sxs-lookup"><span data-stu-id="45999-112">Example 2: Get all failed jobs in the last 7 days</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

<span data-ttu-id="45999-113">Bu komut, kasadaki geçen haftanın başarısız işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="45999-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="45999-114">*From* parametresi, geçmişte UTC 'de belirtilen saat yedi gün içinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="45999-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="45999-115">Komut *to* parametresi için bir değer belirtmiyor.</span><span class="sxs-lookup"><span data-stu-id="45999-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="45999-116">Bu nedenle, geçerli zamanın varsayılan değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="45999-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="45999-117">Örnek 3: devam eden bir iş edinme ve tamamlanma işlemini bekleme</span><span class="sxs-lookup"><span data-stu-id="45999-117">Example 3: Get an in-progress job and wait for completion</span></span>
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="45999-118">Bu komut dosyası, iş tamamlanana kadar devam eden ilk işi yoklar.</span><span class="sxs-lookup"><span data-stu-id="45999-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="45999-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45999-119">PARAMETERS</span></span>

### <span data-ttu-id="45999-120">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="45999-120">-BackupManagementType</span></span>
<span data-ttu-id="45999-121">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="45999-121">Specifies the Backup management type.</span></span>
<span data-ttu-id="45999-122">Şu anda, yalnızca AzureVM, AzureStorage destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="45999-122">Currently, only AzureVM, AzureStorage is supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45999-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45999-123">-DefaultProfile</span></span>
<span data-ttu-id="45999-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45999-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45999-125">'Den</span><span class="sxs-lookup"><span data-stu-id="45999-125">-From</span></span>
<span data-ttu-id="45999-126">Bu cmdlet 'in aldığı işler için zaman aralığının başlangıç, **DateTime** nesnesi olarak başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45999-126">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="45999-127">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="45999-127">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="45999-128">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="45999-128">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="45999-129">Tarihler için UTC biçimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="45999-129">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="45999-130">-Job</span><span class="sxs-lookup"><span data-stu-id="45999-130">-Job</span></span>
<span data-ttu-id="45999-131">Alınacak yedekleme işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="45999-131">Specifies the name of the Backup job to get.</span></span>

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

### <span data-ttu-id="45999-132">-JobId</span><span class="sxs-lookup"><span data-stu-id="45999-132">-JobId</span></span>
<span data-ttu-id="45999-133">Bu cmdlet 'in aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="45999-133">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="45999-134">ID, **Azurermrecoveryservicesbackupjob** nesnesinin InstanceId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="45999-134">The ID is the InstanceId property of an **AzureRmRecoveryServicesBackupJob** object.</span></span>
<span data-ttu-id="45999-135">**Azurermrecoveryservicesbackupjob** nesnesi almak için Get-azrecoveryservicesbackupjob öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="45999-135">To obtain an **AzureRmRecoveryServicesBackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="45999-136">-İşlem</span><span class="sxs-lookup"><span data-stu-id="45999-136">-Operation</span></span>
<span data-ttu-id="45999-137">Bu cmdlet 'in aldığı işlerin bir işlemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="45999-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="45999-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45999-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45999-139">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="45999-139">Backup</span></span>
- <span data-ttu-id="45999-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="45999-140">ConfigureBackup</span></span>
- <span data-ttu-id="45999-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="45999-141">DeleteBackupData</span></span>
- <span data-ttu-id="45999-142">Kaydettiremedi</span><span class="sxs-lookup"><span data-stu-id="45999-142">Register</span></span>
- <span data-ttu-id="45999-143">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="45999-143">Restore</span></span>
- <span data-ttu-id="45999-144">Sayfa korumasını kaldır</span><span class="sxs-lookup"><span data-stu-id="45999-144">UnProtect</span></span>
- <span data-ttu-id="45999-145">Kaldırabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="45999-145">Unregister</span></span>

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

### <span data-ttu-id="45999-146">-Durum</span><span class="sxs-lookup"><span data-stu-id="45999-146">-Status</span></span>
<span data-ttu-id="45999-147">Bu cmdlet 'in aldığı işlerin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="45999-147">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="45999-148">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="45999-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="45999-149">Progress</span><span class="sxs-lookup"><span data-stu-id="45999-149">InProgress</span></span>
- <span data-ttu-id="45999-150">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="45999-150">Failed</span></span>
- <span data-ttu-id="45999-151">İptal</span><span class="sxs-lookup"><span data-stu-id="45999-151">Cancelled</span></span>
- <span data-ttu-id="45999-152">Edilirse</span><span class="sxs-lookup"><span data-stu-id="45999-152">Cancelling</span></span>
- <span data-ttu-id="45999-153">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="45999-153">Completed</span></span>
- <span data-ttu-id="45999-154">Completeduyarıları</span><span class="sxs-lookup"><span data-stu-id="45999-154">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="45999-155">-To</span><span class="sxs-lookup"><span data-stu-id="45999-155">-To</span></span>
<span data-ttu-id="45999-156">Bu cmdlet 'in aldığı işler için zaman aralığının sonunu bir **Tarih saat** olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="45999-156">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="45999-157">Varsayılan değer geçerli sistem saatinin değeridir.</span><span class="sxs-lookup"><span data-stu-id="45999-157">The default value is the current system time.</span></span>
<span data-ttu-id="45999-158">Bu parametreyi belirtirseniz, *from* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="45999-158">If you specify this parameter, you must also specify the *From* parameter.</span></span>
<span data-ttu-id="45999-159">Tarihler için UTC biçimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="45999-159">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="45999-160">-VaultId</span><span class="sxs-lookup"><span data-stu-id="45999-160">-VaultId</span></span>
<span data-ttu-id="45999-161">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="45999-161">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="45999-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45999-162">CommonParameters</span></span>
<span data-ttu-id="45999-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45999-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45999-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45999-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45999-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45999-165">INPUTS</span></span>

### <span data-ttu-id="45999-166">System. String</span><span class="sxs-lookup"><span data-stu-id="45999-166">System.String</span></span>

## <span data-ttu-id="45999-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45999-167">OUTPUTS</span></span>

### <span data-ttu-id="45999-168">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="45999-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="45999-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45999-169">NOTES</span></span>

## <span data-ttu-id="45999-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45999-170">RELATED LINKS</span></span>

[<span data-ttu-id="45999-171">Get-AzRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="45999-171">Get-AzRecoveryServicesBackupJobDetails</span></span>](./Get-AzRecoveryServicesBackupJobDetails.md)

[<span data-ttu-id="45999-172">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="45999-172">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="45999-173">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="45999-173">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


