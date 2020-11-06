---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 63d90aa5f98f6710702a70e9609c7625626e34c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594195"
---
# <span data-ttu-id="f1237-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f1237-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="f1237-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1237-102">SYNOPSIS</span></span>
<span data-ttu-id="f1237-103">Çalışan işi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="f1237-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1237-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1237-104">SYNTAX</span></span>

### <span data-ttu-id="f1237-105">JobFilterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1237-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f1237-106">Idfilterset</span><span class="sxs-lookup"><span data-stu-id="f1237-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1237-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1237-107">DESCRIPTION</span></span>
<span data-ttu-id="f1237-108">**Stop-AzureRmRecoveryServicesBackupJob** cmdlet 'i mevcut bir Azure yedekleme işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="f1237-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="f1237-109">Çok uzun süren ve diğer etkinlikleri engelleyen bir işi durdurmak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1237-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="f1237-110">Yalnızca yedekleme ve geri yükleme işi türlerini iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1237-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="f1237-111">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f1237-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f1237-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1237-112">EXAMPLES</span></span>

### <span data-ttu-id="f1237-113">Örnek 1: yedekleme işini durdurma</span><span class="sxs-lookup"><span data-stu-id="f1237-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="f1237-114">İlk komut bir yedekleme işi alır ve işi $Job değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f1237-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="f1237-115">Son komut $Job uygulamasında yedekleme işinin örnek KIMLIĞINI belirterek işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="f1237-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="f1237-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1237-116">PARAMETERS</span></span>

### <span data-ttu-id="f1237-117">-Job</span><span class="sxs-lookup"><span data-stu-id="f1237-117">-Job</span></span>
<span data-ttu-id="f1237-118">Bu cmdlet 'in iptal olduğu bir iş belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1237-118">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="f1237-119">**Backupjob** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1237-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="f1237-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="f1237-120">-JobId</span></span>
<span data-ttu-id="f1237-121">İptal edilecek işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1237-121">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="f1237-122">ID, **Backupjob** nesnesinin InstanceId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="f1237-122">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="f1237-123">**Backupjob** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupJob seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f1237-123">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="f1237-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1237-124">-DefaultProfile</span></span>
<span data-ttu-id="f1237-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1237-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1237-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1237-126">CommonParameters</span></span>
<span data-ttu-id="f1237-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1237-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1237-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1237-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1237-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1237-129">INPUTS</span></span>

## <span data-ttu-id="f1237-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1237-130">OUTPUTS</span></span>

### <span data-ttu-id="f1237-131">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="f1237-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f1237-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1237-132">NOTES</span></span>

## <span data-ttu-id="f1237-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1237-133">RELATED LINKS</span></span>

[<span data-ttu-id="f1237-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f1237-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="f1237-135">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f1237-135">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


