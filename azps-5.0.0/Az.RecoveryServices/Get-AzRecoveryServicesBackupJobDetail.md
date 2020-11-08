---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276365"
---
# <span data-ttu-id="7c951-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="7c951-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="7c951-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c951-102">SYNOPSIS</span></span>

<span data-ttu-id="7c951-103">Yedekleme işinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="7c951-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="7c951-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c951-104">SYNTAX</span></span>

### <span data-ttu-id="7c951-105">JobFilterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7c951-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7c951-106">Idfilterset</span><span class="sxs-lookup"><span data-stu-id="7c951-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c951-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c951-107">DESCRIPTION</span></span>

<span data-ttu-id="7c951-108">**Get-AzRecoveryServicesBackupJobDetail** cmdlet 'i belirtilen Iş Için Azure yedekleme iş ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="7c951-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="7c951-109">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7c951-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="7c951-110">Uyarı: **Get-AzRecoveryServicesBackupJobDetails** diğer adı gelecekteki bir son değişiklik sürümünde kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="7c951-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="7c951-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c951-111">EXAMPLES</span></span>

### <span data-ttu-id="7c951-112">Örnek 1: başarısız işler için yedekleme işi ayrıntılarını alma</span><span class="sxs-lookup"><span data-stu-id="7c951-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="7c951-113">İlk komut ilgili kasayı getirir.</span><span class="sxs-lookup"><span data-stu-id="7c951-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="7c951-114">İkinci komut, kasadaki başarısız iş dizisini alır ve bunları $Jobs dizisinde depolar.</span><span class="sxs-lookup"><span data-stu-id="7c951-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="7c951-115">Üçüncü komut $Jobs 1 ' deki başarısız işin iş ayrıntılarını alır ve $JobDetails değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7c951-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="7c951-116">Son komutu başarısız olan işlerin hata ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="7c951-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="7c951-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c951-117">PARAMETERS</span></span>

### <span data-ttu-id="7c951-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c951-118">-DefaultProfile</span></span>

<span data-ttu-id="7c951-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c951-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c951-120">-Job</span><span class="sxs-lookup"><span data-stu-id="7c951-120">-Job</span></span>

<span data-ttu-id="7c951-121">Alınacak işi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c951-121">Specifies the job to get.</span></span>
<span data-ttu-id="7c951-122">**Backupjob** nesnesi edinmek için **Get-AzRecoveryServicesBackupJob** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7c951-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c951-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="7c951-123">-JobId</span></span>

<span data-ttu-id="7c951-124">Yedekleme işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c951-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="7c951-125">ID, **Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase** nesnesinin JobId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="7c951-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c951-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7c951-126">-VaultId</span></span>

<span data-ttu-id="7c951-127">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="7c951-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7c951-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c951-128">CommonParameters</span></span>
<span data-ttu-id="7c951-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c951-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c951-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7c951-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c951-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c951-131">INPUTS</span></span>

### <span data-ttu-id="7c951-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7c951-132">System.String</span></span>

## <span data-ttu-id="7c951-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c951-133">OUTPUTS</span></span>

### <span data-ttu-id="7c951-134">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="7c951-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="7c951-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c951-135">NOTES</span></span>

## <span data-ttu-id="7c951-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c951-136">RELATED LINKS</span></span>

[<span data-ttu-id="7c951-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="7c951-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
