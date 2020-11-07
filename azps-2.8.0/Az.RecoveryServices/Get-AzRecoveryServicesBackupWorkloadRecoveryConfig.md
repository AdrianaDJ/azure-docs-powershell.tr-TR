---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4a3ab7ca60807f294ee5739116c8b8bcc965ae2e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932990"
---
# <span data-ttu-id="8a6af-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="8a6af-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="8a6af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a6af-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6af-103">Bu komut SQL DB gibi yedeklenmiş bir öğenin kurtarma yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a6af-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="8a6af-104">Yapılandırma nesnesi, SQL için hedef fiziksel yollar gibi geri yükleme ve uygulamaya özgü parametrelerin hedef hedefleri gibi tüm ayrıntıları depolar.</span><span class="sxs-lookup"><span data-stu-id="8a6af-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="8a6af-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a6af-105">SYNTAX</span></span>

### <span data-ttu-id="8a6af-106">RpParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8a6af-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6af-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a6af-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a6af-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a6af-108">DESCRIPTION</span></span>
<span data-ttu-id="8a6af-109">Komut, restore cmdlet 'ine geçirilen AzureWorkload öğeleri için bir kurtarma yapılandırması döndürür.</span><span class="sxs-lookup"><span data-stu-id="8a6af-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="8a6af-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a6af-110">EXAMPLES</span></span>

### <span data-ttu-id="8a6af-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8a6af-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="8a6af-112">İlk cmdlet, kurtarma noktası nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8a6af-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="8a6af-113">İkinci cmdlet, özgün konum geri yüklemesi için bir kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a6af-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="8a6af-114">Üçüncü cmdlet, alternatif bir konum geri yüklemesi için kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8a6af-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="8a6af-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a6af-115">PARAMETERS</span></span>

### <span data-ttu-id="8a6af-116">-Alternateworkloadres</span><span class="sxs-lookup"><span data-stu-id="8a6af-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="8a6af-117">Kurtarma noktasında bulunan DB bilgileri için yedeklenen VERITABANı 'nun üzerine yazılmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a6af-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="8a6af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6af-118">-DefaultProfile</span></span>
<span data-ttu-id="8a6af-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a6af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a6af-120">-Öğe</span><span class="sxs-lookup"><span data-stu-id="8a6af-120">-Item</span></span>
<span data-ttu-id="8a6af-121">Geri yükleme işleminin gerçekleştirildiği yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a6af-121">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6af-122">-Originalworkloadres</span><span class="sxs-lookup"><span data-stu-id="8a6af-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="8a6af-123">Kurtarma noktasında bulunan DB bilgileri için yedeklenen VERITABANı 'nun üzerine yazılmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a6af-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="8a6af-124">-Pointıntime</span><span class="sxs-lookup"><span data-stu-id="8a6af-124">-PointInTime</span></span>
<span data-ttu-id="8a6af-125">Kurtarma noktasının getirilmesi gereken zaman aralığının bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="8a6af-125">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6af-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8a6af-126">-RecoveryPoint</span></span>
<span data-ttu-id="8a6af-127">Geri yüklenecek kurtarma noktası nesnesi</span><span class="sxs-lookup"><span data-stu-id="8a6af-127">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6af-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="8a6af-128">-TargetItem</span></span>
<span data-ttu-id="8a6af-129">DB 'nin geri yüklenmesi gereken hedefi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8a6af-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="8a6af-130">SQL geri yüklemeler için, yalnızca korunabilir öğe türü SQLInstance olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8a6af-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a6af-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8a6af-131">-VaultId</span></span>
<span data-ttu-id="8a6af-132">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8a6af-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8a6af-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a6af-133">-Confirm</span></span>
<span data-ttu-id="8a6af-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a6af-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a6af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a6af-135">-WhatIf</span></span>
<span data-ttu-id="8a6af-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a6af-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a6af-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a6af-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a6af-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6af-138">CommonParameters</span></span>
<span data-ttu-id="8a6af-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a6af-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6af-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a6af-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6af-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a6af-141">INPUTS</span></span>

### <span data-ttu-id="8a6af-142">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="8a6af-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="8a6af-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8a6af-143">System.String</span></span>

## <span data-ttu-id="8a6af-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a6af-144">OUTPUTS</span></span>

### <span data-ttu-id="8a6af-145">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="8a6af-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="8a6af-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a6af-146">NOTES</span></span>

## <span data-ttu-id="8a6af-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a6af-147">RELATED LINKS</span></span>