---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3BF6DB10-6020-4324-A177-F07BB52AF040
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 70e6cf359f81911d8dff2e96944e93c388cfc80e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591154"
---
# <span data-ttu-id="470a3-101">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="470a3-101">Set-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="470a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="470a3-102">SYNOPSIS</span></span>
<span data-ttu-id="470a3-103">Var olan koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="470a3-103">Modifies an existing protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="470a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="470a3-104">SYNTAX</span></span>

### <span data-ttu-id="470a3-105">NoScheduleParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="470a3-105">NoScheduleParamSet (Default)</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="470a3-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="470a3-106">DailyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Daily] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="470a3-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="470a3-107">WeeklyScheduleParamSet</span></span>
```
Set-AzureRmBackupProtectionPolicy [[-NewName] <String>] [-Weekly] [[-BackupTime] <DateTime>]
 [[-RetentionPolicy] <AzureRMBackupRetentionPolicy[]>] [[-DaysOfWeek] <String[]>]
 [-ProtectionPolicy] <AzureRMBackupProtectionPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="470a3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="470a3-108">DESCRIPTION</span></span>
<span data-ttu-id="470a3-109">**Set-AzureRmBackupProtectionPolicy** cmdlet 'ı Azure Backup 'ta var olan koruma ilkesini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="470a3-109">The **Set-AzureRmBackupProtectionPolicy** cmdlet modifies an existing protection policy in Azure Backup.</span></span>
<span data-ttu-id="470a3-110">Aşağıdaki koruma ilkesi bileşenlerini değiştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="470a3-110">You can modify the following protection policy components:</span></span> 

- <span data-ttu-id="470a3-111">Adlandır</span><span class="sxs-lookup"><span data-stu-id="470a3-111">Name</span></span>
- <span data-ttu-id="470a3-112">Yedekleme zamanlaması</span><span class="sxs-lookup"><span data-stu-id="470a3-112">Backup schedule</span></span>
- <span data-ttu-id="470a3-113">Bekletme ilkeleri</span><span class="sxs-lookup"><span data-stu-id="470a3-113">Retention policies</span></span>

<span data-ttu-id="470a3-114">Herhangi bir değişiklik, ilkeyle ilişkili öğelerin yedekleme ve tutma etkilerini etkileyebilir.</span><span class="sxs-lookup"><span data-stu-id="470a3-114">Any change might affect the backup and retention of the items associated with the policy.</span></span>

## <span data-ttu-id="470a3-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="470a3-115">EXAMPLES</span></span>

## <span data-ttu-id="470a3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="470a3-116">PARAMETERS</span></span>

### <span data-ttu-id="470a3-117">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="470a3-117">-BackupTime</span></span>
<span data-ttu-id="470a3-118">İlkenin yeni yedekleme saatini, bir **Tarih saat** nesnesi olarak ilke için belirtir.</span><span class="sxs-lookup"><span data-stu-id="470a3-118">Specifies the new backup time of day, as a **DateTime** object, for the policy.</span></span>
<span data-ttu-id="470a3-119">**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="470a3-119">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="470a3-120">**TarihSaat** nesneleri hakkında bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="470a3-120">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="470a3-121">-Günlük</span><span class="sxs-lookup"><span data-stu-id="470a3-121">-Daily</span></span>
<span data-ttu-id="470a3-122">Yedekleme işleminin günlük zamanlamada çalışacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="470a3-122">Indicates that the backup operation runs on a Daily schedule.</span></span>

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

### <span data-ttu-id="470a3-123">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="470a3-123">-DaysOfWeek</span></span>
<span data-ttu-id="470a3-124">Haftanın bir günü dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="470a3-124">Specifies an array of days of the week.</span></span>
<span data-ttu-id="470a3-125">Bu ilke, yedekleri bu parametre tarafından belirtilen günlerde çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="470a3-125">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="470a3-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="470a3-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="470a3-127">Den</span><span class="sxs-lookup"><span data-stu-id="470a3-127">Monday</span></span> 
- <span data-ttu-id="470a3-128">Salı</span><span class="sxs-lookup"><span data-stu-id="470a3-128">Tuesday</span></span> 
- <span data-ttu-id="470a3-129">Günü</span><span class="sxs-lookup"><span data-stu-id="470a3-129">Wednesday</span></span> 
- <span data-ttu-id="470a3-130">Per</span><span class="sxs-lookup"><span data-stu-id="470a3-130">Thursday</span></span> 
- <span data-ttu-id="470a3-131">Cuma</span><span class="sxs-lookup"><span data-stu-id="470a3-131">Friday</span></span> 
- <span data-ttu-id="470a3-132">Günü</span><span class="sxs-lookup"><span data-stu-id="470a3-132">Saturday</span></span> 
- <span data-ttu-id="470a3-133">Gününü</span><span class="sxs-lookup"><span data-stu-id="470a3-133">Sunday</span></span>

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

### <span data-ttu-id="470a3-134">-NewName</span><span class="sxs-lookup"><span data-stu-id="470a3-134">-NewName</span></span>
<span data-ttu-id="470a3-135">İlkenin yeni adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="470a3-135">Specifies the new name for the policy.</span></span>
<span data-ttu-id="470a3-136">Bu ad kasada benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="470a3-136">This name must be unique in a vault.</span></span>

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

### <span data-ttu-id="470a3-137">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="470a3-137">-ProtectionPolicy</span></span>
<span data-ttu-id="470a3-138">Bu cmdlet 'in değiştirdiği koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="470a3-138">Specifies protection policy that this cmdlet modifies.</span></span>
<span data-ttu-id="470a3-139">**Azurermbackupprotectionpolicy** nesnesi almak için Get-AzureRmBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="470a3-139">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="470a3-140">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="470a3-140">-RetentionPolicy</span></span>
<span data-ttu-id="470a3-141">Yedekleme ilkesi için bir bekletme ilkeleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="470a3-141">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="470a3-142">**AzureRmBackupRetentionPolicy** nesnelerini edinmek için New-AzureRmBackupRetentionPolicyObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="470a3-142">To obtain **AzureRmBackupRetentionPolicy** objects, use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

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

### <span data-ttu-id="470a3-143">-Haftalık</span><span class="sxs-lookup"><span data-stu-id="470a3-143">-Weekly</span></span>
<span data-ttu-id="470a3-144">Yedekleme işleminin haftalık zamanlamada çalışacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="470a3-144">Indicates that the backup operation runs on a Weekly schedule.</span></span>

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

### <span data-ttu-id="470a3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470a3-145">-DefaultProfile</span></span>
<span data-ttu-id="470a3-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="470a3-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="470a3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470a3-147">CommonParameters</span></span>
<span data-ttu-id="470a3-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="470a3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470a3-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470a3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470a3-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="470a3-150">INPUTS</span></span>

### <span data-ttu-id="470a3-151">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="470a3-151">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="470a3-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="470a3-152">OUTPUTS</span></span>

### <span data-ttu-id="470a3-153">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="470a3-153">None</span></span>

## <span data-ttu-id="470a3-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="470a3-154">NOTES</span></span>

## <span data-ttu-id="470a3-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="470a3-155">RELATED LINKS</span></span>

[<span data-ttu-id="470a3-156">Yeni-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="470a3-156">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


