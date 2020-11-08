---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 6f8aa4220ec73f013ab5b1c797c0dacb5be7fde4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097091"
---
# <span data-ttu-id="71ddd-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="71ddd-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="71ddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="71ddd-103">Çalışan işi iptal eder.</span><span class="sxs-lookup"><span data-stu-id="71ddd-103">Cancels a running job.</span></span>

## <span data-ttu-id="71ddd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71ddd-104">SYNTAX</span></span>

### <span data-ttu-id="71ddd-105">JobFilterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="71ddd-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71ddd-106">Idfilterset</span><span class="sxs-lookup"><span data-stu-id="71ddd-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71ddd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="71ddd-107">DESCRIPTION</span></span>
<span data-ttu-id="71ddd-108">**Stop-AzRecoveryServicesBackupJob** cmdlet 'i mevcut bir Azure yedekleme işini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="71ddd-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="71ddd-109">Çok uzun süren ve diğer etkinlikleri engelleyen bir işi durdurmak için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="71ddd-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="71ddd-110">Yalnızca yedekleme ve geri yükleme işi türlerini iptal edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="71ddd-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="71ddd-111">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="71ddd-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="71ddd-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71ddd-112">EXAMPLES</span></span>

### <span data-ttu-id="71ddd-113">Örnek 1: yedekleme işini durdurma</span><span class="sxs-lookup"><span data-stu-id="71ddd-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="71ddd-114">İlk komut bir yedekleme işi alır ve işi $Job değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="71ddd-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="71ddd-115">Son komut $Job uygulamasında yedekleme işinin örnek KIMLIĞINI belirterek işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="71ddd-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="71ddd-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71ddd-116">PARAMETERS</span></span>

### <span data-ttu-id="71ddd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ddd-117">-DefaultProfile</span></span>
<span data-ttu-id="71ddd-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71ddd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71ddd-119">-Job</span><span class="sxs-lookup"><span data-stu-id="71ddd-119">-Job</span></span>
<span data-ttu-id="71ddd-120">Bu cmdlet 'in iptal olduğu bir iş belirtir.</span><span class="sxs-lookup"><span data-stu-id="71ddd-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="71ddd-121">**Backupjob** nesnesi edinmek için Get-AzRecoveryServicesBackupJob cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="71ddd-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="71ddd-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="71ddd-122">-JobId</span></span>
<span data-ttu-id="71ddd-123">İptal edilecek işin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="71ddd-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="71ddd-124">ID, **Backupjob** nesnesinin InstanceId özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="71ddd-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="71ddd-125">**Backupjob** nesnesi edinmek için Get-AzRecoveryServicesBackupJob öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="71ddd-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="71ddd-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="71ddd-126">-VaultId</span></span>
<span data-ttu-id="71ddd-127">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="71ddd-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="71ddd-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="71ddd-128">-Confirm</span></span>
<span data-ttu-id="71ddd-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="71ddd-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ddd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71ddd-130">-WhatIf</span></span>
<span data-ttu-id="71ddd-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="71ddd-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71ddd-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="71ddd-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ddd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ddd-133">CommonParameters</span></span>
<span data-ttu-id="71ddd-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71ddd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ddd-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="71ddd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ddd-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71ddd-136">INPUTS</span></span>

### <span data-ttu-id="71ddd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="71ddd-137">System.String</span></span>

## <span data-ttu-id="71ddd-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71ddd-138">OUTPUTS</span></span>

### <span data-ttu-id="71ddd-139">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="71ddd-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="71ddd-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71ddd-140">NOTES</span></span>

## <span data-ttu-id="71ddd-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71ddd-141">RELATED LINKS</span></span>

[<span data-ttu-id="71ddd-142">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="71ddd-142">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="71ddd-143">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="71ddd-143">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)

