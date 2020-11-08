---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277554"
---
# <span data-ttu-id="a224e-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="a224e-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="a224e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a224e-102">SYNOPSIS</span></span>

<span data-ttu-id="a224e-103">Yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="a224e-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="a224e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a224e-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a224e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a224e-105">DESCRIPTION</span></span>

<span data-ttu-id="a224e-106">**Backup-Azrecoveryservicesbackupıtem** cmdlet 'i, korumalı Azure yedekleme öğesinin geçici yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="a224e-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="a224e-107">Bu cmdlet 'i kullanarak, korumayı etkinleştirdikten veya zamanlanmış yedekleme başarısız olursa hemen bir yedekleme başlattıktan sonra bir ilk yedekleme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a224e-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="a224e-108">Bu cmdlet, son kullanma tarihi olan veya olmayan özel bekletme için de kullanılabilir-daha fazla ayrıntı için parametre yardım metnine bakın.</span><span class="sxs-lookup"><span data-stu-id="a224e-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="a224e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a224e-109">EXAMPLES</span></span>

### <span data-ttu-id="a224e-110">Örnek 1: yedekleme öğesi için yedekleme başlatma</span><span class="sxs-lookup"><span data-stu-id="a224e-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="a224e-111">İlk komut, AzureVM türünün pstestv2vm1 adındaki yedekleme kapsayıcısını alır ve $NamedContainer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a224e-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="a224e-112">İkinci komut $NamedContainer kapsayıcısına karşılık gelen yedekleme öğesini alır ve $Item değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a224e-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="a224e-113">Son komut $Item içindeki yedekleme öğesi için yedekleme işini tetikler.</span><span class="sxs-lookup"><span data-stu-id="a224e-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="a224e-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a224e-114">Example 2</span></span>

<span data-ttu-id="a224e-115">Yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="a224e-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="a224e-116">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="a224e-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="a224e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a224e-117">PARAMETERS</span></span>

### <span data-ttu-id="a224e-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="a224e-118">-BackupType</span></span>

<span data-ttu-id="a224e-119">Gerçekleştirilecek yedekleme türü</span><span class="sxs-lookup"><span data-stu-id="a224e-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="a224e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a224e-120">-DefaultProfile</span></span>

<span data-ttu-id="a224e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a224e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a224e-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="a224e-122">-EnableCompression</span></span>

<span data-ttu-id="a224e-123">Sıkıştırmayı etkinleştirme gerekirse</span><span class="sxs-lookup"><span data-stu-id="a224e-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="a224e-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="a224e-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="a224e-125">Hiçbir şey yoksa, varsayılan değer olan 30 gün boyunca, kurtarma noktası için bir tarih saat değeri olarak geçerlilik süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a224e-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="a224e-126">VM, SQL (yalnızca salt kopya-tam yedekleme türü için), AFS yedekleme öğeleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="a224e-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="a224e-127">-Öğe</span><span class="sxs-lookup"><span data-stu-id="a224e-127">-Item</span></span>

<span data-ttu-id="a224e-128">Bu cmdlet 'in yedekleme işlemini başlattığı yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a224e-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="a224e-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="a224e-129">-VaultId</span></span>

<span data-ttu-id="a224e-130">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a224e-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="a224e-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a224e-131">-Confirm</span></span>

<span data-ttu-id="a224e-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a224e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a224e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a224e-133">-WhatIf</span></span>

<span data-ttu-id="a224e-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a224e-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="a224e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a224e-135">CommonParameters</span></span>
<span data-ttu-id="a224e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a224e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a224e-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a224e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a224e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a224e-138">INPUTS</span></span>

### <span data-ttu-id="a224e-139">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase</span><span class="sxs-lookup"><span data-stu-id="a224e-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="a224e-140">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="a224e-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a224e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a224e-141">System.String</span></span>

## <span data-ttu-id="a224e-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a224e-142">OUTPUTS</span></span>

### <span data-ttu-id="a224e-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="a224e-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="a224e-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a224e-144">NOTES</span></span>

## <span data-ttu-id="a224e-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a224e-145">RELATED LINKS</span></span>

[<span data-ttu-id="a224e-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a224e-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="a224e-147">Get-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="a224e-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="a224e-148">Restore-Azrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="a224e-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
