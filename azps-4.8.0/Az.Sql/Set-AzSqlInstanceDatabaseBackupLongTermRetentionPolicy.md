---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: cf7cf1dcd91bc1c9f703e4fc5ca613ad6407e575
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266770"
---
# <span data-ttu-id="119f4-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="119f4-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="119f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="119f4-102">SYNOPSIS</span></span>
<span data-ttu-id="119f4-103">**Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet 'i yönetilen veritabanının uzun süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="119f4-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="119f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="119f4-104">SYNTAX</span></span>

### <span data-ttu-id="119f4-105">WeeklyRetentionRequired (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="119f4-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="119f4-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="119f4-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="119f4-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="119f4-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="119f4-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="119f4-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="119f4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="119f4-109">DESCRIPTION</span></span>
<span data-ttu-id="119f4-110">**Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet 'i, bu yönetilen veritabanı için uzun süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="119f4-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="119f4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="119f4-111">EXAMPLES</span></span>

### <span data-ttu-id="119f4-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="119f4-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -WeeklyRetention "P1W"


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P1W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="119f4-113">Veritabanının uzun süreli bekletme haftalık ilkesini bir hafta olarak yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="119f4-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="119f4-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="119f4-114">Example 2</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName target1 -RemovePolicy


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : target1
WeeklyRetention     : PT0S
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="119f4-115">Bu komut, veritabanından uzun süreli bekletme ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="119f4-115">This command removes the long term retention policy from the database.</span></span>

### <span data-ttu-id="119f4-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="119f4-116">Example 3</span></span>

<span data-ttu-id="119f4-117">Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet 'i yönetilen veritabanının uzun süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="119f4-117">The Set-AzSqlInstanceDatabaseLongTermRetentionBackup cmdlet sets a managed database's long term retention policy.</span></span> <span data-ttu-id="119f4-118">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="119f4-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -DatabaseName target1 -InstanceName testInstance -MonthlyRetention P24W -ResourceGroupName testResourceGroup -WeekOfYear 26 -WeeklyRetention 'P1W' -YearlyRetention P10Y
```

## <span data-ttu-id="119f4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="119f4-119">PARAMETERS</span></span>

### <span data-ttu-id="119f4-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="119f4-120">-DatabaseName</span></span>
<span data-ttu-id="119f4-121">Kullanılacak Azure yönetilen veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="119f4-121">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="119f4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="119f4-122">-DefaultProfile</span></span>
<span data-ttu-id="119f4-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="119f4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="119f4-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="119f4-124">-InstanceName</span></span>
<span data-ttu-id="119f4-125">Veritabanının ait olduğu Azure yönetilen örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="119f4-125">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="119f4-126">-Monthlyalıkoyma</span><span class="sxs-lookup"><span data-stu-id="119f4-126">-MonthlyRetention</span></span>
<span data-ttu-id="119f4-127">Aylık bekletme.</span><span class="sxs-lookup"><span data-stu-id="119f4-127">The Monthly Retention.</span></span>
<span data-ttu-id="119f4-128">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="119f4-128">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="119f4-129">En az 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="119f4-129">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="119f4-130">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="119f4-130">-RemovePolicy</span></span>
<span data-ttu-id="119f4-131">Sağlanmışsa, veritabanı ilkesi temizlenir.</span><span class="sxs-lookup"><span data-stu-id="119f4-131">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="119f4-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="119f4-132">-ResourceGroupName</span></span>
<span data-ttu-id="119f4-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="119f4-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="119f4-134">-Weeklyalımesi</span><span class="sxs-lookup"><span data-stu-id="119f4-134">-WeeklyRetention</span></span>
<span data-ttu-id="119f4-135">Haftalık bekletme.</span><span class="sxs-lookup"><span data-stu-id="119f4-135">The Weekly Retention.</span></span>
<span data-ttu-id="119f4-136">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="119f4-136">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="119f4-137">En az 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="119f4-137">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="119f4-138">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="119f4-138">-WeekOfYear</span></span>
<span data-ttu-id="119f4-139">Yıllık bekletmenin kaydedileceği yılın haftası, 1-52.</span><span class="sxs-lookup"><span data-stu-id="119f4-139">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="119f4-140">-Yıllıkbekletme</span><span class="sxs-lookup"><span data-stu-id="119f4-140">-YearlyRetention</span></span>
<span data-ttu-id="119f4-141">Yıllık bekletme.</span><span class="sxs-lookup"><span data-stu-id="119f4-141">The Yearly Retention.</span></span>
<span data-ttu-id="119f4-142">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="119f4-142">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="119f4-143">En az 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="119f4-143">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="119f4-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="119f4-144">-Confirm</span></span>
<span data-ttu-id="119f4-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="119f4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="119f4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="119f4-146">-WhatIf</span></span>
<span data-ttu-id="119f4-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="119f4-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="119f4-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="119f4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="119f4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="119f4-149">CommonParameters</span></span>
<span data-ttu-id="119f4-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="119f4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="119f4-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="119f4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="119f4-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="119f4-152">INPUTS</span></span>

### <span data-ttu-id="119f4-153">System. String</span><span class="sxs-lookup"><span data-stu-id="119f4-153">System.String</span></span>

### <span data-ttu-id="119f4-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="119f4-154">System.Int32</span></span>

## <span data-ttu-id="119f4-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="119f4-155">OUTPUTS</span></span>

### <span data-ttu-id="119f4-156">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="119f4-156">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="119f4-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="119f4-157">NOTES</span></span>

## <span data-ttu-id="119f4-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="119f4-158">RELATED LINKS</span></span>

[<span data-ttu-id="119f4-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="119f4-159">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="119f4-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="119f4-160">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="119f4-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="119f4-161">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="119f4-162">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="119f4-162">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)