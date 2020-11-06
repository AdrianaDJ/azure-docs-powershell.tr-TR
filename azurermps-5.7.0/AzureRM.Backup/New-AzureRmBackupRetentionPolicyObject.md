---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupretentionpolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 0673b0c98e263a0c947fa984267e0eb49ccf9f9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592956"
---
# <span data-ttu-id="adf43-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="adf43-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="adf43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adf43-102">SYNOPSIS</span></span>
<span data-ttu-id="adf43-103">Yedekleme bekletme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="adf43-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adf43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="adf43-104">SYNTAX</span></span>

### <span data-ttu-id="adf43-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="adf43-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adf43-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="adf43-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adf43-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="adf43-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adf43-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="adf43-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adf43-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="adf43-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adf43-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="adf43-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="adf43-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="adf43-111">DESCRIPTION</span></span>
<span data-ttu-id="adf43-112">**New-AzureRmBackupRetentionPolicyObject** cmdlet 'ı bir Azure yedekleme bekletme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="adf43-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="adf43-113">Bekletme ilkesi yedeklemenin bir kurtarma noktası olmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="adf43-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="adf43-114">Bekletme türleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="adf43-114">The types of retention are the following:</span></span> 

- <span data-ttu-id="adf43-115">Mü</span><span class="sxs-lookup"><span data-stu-id="adf43-115">Daily</span></span> 
- <span data-ttu-id="adf43-116">Haftalık</span><span class="sxs-lookup"><span data-stu-id="adf43-116">Weekly</span></span> 
- <span data-ttu-id="adf43-117">Aylık</span><span class="sxs-lookup"><span data-stu-id="adf43-117">Monthly</span></span> 
- <span data-ttu-id="adf43-118">Yıllık</span><span class="sxs-lookup"><span data-stu-id="adf43-118">Yearly</span></span> 

<span data-ttu-id="adf43-119">Kullanmayı düşündüğünüz her bir bekletme türü için bir bekletme ilkesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="adf43-119">Create one retention policy for each type of retention that you plan to use.</span></span>

<span data-ttu-id="adf43-120">Yedekleme ilkesi en az bir bekletme ilkesiyle ilişkilendirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="adf43-120">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="adf43-121">Yedekleme ilkesi oluşturmak için New-AzureRmBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="adf43-121">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="adf43-122">Bunun yerine Enable-AzureRmBackupProtection cmdlet 'e bir bekletme ilkesi sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="adf43-122">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="adf43-123">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="adf43-123">EXAMPLES</span></span>

### <span data-ttu-id="adf43-124">Örnek 1: günlük tutma için bekletme ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="adf43-124">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="adf43-125">İlk komut 30 günlük bekletmenin bir bekletme ilkesi oluşturur ve ardından $Daily değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="adf43-125">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="adf43-126">İkinci komut $Daily içeriğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="adf43-126">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="adf43-127">Örnek 2: aylık bir bekletme ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="adf43-127">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="adf43-128">İlk komut, on iki ay boyunca her ayın onuncu günü ve her ayın yirminleri boyunca yedeklemeyi tutan bekletme ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="adf43-128">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="adf43-129">Komut, bekletme ilkesini $Monthly değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="adf43-129">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="adf43-130">İkinci komut $Monthly içeriğini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="adf43-130">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="adf43-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="adf43-131">PARAMETERS</span></span>

### <span data-ttu-id="adf43-132">-Günlüktutma</span><span class="sxs-lookup"><span data-stu-id="adf43-132">-DailyRetention</span></span>
<span data-ttu-id="adf43-133">Bu cmdlet 'in günlük bekletme ilkesi oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="adf43-133">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-134">-Daysofay</span><span class="sxs-lookup"><span data-stu-id="adf43-134">-DaysOfMonth</span></span>
<span data-ttu-id="adf43-135">Hangi kurtarma noktalarının yedeğine ve ne kadar süreyle saklanacağını tanımlayan ay günlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="adf43-135">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="adf43-136">Bu parametre için kabul edilebilir değerler: 1 ila 28 ve son tamsayılar.</span><span class="sxs-lookup"><span data-stu-id="adf43-136">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="adf43-137">*Dailyalımı* , *MonthlyRetentionInDailyFormat* ve *YearlyRetentionInDailyFormat* parametrelerini belirtmeniz durumunda bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="adf43-137">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-138">-Daysofya</span><span class="sxs-lookup"><span data-stu-id="adf43-138">-DaysOfWeek</span></span>
<span data-ttu-id="adf43-139">Haftanın bir günü dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="adf43-139">Specifies an array of days of the week.</span></span>
<span data-ttu-id="adf43-140">Bu cmdlet 'in hangi kurtarma noktalarının saklanacağını ve ne süreyle kaldığını tanımlayan günler.</span><span class="sxs-lookup"><span data-stu-id="adf43-140">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="adf43-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="adf43-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="adf43-142">Den</span><span class="sxs-lookup"><span data-stu-id="adf43-142">Monday</span></span> 
- <span data-ttu-id="adf43-143">Salı</span><span class="sxs-lookup"><span data-stu-id="adf43-143">Tuesday</span></span> 
- <span data-ttu-id="adf43-144">Günü</span><span class="sxs-lookup"><span data-stu-id="adf43-144">Wednesday</span></span> 
- <span data-ttu-id="adf43-145">Per</span><span class="sxs-lookup"><span data-stu-id="adf43-145">Thursday</span></span> 
- <span data-ttu-id="adf43-146">Cuma</span><span class="sxs-lookup"><span data-stu-id="adf43-146">Friday</span></span> 
- <span data-ttu-id="adf43-147">Günü</span><span class="sxs-lookup"><span data-stu-id="adf43-147">Saturday</span></span> 
- <span data-ttu-id="adf43-148">Gününü</span><span class="sxs-lookup"><span data-stu-id="adf43-148">Sunday</span></span>

<span data-ttu-id="adf43-149">*Weeklyalıkoyma* , *MonthlyRetentionInWeeklyFormat* ve *YearlyRetentionInWeeklyFormat* parametrelerini belirtirseniz bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="adf43-149">Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>

<span data-ttu-id="adf43-150">Yedekleme ve bekletme için seçtiğiniz hafta günlerinin hizalandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="adf43-150">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="adf43-151">Örneğin, yedeğiniz Cumartesi günleri ayarlanmışsa, bekletme ilkelerinin da Cumartesi kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="adf43-151">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adf43-152">-DefaultProfile</span></span>
<span data-ttu-id="adf43-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="adf43-153">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adf43-154">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="adf43-154">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="adf43-155">Bu cmdlet 'in günlük biçimde bir aylık ilke oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="adf43-155">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-156">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="adf43-156">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="adf43-157">Bu cmdlet 'in haftalık biçimde bir aylık ilke oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="adf43-157">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-158">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="adf43-158">-MonthsOfYear</span></span>
<span data-ttu-id="adf43-159">Hangi ayların yedekleme 'nin yıllık olarak sakladığı kurtarma noktalarına sahip olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="adf43-159">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="adf43-160">Bu parametre için kabul edilebilir değerler: ay, Ocak veya Şubat gibi değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="adf43-160">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-161">-Bekletme</span><span class="sxs-lookup"><span data-stu-id="adf43-161">-Retention</span></span>
<span data-ttu-id="adf43-162">Yedekleme bir yedekleme noktasını saklayan saklama süresini gün, ay veya yıl olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="adf43-162">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="adf43-163">Birim, bu cmdlet 'in günlük, aylık veya yıllık bekletme seçeneğini seçdiğine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="adf43-163">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="adf43-164">Örneğin, *Dailyalıkoyma* parametresini belirtirseniz cmdlet, geçerli parametreyi gün sayısı olarak yorumlar.</span><span class="sxs-lookup"><span data-stu-id="adf43-164">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-165">-Weeklyalımesi</span><span class="sxs-lookup"><span data-stu-id="adf43-165">-WeeklyRetention</span></span>
<span data-ttu-id="adf43-166">Bu cmdlet 'in haftalık bekletme ilkesi oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="adf43-166">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-167">-Haftanumarası</span><span class="sxs-lookup"><span data-stu-id="adf43-167">-WeekNumber</span></span>
<span data-ttu-id="adf43-168">Hangi kurtarma noktalarının yedeğine ve ne kadar süreyle saklanacağını tanımlayan ayın haftasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="adf43-168">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="adf43-169">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="adf43-169">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="adf43-170">Eklemelisiniz</span><span class="sxs-lookup"><span data-stu-id="adf43-170">First</span></span> 
- <span data-ttu-id="adf43-171">İden</span><span class="sxs-lookup"><span data-stu-id="adf43-171">Second</span></span> 
- <span data-ttu-id="adf43-172">Üç</span><span class="sxs-lookup"><span data-stu-id="adf43-172">Third</span></span> 
- <span data-ttu-id="adf43-173">Dördüncü</span><span class="sxs-lookup"><span data-stu-id="adf43-173">Fourth</span></span> 
- <span data-ttu-id="adf43-174">Soya</span><span class="sxs-lookup"><span data-stu-id="adf43-174">Last</span></span>

```yaml
Type: String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-175">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="adf43-175">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="adf43-176">Bu cmdlet 'in günlük biçimde bir yıllık bekletme ilkesi oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="adf43-176">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-177">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="adf43-177">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="adf43-178">Bu cmdlet 'in haftalık biçimde bir yıllık bekletme ilkesi oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="adf43-178">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adf43-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adf43-179">CommonParameters</span></span>
<span data-ttu-id="adf43-180">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="adf43-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adf43-181">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adf43-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adf43-182">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="adf43-182">INPUTS</span></span>

### <span data-ttu-id="adf43-183">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="adf43-183">None</span></span>

## <span data-ttu-id="adf43-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="adf43-184">OUTPUTS</span></span>

### <span data-ttu-id="adf43-185">AzureRmBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="adf43-185">AzureRmBackupRetentionPolicy</span></span>

## <span data-ttu-id="adf43-186">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="adf43-186">NOTES</span></span>
* <span data-ttu-id="adf43-187">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="adf43-187">None</span></span>

## <span data-ttu-id="adf43-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="adf43-188">RELATED LINKS</span></span>

[<span data-ttu-id="adf43-189">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="adf43-189">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="adf43-190">Yeni-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="adf43-190">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


