---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: c5450ea3ffdcc8c76fa88c8721902b8f8ae77794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588706"
---
# <span data-ttu-id="c20dd-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c20dd-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="c20dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c20dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c20dd-103">Sunucu uzun bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c20dd-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c20dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c20dd-104">SYNTAX</span></span>

### <span data-ttu-id="c20dd-105">WeeklyRetentionRequired (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c20dd-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c20dd-106">Eski</span><span class="sxs-lookup"><span data-stu-id="c20dd-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c20dd-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="c20dd-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c20dd-108">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="c20dd-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>] [-MonthlyRetention] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c20dd-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="c20dd-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>]
 [[-MonthlyRetention] <String>] [-YearlyRetention] <String> [-WeekOfYear] <Int32> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c20dd-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="c20dd-110">DESCRIPTION</span></span>
<span data-ttu-id="c20dd-111">**Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen uzun süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c20dd-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="c20dd-112">İlke, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="c20dd-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="c20dd-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c20dd-113">EXAMPLES</span></span>

### <span data-ttu-id="c20dd-114">Örnek 1: uzun vadeli bekletme ilkesinin geçerli sürümü için haftalık bekletmenin ayarlanması</span><span class="sxs-lookup"><span data-stu-id="c20dd-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c20dd-115">Bu, database01 'in uzun süreli bekletme ilkesini, haftada iki haftada iki haftada bir tüm</span><span class="sxs-lookup"><span data-stu-id="c20dd-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="c20dd-116">Örnek 2: uzun süreli bekletme ilkesinin geçerli sürümü için aylık bekletmenin ayarlanması</span><span class="sxs-lookup"><span data-stu-id="c20dd-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c20dd-117">Bu, database01 uygulamasının uzun süreli bekletme ilkesini her ay 5 yıl süreyle kaydetmek için ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c20dd-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="c20dd-118">Örnek 3: uzun süreli bekletme ilkesinin geçerli sürümü için yıllık bekletmenin miktarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="c20dd-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c20dd-119">Bu, 10 yıl için yılın 26 tarihinde alınan tam yedeklemeyi kaydetmek üzere database01 'in uzun süreli bekletme ilkesini ayarlar</span><span class="sxs-lookup"><span data-stu-id="c20dd-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="c20dd-120">Örnek 4: uzun süreli bekletme ilkesinin geçerli sürümü için her bir bekletme ayarlayın</span><span class="sxs-lookup"><span data-stu-id="c20dd-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c20dd-121">Bu, her tam yedeklemeyi 14 gün süreyle kaydetmek için database01 'un uzun süreli bekletme ilkesini ayarlar, her ayın 24 haftası için ilk tam yedeklemesini ve 10 yıl için yılın 26 tarihinde alınan tam yedeklemeyi</span><span class="sxs-lookup"><span data-stu-id="c20dd-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="c20dd-122">Örnek 4: uzun süreli bekletme ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c20dd-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c20dd-123">Database01 ilkesini kaldırarak uzun süreli bekletme yedeklemelerini artık kaydetmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="c20dd-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="c20dd-124">Bu, önceden alınmış yedekleri etkilemez</span><span class="sxs-lookup"><span data-stu-id="c20dd-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="c20dd-125">Örnek 4: uzun süreli bekletme ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c20dd-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="c20dd-126">Bu, artık uzun süreli bekletme yedeklemelerini kaydetmemek için database01 ilkesini kaldırmanın bir başka yoludur.</span><span class="sxs-lookup"><span data-stu-id="c20dd-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="c20dd-127">Bu, önceden alınmış yedekleri etkilemez</span><span class="sxs-lookup"><span data-stu-id="c20dd-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="c20dd-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c20dd-128">PARAMETERS</span></span>

### <span data-ttu-id="c20dd-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c20dd-129">-DatabaseName</span></span>
<span data-ttu-id="c20dd-130">Kullanılacak Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c20dd-130">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c20dd-131">-DefaultProfile</span></span>
<span data-ttu-id="c20dd-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c20dd-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c20dd-133">-Monthlyalıkoyma</span><span class="sxs-lookup"><span data-stu-id="c20dd-133">-MonthlyRetention</span></span>
<span data-ttu-id="c20dd-134">Aylık bekletme.</span><span class="sxs-lookup"><span data-stu-id="c20dd-134">The Monthly Retention.</span></span>
<span data-ttu-id="c20dd-135">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="c20dd-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c20dd-136">En fazla 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="c20dd-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="c20dd-137">-RemovePolicy</span></span>
<span data-ttu-id="c20dd-138">Sağlanmışsa, veritabanı ilkesi kaldırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="c20dd-138">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c20dd-139">-ResourceGroupName</span></span>
<span data-ttu-id="c20dd-140">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c20dd-140">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c20dd-141">-ResourceId</span></span>
<span data-ttu-id="c20dd-142">Uzun vadeli bekletme ilkesinin yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="c20dd-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c20dd-143">-ServerName</span></span>
<span data-ttu-id="c20dd-144">Veritabanının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="c20dd-144">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-145">Durumlu</span><span class="sxs-lookup"><span data-stu-id="c20dd-145">-State</span></span>
<span data-ttu-id="c20dd-146">Uzun vadeli bekletme yedekleme ilkesinin durumu, ' Enabled ' veya ' Disabled '</span><span class="sxs-lookup"><span data-stu-id="c20dd-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-147">-Weeklyalımesi</span><span class="sxs-lookup"><span data-stu-id="c20dd-147">-WeeklyRetention</span></span>
<span data-ttu-id="c20dd-148">Haftalık bekletme.</span><span class="sxs-lookup"><span data-stu-id="c20dd-148">The Weekly Retention.</span></span>
<span data-ttu-id="c20dd-149">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="c20dd-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c20dd-150">En fazla 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="c20dd-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="c20dd-151">-WeekOfYear</span></span>
<span data-ttu-id="c20dd-152">Yıllık bekletmenin kaydedileceği yılın haftası, 1-52.</span><span class="sxs-lookup"><span data-stu-id="c20dd-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-153">-Yıllıkbekletme</span><span class="sxs-lookup"><span data-stu-id="c20dd-153">-YearlyRetention</span></span>
<span data-ttu-id="c20dd-154">Yıllık bekletme.</span><span class="sxs-lookup"><span data-stu-id="c20dd-154">The Yearly Retention.</span></span>
<span data-ttu-id="c20dd-155">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="c20dd-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="c20dd-156">En fazla 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="c20dd-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-157">-Onay</span><span class="sxs-lookup"><span data-stu-id="c20dd-157">-Confirm</span></span>
<span data-ttu-id="c20dd-158">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c20dd-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c20dd-159">-WhatIf</span></span>
<span data-ttu-id="c20dd-160">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c20dd-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c20dd-161">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c20dd-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20dd-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c20dd-162">CommonParameters</span></span>
<span data-ttu-id="c20dd-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c20dd-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c20dd-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c20dd-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c20dd-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c20dd-165">INPUTS</span></span>

### <span data-ttu-id="c20dd-166">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c20dd-166">None</span></span>
<span data-ttu-id="c20dd-167">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c20dd-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c20dd-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c20dd-168">OUTPUTS</span></span>

### <span data-ttu-id="c20dd-169">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c20dd-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="c20dd-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c20dd-170">NOTES</span></span>

## <span data-ttu-id="c20dd-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c20dd-171">RELATED LINKS</span></span>

[<span data-ttu-id="c20dd-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c20dd-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="c20dd-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c20dd-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c20dd-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="c20dd-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="c20dd-175">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c20dd-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
