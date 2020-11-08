---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098984"
---
# <span data-ttu-id="ced11-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ced11-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="ced11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ced11-102">SYNOPSIS</span></span>

<span data-ttu-id="ced11-103">Yedekleme işinin bitmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="ced11-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="ced11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ced11-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ced11-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ced11-105">DESCRIPTION</span></span>

<span data-ttu-id="ced11-106">**Wait-AzRecoveryServicesBackupJob** cmdlet 'ı bir Azure yedekleme işinin bitmesini bekler.</span><span class="sxs-lookup"><span data-stu-id="ced11-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="ced11-107">Yedekleme işleri uzun zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="ced11-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="ced11-108">Bir yedekleme işini bir komut dosyasının parçası olarak çalıştırırsanız, diğer görevlere devam etmeden önce bu komut dosyasının işin bitmesini beklemeye zorlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ced11-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="ced11-109">Bu cmdlet 'i içeren bir komut dosyası, iş durumu için yedekleme hizmetini yoklayıp birden kolay olabilir.</span><span class="sxs-lookup"><span data-stu-id="ced11-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="ced11-110">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ced11-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="ced11-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ced11-111">EXAMPLES</span></span>

### <span data-ttu-id="ced11-112">Örnek 1: işin bitmesini bekle</span><span class="sxs-lookup"><span data-stu-id="ced11-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="ced11-113">Bu komut dosyası, iş tamamlanana kadar devam eden ilk işi yoklar veya zaman aşımı süresi 1 saattir.</span><span class="sxs-lookup"><span data-stu-id="ced11-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="ced11-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ced11-114">PARAMETERS</span></span>

### <span data-ttu-id="ced11-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced11-115">-DefaultProfile</span></span>

<span data-ttu-id="ced11-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ced11-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ced11-117">-Job</span><span class="sxs-lookup"><span data-stu-id="ced11-117">-Job</span></span>

<span data-ttu-id="ced11-118">Bekleme işini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ced11-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="ced11-119">**Backupjob** nesnesi edinmek için **Get-AzRecoveryServicesBackupJob** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ced11-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="ced11-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="ced11-120">-Timeout</span></span>

<span data-ttu-id="ced11-121">Bu cmdlet işin bitmesini beklediği en uzun süreyi saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ced11-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="ced11-122">Zaman aşımı değeri belirtmeniz önerilir.</span><span class="sxs-lookup"><span data-stu-id="ced11-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="ced11-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ced11-123">-VaultId</span></span>

<span data-ttu-id="ced11-124">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ced11-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ced11-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced11-125">CommonParameters</span></span>
<span data-ttu-id="ced11-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ced11-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced11-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ced11-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced11-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ced11-128">INPUTS</span></span>

### <span data-ttu-id="ced11-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="ced11-129">System.Object</span></span>

### <span data-ttu-id="ced11-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ced11-130">System.String</span></span>

## <span data-ttu-id="ced11-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ced11-131">OUTPUTS</span></span>

### <span data-ttu-id="ced11-132">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="ced11-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ced11-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ced11-133">NOTES</span></span>

## <span data-ttu-id="ced11-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ced11-134">RELATED LINKS</span></span>

[<span data-ttu-id="ced11-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ced11-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
