---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 6c8debac9091d28091695847b36d0cbc1b219125
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933067"
---
# <span data-ttu-id="0e406-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0e406-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="0e406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e406-102">SYNOPSIS</span></span>

<span data-ttu-id="0e406-103">Yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="0e406-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="0e406-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e406-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e406-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e406-105">DESCRIPTION</span></span>

<span data-ttu-id="0e406-106">**Backup-Azrecoveryservicesbackupıtem** cmdlet 'i, yedekleme zamanlamasına bağlı olmayan korumalı bir Azure yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="0e406-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="0e406-107">Zamanlanmış bir yedekleme başarısız olduktan sonra, korumayı etkinleştirdikten veya yedekleme başlattıktan sonra bir ilk yedekleme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e406-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="0e406-108">-VaultId parametresini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0e406-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="0e406-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e406-109">EXAMPLES</span></span>

### <span data-ttu-id="0e406-110">Örnek 1: yedekleme öğesi için yedekleme başlatma</span><span class="sxs-lookup"><span data-stu-id="0e406-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="0e406-111">İlk komut, AzureVM türünün pstestv2vm1 adındaki yedekleme kapsayıcısını alır ve $NamedContainer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0e406-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="0e406-112">İkinci komut $NamedContainer kapsayıcısına karşılık gelen yedekleme öğesini alır ve $Item değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0e406-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="0e406-113">Son komut $Item içindeki yedekleme öğesi için yedekleme işini tetikler.</span><span class="sxs-lookup"><span data-stu-id="0e406-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="0e406-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e406-114">PARAMETERS</span></span>

### <span data-ttu-id="0e406-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="0e406-115">-BackupType</span></span>

<span data-ttu-id="0e406-116">Gerçekleştirilecek yedekleme türü</span><span class="sxs-lookup"><span data-stu-id="0e406-116">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e406-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e406-117">-DefaultProfile</span></span>

<span data-ttu-id="0e406-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e406-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e406-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="0e406-119">-EnableCompression</span></span>

<span data-ttu-id="0e406-120">Sıkıştırmayı etkinleştirme gerekirse</span><span class="sxs-lookup"><span data-stu-id="0e406-120">If enabling compression is required</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e406-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="0e406-121">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="0e406-122">**Tarih saat** nesnesi olarak sona erme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e406-122">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e406-123">-Öğe</span><span class="sxs-lookup"><span data-stu-id="0e406-123">-Item</span></span>

<span data-ttu-id="0e406-124">Bu cmdlet 'in yedekleme işlemini başlattığı yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e406-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e406-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0e406-125">-VaultId</span></span>

<span data-ttu-id="0e406-126">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0e406-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0e406-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e406-127">-Confirm</span></span>

<span data-ttu-id="0e406-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e406-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e406-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e406-129">-WhatIf</span></span>

<span data-ttu-id="0e406-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e406-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e406-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e406-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e406-132">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e406-132">-CommonParameters</span></span>

<span data-ttu-id="0e406-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e406-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e406-134">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0e406-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e406-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e406-135">INPUTS</span></span>

### <span data-ttu-id="0e406-136">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="0e406-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="0e406-137">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="0e406-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0e406-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0e406-138">System.String</span></span>

## <span data-ttu-id="0e406-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e406-139">OUTPUTS</span></span>

### <span data-ttu-id="0e406-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="0e406-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0e406-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e406-141">NOTES</span></span>

## <span data-ttu-id="0e406-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e406-142">RELATED LINKS</span></span>

[<span data-ttu-id="0e406-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0e406-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="0e406-144">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="0e406-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="0e406-145">Restore-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="0e406-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
