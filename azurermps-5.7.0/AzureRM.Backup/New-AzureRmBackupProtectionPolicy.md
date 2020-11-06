---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 4ea286ae6e3aec7f3eca961b5dc1452c717f3c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592957"
---
# <span data-ttu-id="6158f-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6158f-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="6158f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6158f-102">SYNOPSIS</span></span>
<span data-ttu-id="6158f-103">Yedekleme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6158f-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6158f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6158f-104">SYNTAX</span></span>

### <span data-ttu-id="6158f-105">NoScheduleParamSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6158f-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6158f-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="6158f-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6158f-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="6158f-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6158f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6158f-108">DESCRIPTION</span></span>
<span data-ttu-id="6158f-109">**New-AzureRmBackupProtectionPolicy** cmdlet 'ı Azure PowerShell nesnesi olarak bir Azure yedekleme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6158f-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="6158f-110">Yedekleme ilkesi, yedeklemenin ne zaman ve ne sıklıkta yedekleme</span><span class="sxs-lookup"><span data-stu-id="6158f-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="6158f-111">Enable-AzureRmBackupProtection cmdlet 'i yedekleme İlkesi kullanır.</span><span class="sxs-lookup"><span data-stu-id="6158f-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="6158f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6158f-112">EXAMPLES</span></span>

### <span data-ttu-id="6158f-113">Örnek 1: günlük ve aylık bekletme ile günlük yedekleme ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6158f-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="6158f-114">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="6158f-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="6158f-115">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6158f-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="6158f-116">İkinci komut 30 günlük bekletmenin bir bekletme ilkesi oluşturur ve ardından $Daily değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6158f-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="6158f-117">Üçüncü komut, on iki ay boyunca her ayın onuncu günü ve her ayın yirminleri boyunca yedeklemeyi tutan bekletme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6158f-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="6158f-118">Komut, bekletme ilkesini $Monthly değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6158f-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="6158f-119">Son komutu, $Vault 'de kasa için günlük yedekleme süresi 3:00 PM olan bir yedekleme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6158f-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="6158f-120">Komut, $Daily ve $Monthly depolanan bekletme ilkelerini atar.</span><span class="sxs-lookup"><span data-stu-id="6158f-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="6158f-121">Komut sonucu $ProtectionPolicy değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6158f-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="6158f-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6158f-122">PARAMETERS</span></span>

### <span data-ttu-id="6158f-123">-BackupTime</span><span class="sxs-lookup"><span data-stu-id="6158f-123">-BackupTime</span></span>
<span data-ttu-id="6158f-124">Yedekleme işlemi için günün saatini bir **TarihSaat** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="6158f-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="6158f-125">**TarihSaat** almak için Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6158f-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="6158f-126">**TarihSaat** nesneleri hakkında bilgi için, yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="6158f-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6158f-127">-Günlük</span><span class="sxs-lookup"><span data-stu-id="6158f-127">-Daily</span></span>
<span data-ttu-id="6158f-128">Yedekleme işleminin günlük zamanlamada çalışacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6158f-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6158f-129">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="6158f-129">-DaysOfWeek</span></span>
<span data-ttu-id="6158f-130">Haftanın bir günü dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6158f-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="6158f-131">Bu ilke, yedekleri bu parametre tarafından belirtilen günlerde çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="6158f-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="6158f-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6158f-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6158f-133">Den</span><span class="sxs-lookup"><span data-stu-id="6158f-133">Monday</span></span> 
- <span data-ttu-id="6158f-134">Salı</span><span class="sxs-lookup"><span data-stu-id="6158f-134">Tuesday</span></span> 
- <span data-ttu-id="6158f-135">Günü</span><span class="sxs-lookup"><span data-stu-id="6158f-135">Wednesday</span></span> 
- <span data-ttu-id="6158f-136">Per</span><span class="sxs-lookup"><span data-stu-id="6158f-136">Thursday</span></span> 
- <span data-ttu-id="6158f-137">Cuma</span><span class="sxs-lookup"><span data-stu-id="6158f-137">Friday</span></span> 
- <span data-ttu-id="6158f-138">Günü</span><span class="sxs-lookup"><span data-stu-id="6158f-138">Saturday</span></span> 
- <span data-ttu-id="6158f-139">Gününü</span><span class="sxs-lookup"><span data-stu-id="6158f-139">Sunday</span></span>

<span data-ttu-id="6158f-140">*Weekly* parametresini belirtirseniz, bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="6158f-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6158f-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6158f-141">-DefaultProfile</span></span>
<span data-ttu-id="6158f-142">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6158f-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6158f-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="6158f-143">-Name</span></span>
<span data-ttu-id="6158f-144">Yedekleme ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6158f-144">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="6158f-145">Kasada benzersiz bir ad seçin.</span><span class="sxs-lookup"><span data-stu-id="6158f-145">Select a name that is unique in the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6158f-146">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="6158f-146">-RetentionPolicy</span></span>
<span data-ttu-id="6158f-147">Yedekleme ilkesi için bir bekletme ilkeleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6158f-147">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="6158f-148">**AzureRmBackupRetentionPolicy** edinmek için New-AzureRmBackupRetentionPolicyObject cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6158f-148">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6158f-149">-Tür</span><span class="sxs-lookup"><span data-stu-id="6158f-149">-Type</span></span>
<span data-ttu-id="6158f-150">İlkenin uygulandığı yedekleme öğesinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6158f-150">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="6158f-151">Şu anda desteklenen tek değer AzureVM.</span><span class="sxs-lookup"><span data-stu-id="6158f-151">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6158f-152">-Kasa</span><span class="sxs-lookup"><span data-stu-id="6158f-152">-Vault</span></span>
<span data-ttu-id="6158f-153">Yedekleme ilkesinin ait olduğu Azure Yedekleme Kasası 'nı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6158f-153">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="6158f-154">**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6158f-154">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6158f-155">-Haftalık</span><span class="sxs-lookup"><span data-stu-id="6158f-155">-Weekly</span></span>
<span data-ttu-id="6158f-156">Yedekleme ilkesinin haftanın bir veya birden çok günü haftalık olarak tetiklenmesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6158f-156">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6158f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6158f-157">CommonParameters</span></span>
<span data-ttu-id="6158f-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6158f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6158f-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6158f-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6158f-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6158f-160">INPUTS</span></span>

### <span data-ttu-id="6158f-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6158f-161">None</span></span>

## <span data-ttu-id="6158f-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6158f-162">OUTPUTS</span></span>

### <span data-ttu-id="6158f-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6158f-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="6158f-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6158f-164">NOTES</span></span>
* <span data-ttu-id="6158f-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6158f-165">None</span></span>

## <span data-ttu-id="6158f-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6158f-166">RELATED LINKS</span></span>

[<span data-ttu-id="6158f-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="6158f-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="6158f-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6158f-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="6158f-169">Get-Azurermbackupkasası</span><span class="sxs-lookup"><span data-stu-id="6158f-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="6158f-170">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="6158f-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="6158f-171">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6158f-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="6158f-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="6158f-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


