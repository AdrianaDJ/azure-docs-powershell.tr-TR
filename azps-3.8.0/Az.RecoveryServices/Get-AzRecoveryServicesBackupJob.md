---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 4d5ec07e7a068e1ab96f485ee67db0c1dd43f388
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096366"
---
# <span data-ttu-id="8f33c-101">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8f33c-101">Get-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="8f33c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f33c-102">SYNOPSIS</span></span>

<span data-ttu-id="8f33c-103">Yedekleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8f33c-103">Gets Backup jobs.</span></span>

## <span data-ttu-id="8f33c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f33c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f33c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f33c-105">DESCRIPTION</span></span>

<span data-ttu-id="8f33c-106">**Get-AzRecoveryServicesBackupJob** cmdlet 'i, belirli bir kasa Için Azure yedekleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8f33c-106">The **Get-AzRecoveryServicesBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>
<span data-ttu-id="8f33c-107">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8f33c-107">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="8f33c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f33c-108">EXAMPLES</span></span>

### <span data-ttu-id="8f33c-109">Örnek 1: devam eden tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="8f33c-109">Example 1: Get all in-progress jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

<span data-ttu-id="8f33c-110">İlk komut, sürmekte olan işlerin durumunu dizi olarak alır ve $Joblist değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8f33c-110">The first command gets status of an in-progress jobs as an array, and then stores it in the $Joblist variable.</span></span>
<span data-ttu-id="8f33c-111">İkinci komut $Joblist dizisindeki ilk öğeyi görüntüler.</span><span class="sxs-lookup"><span data-stu-id="8f33c-111">The second command displays the first item in the $Joblist array.</span></span>

### <span data-ttu-id="8f33c-112">Örnek 2: son 7 gündeki tüm başarısız işleri alma</span><span class="sxs-lookup"><span data-stu-id="8f33c-112">Example 2: Get all failed jobs in the last 7 days</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

<span data-ttu-id="8f33c-113">Bu komut, kasadaki geçen haftanın başarısız işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="8f33c-113">This command gets failed jobs from the last week in the vault.</span></span>
<span data-ttu-id="8f33c-114">*From* parametresi, geçmişte UTC 'de belirtilen saat yedi gün içinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-114">The *From* parameter specifies a time seven days in the past specified in UTC.</span></span>
<span data-ttu-id="8f33c-115">Komut *to* parametresi için bir değer belirtmiyor.</span><span class="sxs-lookup"><span data-stu-id="8f33c-115">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="8f33c-116">Bu nedenle, geçerli zamanın varsayılan değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8f33c-116">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="8f33c-117">Örnek 3: devam eden bir iş edinme ve tamamlanma işlemini bekleme</span><span class="sxs-lookup"><span data-stu-id="8f33c-117">Example 3: Get an in-progress job and wait for completion</span></span>

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="8f33c-118">Bu komut dosyası, iş tamamlanana kadar devam eden ilk işi yoklar.</span><span class="sxs-lookup"><span data-stu-id="8f33c-118">This script polls the first job that is currently in progress until the job has completed.</span></span>

<span data-ttu-id="8f33c-119">Not: **wait-AzRecoveryServicesBackupJob** cmdlet 'ini kullanarak bir Azure yedekleme işinin bitmesini bekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8f33c-119">Note: You can use **Wait-AzRecoveryServicesBackupJob** cmdlet to wait for an Azure Backup job to finish instead of While loop.</span></span>

## <span data-ttu-id="8f33c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f33c-120">PARAMETERS</span></span>

### <span data-ttu-id="8f33c-121">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="8f33c-121">-BackupManagementType</span></span>

<span data-ttu-id="8f33c-122">Yedekleme yönetim türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-122">Specifies the Backup management type.</span></span>
<span data-ttu-id="8f33c-123">Şu anda, yalnızca AzureVM, AzureStorage destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="8f33c-123">Currently, only AzureVM, AzureStorage is supported.</span></span>

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

### <span data-ttu-id="8f33c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f33c-124">-DefaultProfile</span></span>

<span data-ttu-id="8f33c-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f33c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f33c-126">'Den</span><span class="sxs-lookup"><span data-stu-id="8f33c-126">-From</span></span>

<span data-ttu-id="8f33c-127">Bu cmdlet 'in aldığı işler için zaman aralığının başlangıç, **DateTime** nesnesi olarak başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-127">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8f33c-128">**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8f33c-128">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="8f33c-129">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8f33c-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="8f33c-130">Tarihler için UTC biçimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8f33c-130">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="8f33c-131">-Job</span><span class="sxs-lookup"><span data-stu-id="8f33c-131">-Job</span></span>

<span data-ttu-id="8f33c-132">Alınacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-132">Specifies the job to get.</span></span>

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

### <span data-ttu-id="8f33c-133">-JobId</span><span class="sxs-lookup"><span data-stu-id="8f33c-133">-JobId</span></span>

<span data-ttu-id="8f33c-134">Bu cmdlet 'in aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-134">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="8f33c-135">ID, **Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase** nesnesinin JobId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-135">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="8f33c-136">-İşlem</span><span class="sxs-lookup"><span data-stu-id="8f33c-136">-Operation</span></span>

<span data-ttu-id="8f33c-137">Bu cmdlet 'in aldığı işlerin bir işlemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-137">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8f33c-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8f33c-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f33c-139">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="8f33c-139">Backup</span></span>
- <span data-ttu-id="8f33c-140">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="8f33c-140">ConfigureBackup</span></span>
- <span data-ttu-id="8f33c-141">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="8f33c-141">DeleteBackupData</span></span>
- <span data-ttu-id="8f33c-142">DisableBackup</span><span class="sxs-lookup"><span data-stu-id="8f33c-142">DisableBackup</span></span>
- <span data-ttu-id="8f33c-143">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="8f33c-143">Restore</span></span>

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

### <span data-ttu-id="8f33c-144">-Durum</span><span class="sxs-lookup"><span data-stu-id="8f33c-144">-Status</span></span>

<span data-ttu-id="8f33c-145">Bu cmdlet 'in aldığı işlerin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-145">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8f33c-146">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8f33c-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8f33c-147">Progress</span><span class="sxs-lookup"><span data-stu-id="8f33c-147">InProgress</span></span>
- <span data-ttu-id="8f33c-148">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="8f33c-148">Failed</span></span>
- <span data-ttu-id="8f33c-149">İptal</span><span class="sxs-lookup"><span data-stu-id="8f33c-149">Cancelled</span></span>
- <span data-ttu-id="8f33c-150">Edilirse</span><span class="sxs-lookup"><span data-stu-id="8f33c-150">Cancelling</span></span>
- <span data-ttu-id="8f33c-151">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="8f33c-151">Completed</span></span>
- <span data-ttu-id="8f33c-152">Completeduyarıları</span><span class="sxs-lookup"><span data-stu-id="8f33c-152">CompletedWithWarnings</span></span>

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

### <span data-ttu-id="8f33c-153">-To</span><span class="sxs-lookup"><span data-stu-id="8f33c-153">-To</span></span>

<span data-ttu-id="8f33c-154">Bu cmdlet 'in aldığı işler için zaman aralığının sonunu bir **Tarih saat** olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-154">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="8f33c-155">Varsayılan değer geçerli sistem saatinin değeridir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-155">The default value is the current system time.</span></span>
<span data-ttu-id="8f33c-156">Bu parametreyi belirtirseniz, **-from** parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8f33c-156">If you specify this parameter, you must also specify the **-From** parameter.</span></span>
<span data-ttu-id="8f33c-157">Tarihler için UTC biçimini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8f33c-157">Use UTC format for dates.</span></span>

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

### <span data-ttu-id="8f33c-158">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8f33c-158">-VaultId</span></span>

<span data-ttu-id="8f33c-159">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8f33c-159">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8f33c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f33c-160">CommonParameters</span></span>
<span data-ttu-id="8f33c-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f33c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f33c-162">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8f33c-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f33c-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f33c-163">INPUTS</span></span>

### <span data-ttu-id="8f33c-164">System. String</span><span class="sxs-lookup"><span data-stu-id="8f33c-164">System.String</span></span>

## <span data-ttu-id="8f33c-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f33c-165">OUTPUTS</span></span>

### <span data-ttu-id="8f33c-166">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="8f33c-166">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="8f33c-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f33c-167">NOTES</span></span>

## <span data-ttu-id="8f33c-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f33c-168">RELATED LINKS</span></span>

[<span data-ttu-id="8f33c-169">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="8f33c-169">Get-AzRecoveryServicesBackupJobDetail</span></span>](./Get-AzRecoveryServicesBackupJobDetail.md)

[<span data-ttu-id="8f33c-170">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8f33c-170">Stop-AzRecoveryServicesBackupJob</span></span>](./Stop-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="8f33c-171">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="8f33c-171">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)
