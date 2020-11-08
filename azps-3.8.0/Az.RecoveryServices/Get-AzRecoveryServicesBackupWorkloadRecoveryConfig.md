---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6033421b9a78e7cb531d2a33eabba1e97010c4f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104720"
---
# <span data-ttu-id="15c0e-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="15c0e-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="15c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="15c0e-103">Bu komut SQL DB gibi yedeklenmiş bir öğenin kurtarma yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15c0e-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="15c0e-104">Yapılandırma nesnesi, SQL için hedef fiziksel yollar gibi geri yükleme ve uygulamaya özgü parametrelerin hedef hedefleri gibi tüm ayrıntıları depolar.</span><span class="sxs-lookup"><span data-stu-id="15c0e-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="15c0e-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15c0e-105">SYNTAX</span></span>

### <span data-ttu-id="15c0e-106">RpParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15c0e-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15c0e-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c0e-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15c0e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="15c0e-108">DESCRIPTION</span></span>
<span data-ttu-id="15c0e-109">Komut, restore cmdlet 'ine geçirilen AzureWorkload öğeleri için bir kurtarma yapılandırması döndürür.</span><span class="sxs-lookup"><span data-stu-id="15c0e-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="15c0e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15c0e-110">EXAMPLES</span></span>

### <span data-ttu-id="15c0e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="15c0e-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="15c0e-112">İlk cmdlet, kurtarma noktası nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="15c0e-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="15c0e-113">İkinci cmdlet, özgün konum geri yüklemesi için bir kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15c0e-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="15c0e-114">Üçüncü cmdlet, alternatif bir konum geri yüklemesi için kurtarma planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="15c0e-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="15c0e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15c0e-115">PARAMETERS</span></span>

### <span data-ttu-id="15c0e-116">-Alternateworkloadres</span><span class="sxs-lookup"><span data-stu-id="15c0e-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="15c0e-117">Kurtarma noktasında bulunan DB bilgileri için yedeklenen VERITABANı 'nun üzerine yazılmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15c0e-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="15c0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c0e-118">-DefaultProfile</span></span>
<span data-ttu-id="15c0e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15c0e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c0e-120">-DosyaYolu</span><span class="sxs-lookup"><span data-stu-id="15c0e-120">-FilePath</span></span>
<span data-ttu-id="15c0e-121">Geri yükleme için FilePath 'i belirtir.</span><span class="sxs-lookup"><span data-stu-id="15c0e-121">Specifies the filepath for restore operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c0e-122">-FromFull</span><span class="sxs-lookup"><span data-stu-id="15c0e-122">-FromFull</span></span>
<span data-ttu-id="15c0e-123">Günlük yedeklemelerinin uygulanacağı tam RecoveryPoint noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15c0e-123">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c0e-124">-Öğe</span><span class="sxs-lookup"><span data-stu-id="15c0e-124">-Item</span></span>
<span data-ttu-id="15c0e-125">Geri yükleme işleminin gerçekleştirildiği yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15c0e-125">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="15c0e-126">-Originalworkloadres</span><span class="sxs-lookup"><span data-stu-id="15c0e-126">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="15c0e-127">Kurtarma noktasında bulunan DB bilgileri için yedeklenen VERITABANı 'nun üzerine yazılmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15c0e-127">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="15c0e-128">-Pointıntime</span><span class="sxs-lookup"><span data-stu-id="15c0e-128">-PointInTime</span></span>
<span data-ttu-id="15c0e-129">Kurtarma noktasının getirilmesi gereken zaman aralığının bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="15c0e-129">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="15c0e-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="15c0e-130">-RecoveryPoint</span></span>
<span data-ttu-id="15c0e-131">Geri yüklenecek kurtarma noktası nesnesi</span><span class="sxs-lookup"><span data-stu-id="15c0e-131">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="15c0e-132">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="15c0e-132">-RestoreAsFiles</span></span>
<span data-ttu-id="15c0e-133">Veritabanında dosya olarak veritabanını geri yüklemeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="15c0e-133">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="15c0e-134">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="15c0e-134">-TargetContainer</span></span>
<span data-ttu-id="15c0e-135">DB dosyalarının geri yüklenmesi gereken hedef makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="15c0e-135">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c0e-136">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="15c0e-136">-TargetItem</span></span>
<span data-ttu-id="15c0e-137">DB 'nin geri yüklenmesi gereken hedefi belirtir.</span><span class="sxs-lookup"><span data-stu-id="15c0e-137">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="15c0e-138">SQL geri yüklemeler için, yalnızca korunabilir öğe türü SQLInstance olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="15c0e-138">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="15c0e-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="15c0e-139">-VaultId</span></span>
<span data-ttu-id="15c0e-140">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="15c0e-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="15c0e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c0e-141">CommonParameters</span></span>
<span data-ttu-id="15c0e-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15c0e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c0e-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15c0e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c0e-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15c0e-144">INPUTS</span></span>

### <span data-ttu-id="15c0e-145">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="15c0e-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="15c0e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="15c0e-146">System.String</span></span>

## <span data-ttu-id="15c0e-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15c0e-147">OUTPUTS</span></span>

### <span data-ttu-id="15c0e-148">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="15c0e-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="15c0e-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15c0e-149">NOTES</span></span>

## <span data-ttu-id="15c0e-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15c0e-150">RELATED LINKS</span></span>
