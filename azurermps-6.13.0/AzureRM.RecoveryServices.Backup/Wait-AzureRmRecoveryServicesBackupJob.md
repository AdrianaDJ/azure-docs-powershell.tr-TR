---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 377250dcc8cbeb3727e7d2bf3f0dd0a8581d6401
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591926"
---
# <span data-ttu-id="6489f-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6489f-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="6489f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6489f-102">SYNOPSIS</span></span>
<span data-ttu-id="6489f-103">Yedekleme işinin bitmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="6489f-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6489f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6489f-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6489f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6489f-105">DESCRIPTION</span></span>
<span data-ttu-id="6489f-106">**Wait-AzureRmRecoveryServicesBackupJob** cmdlet 'ı bir Azure yedekleme işinin bitmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="6489f-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="6489f-107">Yedekleme işleri uzun zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="6489f-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="6489f-108">Bir yedekleme işini bir komut dosyasının parçası olarak çalıştırırsanız, diğer görevlere devam etmeden önce bu komut dosyasının işin bitmesini beklemeye zorlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6489f-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="6489f-109">Bu cmdlet 'i içeren bir komut dosyası, iş durumu için yedekleme hizmetini yoklayıp birden kolay olabilir.</span><span class="sxs-lookup"><span data-stu-id="6489f-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="6489f-110">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6489f-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6489f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6489f-111">EXAMPLES</span></span>

### <span data-ttu-id="6489f-112">Örnek 1: işin bitmesini bekle</span><span class="sxs-lookup"><span data-stu-id="6489f-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="6489f-113">Bu komut dosyası, iş tamamlanana kadar devam eden ilk işi yoklar.</span><span class="sxs-lookup"><span data-stu-id="6489f-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="6489f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6489f-114">PARAMETERS</span></span>

### <span data-ttu-id="6489f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6489f-115">-DefaultProfile</span></span>
<span data-ttu-id="6489f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6489f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6489f-117">-Job</span><span class="sxs-lookup"><span data-stu-id="6489f-117">-Job</span></span>
<span data-ttu-id="6489f-118">Bekleme işini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6489f-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="6489f-119">**Backupjob** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6489f-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6489f-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="6489f-120">-Timeout</span></span>
<span data-ttu-id="6489f-121">Bu cmdlet işin bitmesini beklediği en uzun süreyi saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="6489f-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="6489f-122">Zaman aşımı değeri belirtmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="6489f-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6489f-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6489f-123">-VaultId</span></span>
<span data-ttu-id="6489f-124">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6489f-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6489f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6489f-125">CommonParameters</span></span>
<span data-ttu-id="6489f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6489f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6489f-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6489f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6489f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6489f-128">INPUTS</span></span>

### <span data-ttu-id="6489f-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="6489f-129">System.Object</span></span>
<span data-ttu-id="6489f-130">Parametreler: Iş (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6489f-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="6489f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6489f-131">System.String</span></span>
<span data-ttu-id="6489f-132">Parametreler: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6489f-132">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="6489f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6489f-133">OUTPUTS</span></span>

### <span data-ttu-id="6489f-134">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="6489f-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6489f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6489f-135">NOTES</span></span>

## <span data-ttu-id="6489f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6489f-136">RELATED LINKS</span></span>

[<span data-ttu-id="6489f-137">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6489f-137">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


