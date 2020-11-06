---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: cbdb60fb4ec139b1dae92b7dd8e2e54675ae1f90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589593"
---
# <span data-ttu-id="64db9-101">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="64db9-101">Get-AzureRmBackupJob</span></span>

## <span data-ttu-id="64db9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64db9-102">SYNOPSIS</span></span>
<span data-ttu-id="64db9-103">Yedekleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="64db9-103">Gets Backup jobs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64db9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64db9-104">SYNTAX</span></span>

### <span data-ttu-id="64db9-105">FiltersSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="64db9-105">FiltersSet (Default)</span></span>
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64db9-106">JobsListFilter</span><span class="sxs-lookup"><span data-stu-id="64db9-106">JobsListFilter</span></span>
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64db9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="64db9-107">DESCRIPTION</span></span>
<span data-ttu-id="64db9-108">**Get-AzureRmBackupJob** cmdlet 'i, belirli bir kasa Için Azure yedekleme işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="64db9-108">The **Get-AzureRmBackupJob** cmdlet gets Azure Backup jobs for a specific vault.</span></span>

## <span data-ttu-id="64db9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64db9-109">EXAMPLES</span></span>

### <span data-ttu-id="64db9-110">Örnek 1: yedekleme kasasındaki tüm işleri alma</span><span class="sxs-lookup"><span data-stu-id="64db9-110">Example 1: Get all jobs in a Backup vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="64db9-111">İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="64db9-111">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="64db9-112">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="64db9-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="64db9-113">İkinci komut $Vault kasa için tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="64db9-113">The second command gets all the jobs for the vault in $Vault.</span></span>

### <span data-ttu-id="64db9-114">Örnek 2: tamamlanan işleri alma</span><span class="sxs-lookup"><span data-stu-id="64db9-114">Example 2: Get completed jobs</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

<span data-ttu-id="64db9-115">Bu komut $Vault iş kasasından tamamlanmış işleri alır.</span><span class="sxs-lookup"><span data-stu-id="64db9-115">This command gets completed jobs from the vault in $Vault.</span></span>

### <span data-ttu-id="64db9-116">Örnek 3: geçen hafta başarısız iş alma</span><span class="sxs-lookup"><span data-stu-id="64db9-116">Example 3: Get failed jobs for the last week</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

<span data-ttu-id="64db9-117">Bu komut, $Vault 'daki kasadan geçen haftaki başarısız işleri alır.</span><span class="sxs-lookup"><span data-stu-id="64db9-117">This command gets failed jobs from the last week from the vault in $Vault.</span></span>
<span data-ttu-id="64db9-118">*From* parametresi geçmişte yedi gün bir saat belirtir.</span><span class="sxs-lookup"><span data-stu-id="64db9-118">The *From* parameter specifies a time seven days in the past.</span></span>
<span data-ttu-id="64db9-119">Komut *to* parametresi için bir değer belirtmiyor.</span><span class="sxs-lookup"><span data-stu-id="64db9-119">The command does not specify a value for the *To* parameter.</span></span>
<span data-ttu-id="64db9-120">Bu nedenle, geçerli zamanın varsayılan değerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="64db9-120">Therefore, it uses the default value of the current time.</span></span>

### <span data-ttu-id="64db9-121">Örnek 4: süren devam eden iş için yedekleme yoklama</span><span class="sxs-lookup"><span data-stu-id="64db9-121">Example 4: Poll Backup for an in progress job that finishes</span></span>
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

<span data-ttu-id="64db9-122">Bu komut dosyası, iş tamamlanana kadar devam eden ilk işi yoklar.</span><span class="sxs-lookup"><span data-stu-id="64db9-122">This script polls the first job that is currently in progress until the job has completed.</span></span>
<span data-ttu-id="64db9-123">Komut dosyasının ilk satırı, sürmekte olan $Vault tüm işleri alır ve bu işleri $Jobs dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="64db9-123">The first line of the script gets all the jobs in $Vault that are in progress, and then stores those jobs in the $Jobs array variable.</span></span>
<span data-ttu-id="64db9-124">İkinci satır, $Job değişkeninde $Jobs dizisinden ilk işi depolar.</span><span class="sxs-lookup"><span data-stu-id="64db9-124">The second line stores the first job from the $Jobs array in the $Job variable.</span></span>
<span data-ttu-id="64db9-125">Üçüncü satır, iş tamamlanana kadar işin geçerli durumunu denetleyen **while** döngüsünü başlatır.</span><span class="sxs-lookup"><span data-stu-id="64db9-125">The third line starts a **while** loop that checks the current status of the job until the job is completed.</span></span>
<span data-ttu-id="64db9-126">Eğer **anahtar sözcüğü** hakkında bilgi için şunu yazın `Get-Help about_While` .</span><span class="sxs-lookup"><span data-stu-id="64db9-126">For information about the **while** keyword, type `Get-Help about_While`.</span></span>
<span data-ttu-id="64db9-127">**While** döngüsü konsola bir ileti yazar, on $Job saniye boyunca uyku</span><span class="sxs-lookup"><span data-stu-id="64db9-127">The **while** loop writes a message to the console, sleeps for ten seconds, and then updates the $Job variable.</span></span>
<span data-ttu-id="64db9-128">Komut dosyası, işin mevcut durumunu almak için mevcut $Job değerini ve geçerli cmdlet 'i kullanarak $Job değişkenini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="64db9-128">The script updates the $Job variable by using existing value of $Job and the current cmdlet to get the current status of the job.</span></span>
<span data-ttu-id="64db9-129">Windows PowerShell cmdlet 'leri hakkında bilgi için, `Get-Help Write-Host` ve yazın `Get-Help Start-Sleep` .</span><span class="sxs-lookup"><span data-stu-id="64db9-129">For information about the Windows PowerShell cmdlets, type `Get-Help Write-Host` and `Get-Help Start-Sleep`.</span></span>
<span data-ttu-id="64db9-130">Komut dosyasının son satırında, komut dosyasının bittiğini söyler.</span><span class="sxs-lookup"><span data-stu-id="64db9-130">The final line of the script tells you that the script has finished.</span></span>

## <span data-ttu-id="64db9-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64db9-131">PARAMETERS</span></span>

### <span data-ttu-id="64db9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64db9-132">-DefaultProfile</span></span>
<span data-ttu-id="64db9-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="64db9-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64db9-134">'Den</span><span class="sxs-lookup"><span data-stu-id="64db9-134">-From</span></span>
<span data-ttu-id="64db9-135">Bu cmdlet 'in aldığı işler için zaman aralığının başlangıç, **DateTime** nesnesi olarak başlangıcını belirtir.</span><span class="sxs-lookup"><span data-stu-id="64db9-135">Specifies the start, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="64db9-136">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="64db9-136">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="64db9-137">**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="64db9-137">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db9-138">-Job</span><span class="sxs-lookup"><span data-stu-id="64db9-138">-Job</span></span>
<span data-ttu-id="64db9-139">Bu cmdlet 'in aldığı işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="64db9-139">Specifies a job that this cmdlet gets.</span></span>
<span data-ttu-id="64db9-140">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="64db9-140">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db9-141">-JobId</span><span class="sxs-lookup"><span data-stu-id="64db9-141">-JobId</span></span>
<span data-ttu-id="64db9-142">Bu cmdlet 'in aldığı bir işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="64db9-142">Specifies the ID of a job that this cmdlet gets.</span></span>
<span data-ttu-id="64db9-143">ID, **Azurermbackupjob** nesnesinin **InstanceId** özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="64db9-143">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="64db9-144">**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="64db9-144">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db9-145">-İşlem</span><span class="sxs-lookup"><span data-stu-id="64db9-145">-Operation</span></span>
<span data-ttu-id="64db9-146">Bu cmdlet 'in aldığı işlerin bir işlemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="64db9-146">Specifies an operation of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="64db9-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="64db9-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64db9-148">Yedeğinin</span><span class="sxs-lookup"><span data-stu-id="64db9-148">Backup</span></span> 
- <span data-ttu-id="64db9-149">ConfigureBackup</span><span class="sxs-lookup"><span data-stu-id="64db9-149">ConfigureBackup</span></span> 
- <span data-ttu-id="64db9-150">DeleteBackupData</span><span class="sxs-lookup"><span data-stu-id="64db9-150">DeleteBackupData</span></span> 
- <span data-ttu-id="64db9-151">Kaydettiremedi</span><span class="sxs-lookup"><span data-stu-id="64db9-151">Register</span></span> 
- <span data-ttu-id="64db9-152">Kurtarma</span><span class="sxs-lookup"><span data-stu-id="64db9-152">Restore</span></span> 
- <span data-ttu-id="64db9-153">Sayfa korumasını kaldır</span><span class="sxs-lookup"><span data-stu-id="64db9-153">UnProtect</span></span> 
- <span data-ttu-id="64db9-154">Kaldırabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="64db9-154">Unregister</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db9-155">-Durum</span><span class="sxs-lookup"><span data-stu-id="64db9-155">-Status</span></span>
<span data-ttu-id="64db9-156">Bu cmdlet 'in aldığı işlerin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="64db9-156">Specifies a status of the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="64db9-157">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="64db9-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="64db9-158">Progress</span><span class="sxs-lookup"><span data-stu-id="64db9-158">InProgress</span></span>
- <span data-ttu-id="64db9-159">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="64db9-159">Failed</span></span>
- <span data-ttu-id="64db9-160">İptal</span><span class="sxs-lookup"><span data-stu-id="64db9-160">Cancelled</span></span>
- <span data-ttu-id="64db9-161">Edilirse</span><span class="sxs-lookup"><span data-stu-id="64db9-161">Cancelling</span></span>
- <span data-ttu-id="64db9-162">Tamamladığı</span><span class="sxs-lookup"><span data-stu-id="64db9-162">Completed</span></span>
- <span data-ttu-id="64db9-163">Completedwithuyarılar tüm sürmekte olan işleri veya tüm başarısız işleri bulmak için bu parametreyi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="64db9-163">CompletedWithWarnings You can specify this parameter to find all in progress jobs or all failed jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db9-164">-To</span><span class="sxs-lookup"><span data-stu-id="64db9-164">-To</span></span>
<span data-ttu-id="64db9-165">Bu cmdlet 'in aldığı işler için zaman aralığının sonunu bir **Tarih saat** olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="64db9-165">Specifies the end, as a **DateTime** object, of a time range for the jobs that this cmdlet gets.</span></span>
<span data-ttu-id="64db9-166">Varsayılan değer geçerli sistem saatinin değeridir.</span><span class="sxs-lookup"><span data-stu-id="64db9-166">The default value is the current system time.</span></span>
<span data-ttu-id="64db9-167">Bu parametreyi belirtirseniz, *from* parametresini de belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="64db9-167">If you specify this parameter, you must also specify the *From* parameter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db9-168">-Tür</span><span class="sxs-lookup"><span data-stu-id="64db9-168">-Type</span></span>
<span data-ttu-id="64db9-169">Bu cmdlet 'in yedekleme işlerini aldığı kapsayıcının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="64db9-169">Specifies the type of container for which this cmdlet gets backup jobs.</span></span>
<span data-ttu-id="64db9-170">Şu anda desteklenen tek değer AzureVM.</span><span class="sxs-lookup"><span data-stu-id="64db9-170">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64db9-171">-Kasa</span><span class="sxs-lookup"><span data-stu-id="64db9-171">-Vault</span></span>
<span data-ttu-id="64db9-172">Bu cmdlet 'in işleri aldığı yedek kasayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="64db9-172">Specifies the Backup vault for which this cmdlet gets jobs.</span></span>
<span data-ttu-id="64db9-173">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="64db9-173">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64db9-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64db9-174">CommonParameters</span></span>
<span data-ttu-id="64db9-175">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64db9-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64db9-176">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64db9-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64db9-177">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64db9-177">INPUTS</span></span>

### <span data-ttu-id="64db9-178">Microsoft. Azure. Commands. AzureBackup. modeller. Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="64db9-178">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="64db9-179">Parametreler: kasa (ByValue)</span><span class="sxs-lookup"><span data-stu-id="64db9-179">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="64db9-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64db9-180">OUTPUTS</span></span>

### <span data-ttu-id="64db9-181">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="64db9-181">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="64db9-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64db9-182">NOTES</span></span>
* <span data-ttu-id="64db9-183">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="64db9-183">None</span></span>

## <span data-ttu-id="64db9-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64db9-184">RELATED LINKS</span></span>

[<span data-ttu-id="64db9-185">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="64db9-185">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="64db9-186">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="64db9-186">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)

[<span data-ttu-id="64db9-187">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="64db9-187">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


