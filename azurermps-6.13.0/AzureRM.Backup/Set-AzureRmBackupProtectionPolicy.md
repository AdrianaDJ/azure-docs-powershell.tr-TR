---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: caf6394ce84b18bd8e36b4504173fe7f7bb07fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588599"
---
# <span data-ttu-id="b3ce9-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3ce9-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="b3ce9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ce9-103">Var olan koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3ce9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3ce9-104">SYNTAX</span></span>

### <span data-ttu-id="b3ce9-105">NoScheduleParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3ce9-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3ce9-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="b3ce9-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3ce9-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="b3ce9-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3ce9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3ce9-108">DESCRIPTION</span></span>
<span data-ttu-id="b3ce9-109">**Set-AzureRmBackupProtectionPolicy** cmdlet 'ı Azure Backup 'ta var olan koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="b3ce9-110">Aşağıdaki koruma ilkesi bileşenlerini değiştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="b3ce9-110">You can modify the following protection policy components:</span></span> 
- <span data-ttu-id="b3ce9-111">Adlandır</span><span class="sxs-lookup"><span data-stu-id="b3ce9-111">Name</span></span>
- <span data-ttu-id="b3ce9-112">Yedekleme zamanlaması</span><span class="sxs-lookup"><span data-stu-id="b3ce9-112">Backup schedule</span></span>
- <span data-ttu-id="b3ce9-113">Bekletme ilkeleri herhangi bir değişiklik, ilkeyle ilişkili öğelerin yedekleme ve tutma etkilerini etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-113">Retention policies Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="b3ce9-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3ce9-114">EXAMPLES</span></span>

## <span data-ttu-id="b3ce9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3ce9-115">PARAMETERS</span></span>

### <span data-ttu-id="b3ce9-116">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="b3ce9-116">-BackupTime</span></span>
<span data-ttu-id="b3ce9-117">İlkenin yeni yedekleme saatini, bir **Tarih saat** nesnesi olarak ilke için belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-117">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="b3ce9-118">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-118">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="b3ce9-119">**TarihSaat** nesneleri hakkında bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b3ce9-119">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce9-120">-Günlük</span><span class="sxs-lookup"><span data-stu-id="b3ce9-120">-Daily</span></span>
<span data-ttu-id="b3ce9-121">Yedekleme işleminin günlük zamanlamada çalışacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-121">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce9-122">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="b3ce9-122">-DaysOfWeek</span></span>
<span data-ttu-id="b3ce9-123">Haftanın bir günü dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-123">Specifies an array of days of the week.</span></span>
<span data-ttu-id="b3ce9-124">Bu ilke, yedekleri bu parametre tarafından belirtilen günlerde çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-124">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="b3ce9-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b3ce9-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b3ce9-126">Den</span><span class="sxs-lookup"><span data-stu-id="b3ce9-126">Monday</span></span> 
- <span data-ttu-id="b3ce9-127">Salı</span><span class="sxs-lookup"><span data-stu-id="b3ce9-127">Tuesday</span></span> 
- <span data-ttu-id="b3ce9-128">Günü</span><span class="sxs-lookup"><span data-stu-id="b3ce9-128">Wednesday</span></span> 
- <span data-ttu-id="b3ce9-129">Per</span><span class="sxs-lookup"><span data-stu-id="b3ce9-129">Thursday</span></span> 
- <span data-ttu-id="b3ce9-130">Cuma</span><span class="sxs-lookup"><span data-stu-id="b3ce9-130">Friday</span></span> 
- <span data-ttu-id="b3ce9-131">Günü</span><span class="sxs-lookup"><span data-stu-id="b3ce9-131">Saturday</span></span> 
- <span data-ttu-id="b3ce9-132">Gününü</span><span class="sxs-lookup"><span data-stu-id="b3ce9-132">Sunday</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce9-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ce9-133">-DefaultProfile</span></span>
<span data-ttu-id="b3ce9-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3ce9-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3ce9-135">-NewName</span><span class="sxs-lookup"><span data-stu-id="b3ce9-135">-NewName</span></span>
<span data-ttu-id="b3ce9-136">İlkenin yeni adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-136">Specifies the new name for the policy.</span></span>
<span data-ttu-id="b3ce9-137">Bu ad kasada benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-137">This name must be unique in a vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce9-138">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3ce9-138">-ProtectionPolicy</span></span>
<span data-ttu-id="b3ce9-139">Bu cmdlet 'in değiştirdiği koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-139">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="b3ce9-140">**Azurermbackupprotectionpolicy** nesnesi almak için Get-AzureRmBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-140">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce9-141">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3ce9-141">-RetentionPolicy</span></span>
<span data-ttu-id="b3ce9-142">Yedekleme ilkesi için bir bekletme ilkeleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-142">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="b3ce9-143">**AzureRmBackupRetentionPolicy** nesnelerini edinmek için New-AzureRmBackupRetentionPolicyObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-143">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce9-144">-Haftalık</span><span class="sxs-lookup"><span data-stu-id="b3ce9-144">-Weekly</span></span>
<span data-ttu-id="b3ce9-145">Yedekleme işleminin haftalık zamanlamada çalışacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-145">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3ce9-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ce9-146">CommonParameters</span></span>
<span data-ttu-id="b3ce9-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3ce9-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ce9-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3ce9-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ce9-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3ce9-149">INPUTS</span></span>

### <span data-ttu-id="b3ce9-150">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3ce9-150">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="b3ce9-151">Parametreler: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b3ce9-151">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="b3ce9-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3ce9-152">OUTPUTS</span></span>

### <span data-ttu-id="b3ce9-153">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="b3ce9-153">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="b3ce9-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3ce9-154">NOTES</span></span>

## <span data-ttu-id="b3ce9-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3ce9-155">RELATED LINKS</span></span>

[<span data-ttu-id="b3ce9-156">Yeni-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3ce9-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


