---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278800"
---
# <span data-ttu-id="69509-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="69509-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="69509-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69509-102">SYNOPSIS</span></span>
<span data-ttu-id="69509-103">Sunucu uzun bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="69509-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="69509-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69509-104">SYNTAX</span></span>

### <span data-ttu-id="69509-105">WeeklyRetentionRequired (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69509-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69509-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="69509-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69509-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="69509-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69509-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="69509-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69509-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="69509-109">DESCRIPTION</span></span>
<span data-ttu-id="69509-110">**Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen uzun süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="69509-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="69509-111">İlke, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="69509-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="69509-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69509-112">EXAMPLES</span></span>

### <span data-ttu-id="69509-113">Örnek 1: uzun vadeli bekletme ilkesinin geçerli sürümü için haftalık bekletmenin ayarlanması</span><span class="sxs-lookup"><span data-stu-id="69509-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="69509-114">Bu, database01 'in uzun süreli bekletme ilkesini, haftada iki haftada iki haftada bir tüm</span><span class="sxs-lookup"><span data-stu-id="69509-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="69509-115">Örnek 2: uzun süreli bekletme ilkesinin geçerli sürümü için aylık bekletmenin ayarlanması</span><span class="sxs-lookup"><span data-stu-id="69509-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="69509-116">Bu, database01 uygulamasının uzun süreli bekletme ilkesini her ay 5 yıl süreyle kaydetmek için ayarlar.</span><span class="sxs-lookup"><span data-stu-id="69509-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="69509-117">Örnek 3: uzun süreli bekletme ilkesinin geçerli sürümü için yıllık bekletmenin miktarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="69509-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="69509-118">Bu, 10 yıl için yılın 26 tarihinde alınan tam yedeklemeyi kaydetmek üzere database01 'in uzun süreli bekletme ilkesini ayarlar</span><span class="sxs-lookup"><span data-stu-id="69509-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="69509-119">Örnek 4: uzun süreli bekletme ilkesinin geçerli sürümü için her bir bekletme ayarlayın</span><span class="sxs-lookup"><span data-stu-id="69509-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="69509-120">Bu, her tam yedeklemeyi 14 gün süreyle kaydetmek için database01 'un uzun süreli bekletme ilkesini ayarlar, her ayın 24 haftası için ilk tam yedeklemesini ve 10 yıl için yılın 26 tarihinde alınan tam yedeklemeyi</span><span class="sxs-lookup"><span data-stu-id="69509-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="69509-121">Örnek 5: uzun süreli bekletme ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="69509-121">Example 5: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="69509-122">Database01 ilkesini kaldırarak uzun süreli bekletme yedeklemelerini artık kaydetmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="69509-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="69509-123">Bu, önceden alınmış yedekleri etkilemez</span><span class="sxs-lookup"><span data-stu-id="69509-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="69509-124">Örnek 6: uzun süreli bekletme ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="69509-124">Example 6: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="69509-125">Bu, artık uzun süreli bekletme yedeklemelerini kaydetmemek için database01 ilkesini kaldırmanın bir başka yoludur.</span><span class="sxs-lookup"><span data-stu-id="69509-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="69509-126">Bu, önceden alınmış yedekleri etkilemez</span><span class="sxs-lookup"><span data-stu-id="69509-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="69509-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69509-127">PARAMETERS</span></span>

### <span data-ttu-id="69509-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="69509-128">-DatabaseName</span></span>
<span data-ttu-id="69509-129">Kullanılacak Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="69509-129">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69509-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69509-130">-DefaultProfile</span></span>
<span data-ttu-id="69509-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69509-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69509-132">-Monthlyalıkoyma</span><span class="sxs-lookup"><span data-stu-id="69509-132">-MonthlyRetention</span></span>
<span data-ttu-id="69509-133">Aylık bekletme.</span><span class="sxs-lookup"><span data-stu-id="69509-133">The Monthly Retention.</span></span>
<span data-ttu-id="69509-134">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="69509-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="69509-135">En az 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="69509-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69509-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="69509-136">-RemovePolicy</span></span>
<span data-ttu-id="69509-137">Sağlanmışsa, veritabanı ilkesi kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="69509-137">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69509-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69509-138">-ResourceGroupName</span></span>
<span data-ttu-id="69509-139">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="69509-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69509-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69509-140">-ServerName</span></span>
<span data-ttu-id="69509-141">Veritabanının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="69509-141">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69509-142">-Weeklyalımesi</span><span class="sxs-lookup"><span data-stu-id="69509-142">-WeeklyRetention</span></span>
<span data-ttu-id="69509-143">Haftalık bekletme.</span><span class="sxs-lookup"><span data-stu-id="69509-143">The Weekly Retention.</span></span>
<span data-ttu-id="69509-144">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="69509-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="69509-145">En az 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="69509-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69509-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="69509-146">-WeekOfYear</span></span>
<span data-ttu-id="69509-147">Yıllık bekletmenin kaydedileceği yılın haftası, 1-52.</span><span class="sxs-lookup"><span data-stu-id="69509-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69509-148">-Yıllıkbekletme</span><span class="sxs-lookup"><span data-stu-id="69509-148">-YearlyRetention</span></span>
<span data-ttu-id="69509-149">Yıllık bekletme.</span><span class="sxs-lookup"><span data-stu-id="69509-149">The Yearly Retention.</span></span>
<span data-ttu-id="69509-150">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="69509-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="69509-151">En az 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="69509-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69509-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="69509-152">-Confirm</span></span>
<span data-ttu-id="69509-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69509-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69509-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69509-154">-WhatIf</span></span>
<span data-ttu-id="69509-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69509-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69509-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69509-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69509-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69509-157">CommonParameters</span></span>
<span data-ttu-id="69509-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69509-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69509-159">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69509-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69509-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69509-160">INPUTS</span></span>

### <span data-ttu-id="69509-161">System. String</span><span class="sxs-lookup"><span data-stu-id="69509-161">System.String</span></span>

### <span data-ttu-id="69509-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="69509-162">System.Int32</span></span>

## <span data-ttu-id="69509-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69509-163">OUTPUTS</span></span>

### <span data-ttu-id="69509-164">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="69509-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="69509-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69509-165">NOTES</span></span>

## <span data-ttu-id="69509-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69509-166">RELATED LINKS</span></span>

[<span data-ttu-id="69509-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="69509-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="69509-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="69509-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="69509-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="69509-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="69509-170">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="69509-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)