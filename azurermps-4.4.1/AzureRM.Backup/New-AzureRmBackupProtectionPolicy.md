---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 803299a64fb98aecc249bc7bb2f505ada74a5573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593830"
---
# <span data-ttu-id="75c74-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75c74-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="75c74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c74-102">SYNOPSIS</span></span>
<span data-ttu-id="75c74-103">Yedekleme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75c74-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75c74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75c74-104">SYNTAX</span></span>

### <span data-ttu-id="75c74-105">NoScheduleParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="75c74-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75c74-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="75c74-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75c74-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="75c74-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75c74-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="75c74-108">DESCRIPTION</span></span>
<span data-ttu-id="75c74-109">**New-AzureRmBackupProtectionPolicy** cmdlet 'ı Azure PowerShell nesnesi olarak bir Azure yedekleme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75c74-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="75c74-110">Yedekleme ilkesi, yedeklemenin ne zaman ve ne sıklıkta yedekleme</span><span class="sxs-lookup"><span data-stu-id="75c74-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="75c74-111">Enable-AzureRmBackupProtection cmdlet 'i yedekleme İlkesi kullanır.</span><span class="sxs-lookup"><span data-stu-id="75c74-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="75c74-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75c74-112">EXAMPLES</span></span>

### <span data-ttu-id="75c74-113">Örnek 1: günlük ve aylık bekletme ile günlük yedekleme ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="75c74-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="75c74-114">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="75c74-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="75c74-115">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="75c74-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="75c74-116">İkinci komut 30 günlük bekletmenin bir bekletme ilkesi oluşturur ve ardından $Daily değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="75c74-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="75c74-117">Üçüncü komut, on iki ay boyunca her ayın onuncu günü ve her ayın yirminleri boyunca yedeklemeyi tutan bekletme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75c74-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="75c74-118">Komut, bekletme ilkesini $Monthly değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="75c74-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="75c74-119">Son komutu, $Vault 'de kasa için günlük yedekleme süresi 3:00 PM olan bir yedekleme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="75c74-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="75c74-120">Komut, $Daily ve $Monthly depolanan bekletme ilkelerini atar.</span><span class="sxs-lookup"><span data-stu-id="75c74-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="75c74-121">Komut sonucu $ProtectionPolicy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="75c74-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="75c74-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75c74-122">PARAMETERS</span></span>

### <span data-ttu-id="75c74-123">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="75c74-123">-BackupTime</span></span>
<span data-ttu-id="75c74-124">Yedekleme işlemi için günün saatini bir **TarihSaat** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c74-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="75c74-125">**TarihSaat** almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="75c74-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="75c74-126">**TarihSaat** nesneleri hakkında bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="75c74-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75c74-127">-Günlük</span><span class="sxs-lookup"><span data-stu-id="75c74-127">-Daily</span></span>
<span data-ttu-id="75c74-128">Yedekleme işleminin günlük zamanlamada çalışacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75c74-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c74-129">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="75c74-129">-DaysOfWeek</span></span>
<span data-ttu-id="75c74-130">Haftanın bir günü dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c74-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="75c74-131">Bu ilke, yedekleri bu parametre tarafından belirtilen günlerde çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="75c74-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="75c74-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="75c74-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="75c74-133">Den</span><span class="sxs-lookup"><span data-stu-id="75c74-133">Monday</span></span> 
- <span data-ttu-id="75c74-134">Salı</span><span class="sxs-lookup"><span data-stu-id="75c74-134">Tuesday</span></span> 
- <span data-ttu-id="75c74-135">Günü</span><span class="sxs-lookup"><span data-stu-id="75c74-135">Wednesday</span></span> 
- <span data-ttu-id="75c74-136">Per</span><span class="sxs-lookup"><span data-stu-id="75c74-136">Thursday</span></span> 
- <span data-ttu-id="75c74-137">Cuma</span><span class="sxs-lookup"><span data-stu-id="75c74-137">Friday</span></span> 
- <span data-ttu-id="75c74-138">Günü</span><span class="sxs-lookup"><span data-stu-id="75c74-138">Saturday</span></span> 
- <span data-ttu-id="75c74-139">Gününü</span><span class="sxs-lookup"><span data-stu-id="75c74-139">Sunday</span></span>

<span data-ttu-id="75c74-140">*Weekly* parametresini belirtirseniz, bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="75c74-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75c74-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="75c74-141">-Name</span></span>
<span data-ttu-id="75c74-142">Yedekleme ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c74-142">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="75c74-143">Kasada benzersiz bir ad seçin.</span><span class="sxs-lookup"><span data-stu-id="75c74-143">Select a name that is unique in the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c74-144">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="75c74-144">-RetentionPolicy</span></span>
<span data-ttu-id="75c74-145">Yedekleme ilkesi için bir bekletme ilkeleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c74-145">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="75c74-146">**AzureRmBackupRetentionPolicy** edinmek için New-AzureRmBackupRetentionPolicyObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="75c74-146">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75c74-147">-Tür</span><span class="sxs-lookup"><span data-stu-id="75c74-147">-Type</span></span>
<span data-ttu-id="75c74-148">İlkenin uygulandığı yedekleme öğesinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c74-148">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="75c74-149">Şu anda desteklenen tek değer AzureVM.</span><span class="sxs-lookup"><span data-stu-id="75c74-149">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75c74-150">-Kasa</span><span class="sxs-lookup"><span data-stu-id="75c74-150">-Vault</span></span>
<span data-ttu-id="75c74-151">Yedekleme ilkesinin ait olduğu Azure Yedekleme Kasası 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c74-151">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="75c74-152">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="75c74-152">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75c74-153">-Haftalık</span><span class="sxs-lookup"><span data-stu-id="75c74-153">-Weekly</span></span>
<span data-ttu-id="75c74-154">Yedekleme ilkesinin haftanın bir veya birden çok günü haftalık olarak tetiklenmesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="75c74-154">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c74-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c74-155">-DefaultProfile</span></span>
<span data-ttu-id="75c74-156">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75c74-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c74-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c74-157">CommonParameters</span></span>
<span data-ttu-id="75c74-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75c74-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c74-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c74-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c74-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75c74-160">INPUTS</span></span>

### <span data-ttu-id="75c74-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="75c74-161">None</span></span>

## <span data-ttu-id="75c74-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75c74-162">OUTPUTS</span></span>

### <span data-ttu-id="75c74-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75c74-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="75c74-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75c74-164">NOTES</span></span>
* <span data-ttu-id="75c74-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="75c74-165">None</span></span>

## <span data-ttu-id="75c74-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75c74-166">RELATED LINKS</span></span>

[<span data-ttu-id="75c74-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="75c74-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="75c74-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75c74-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="75c74-169">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="75c74-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="75c74-170">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="75c74-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="75c74-171">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75c74-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="75c74-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="75c74-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


