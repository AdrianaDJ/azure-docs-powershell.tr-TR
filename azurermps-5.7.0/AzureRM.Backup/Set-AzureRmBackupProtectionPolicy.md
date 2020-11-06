---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 7d41abd1d56bab4df0d716c3a9d11ea14140b784
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592943"
---
# <span data-ttu-id="7125c-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7125c-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="7125c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7125c-102">SYNOPSIS</span></span>
<span data-ttu-id="7125c-103">Var olan koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7125c-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7125c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7125c-104">SYNTAX</span></span>

### <span data-ttu-id="7125c-105">NoScheduleParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7125c-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7125c-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="7125c-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7125c-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="7125c-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7125c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7125c-108">DESCRIPTION</span></span>
<span data-ttu-id="7125c-109">**Set-AzureRmBackupProtectionPolicy** cmdlet 'ı Azure Backup 'ta var olan koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7125c-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="7125c-110">Aşağıdaki koruma ilkesi bileşenlerini değiştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7125c-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="7125c-111">Adlandır</span><span class="sxs-lookup"><span data-stu-id="7125c-111">Name</span></span>
- <span data-ttu-id="7125c-112">Yedekleme zamanlaması</span><span class="sxs-lookup"><span data-stu-id="7125c-112">Backup schedule</span></span>
- <span data-ttu-id="7125c-113">Bekletme ilkeleri</span><span class="sxs-lookup"><span data-stu-id="7125c-113">Retention policies</span></span>

<span data-ttu-id="7125c-114">Herhangi bir değişiklik, ilkeyle ilişkili öğelerin yedekleme ve tutma etkilerini etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="7125c-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="7125c-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7125c-115">EXAMPLES</span></span>

## <span data-ttu-id="7125c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7125c-116">PARAMETERS</span></span>

### <span data-ttu-id="7125c-117">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="7125c-117">-BackupTime</span></span>
<span data-ttu-id="7125c-118">İlkenin yeni yedekleme saatini, bir **Tarih saat** nesnesi olarak ilke için belirtir.</span><span class="sxs-lookup"><span data-stu-id="7125c-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="7125c-119">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7125c-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="7125c-120">**TarihSaat** nesneleri hakkında bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7125c-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125c-121">-Günlük</span><span class="sxs-lookup"><span data-stu-id="7125c-121">-Daily</span></span>
<span data-ttu-id="7125c-122">Yedekleme işleminin günlük zamanlamada çalışacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7125c-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125c-123">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="7125c-123">-DaysOfWeek</span></span>
<span data-ttu-id="7125c-124">Haftanın bir günü dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7125c-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="7125c-125">Bu ilke, yedekleri bu parametre tarafından belirtilen günlerde çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="7125c-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="7125c-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7125c-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7125c-127">Den</span><span class="sxs-lookup"><span data-stu-id="7125c-127">Monday</span></span> 
- <span data-ttu-id="7125c-128">Salı</span><span class="sxs-lookup"><span data-stu-id="7125c-128">Tuesday</span></span> 
- <span data-ttu-id="7125c-129">Günü</span><span class="sxs-lookup"><span data-stu-id="7125c-129">Wednesday</span></span> 
- <span data-ttu-id="7125c-130">Per</span><span class="sxs-lookup"><span data-stu-id="7125c-130">Thursday</span></span> 
- <span data-ttu-id="7125c-131">Cuma</span><span class="sxs-lookup"><span data-stu-id="7125c-131">Friday</span></span> 
- <span data-ttu-id="7125c-132">Günü</span><span class="sxs-lookup"><span data-stu-id="7125c-132">Saturday</span></span> 
- <span data-ttu-id="7125c-133">Gününü</span><span class="sxs-lookup"><span data-stu-id="7125c-133">Sunday</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7125c-134">-DefaultProfile</span></span>
<span data-ttu-id="7125c-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7125c-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125c-136">-NewName</span><span class="sxs-lookup"><span data-stu-id="7125c-136">-NewName</span></span>
<span data-ttu-id="7125c-137">İlkenin yeni adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7125c-137">Specifies the new name for the policy.</span></span>
<span data-ttu-id="7125c-138">Bu ad kasada benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7125c-138">This name must be unique in a vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125c-139">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7125c-139">-ProtectionPolicy</span></span>
<span data-ttu-id="7125c-140">Bu cmdlet 'in değiştirdiği koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7125c-140">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="7125c-141">**Azurermbackupprotectionpolicy** nesnesi almak için Get-AzureRmBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7125c-141">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7125c-142">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7125c-142">-RetentionPolicy</span></span>
<span data-ttu-id="7125c-143">Yedekleme ilkesi için bir bekletme ilkeleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7125c-143">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="7125c-144">**AzureRmBackupRetentionPolicy** nesnelerini edinmek için New-AzureRmBackupRetentionPolicyObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7125c-144">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125c-145">-Haftalık</span><span class="sxs-lookup"><span data-stu-id="7125c-145">-Weekly</span></span>
<span data-ttu-id="7125c-146">Yedekleme işleminin haftalık zamanlamada çalışacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7125c-146">Indicates that the backup operation runs on a Weekly schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7125c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7125c-147">CommonParameters</span></span>
<span data-ttu-id="7125c-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7125c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7125c-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7125c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7125c-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7125c-150">INPUTS</span></span>

### <span data-ttu-id="7125c-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7125c-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="7125c-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7125c-152">OUTPUTS</span></span>

### <span data-ttu-id="7125c-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7125c-153">None</span></span>

## <span data-ttu-id="7125c-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7125c-154">NOTES</span></span>

## <span data-ttu-id="7125c-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7125c-155">RELATED LINKS</span></span>

[<span data-ttu-id="7125c-156">Yeni-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7125c-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


