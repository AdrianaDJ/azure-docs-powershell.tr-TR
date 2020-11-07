---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5d734836f822b61ac37ca0ba567eda4473e0292e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938018"
---
# <span data-ttu-id="b913f-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b913f-101">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="b913f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b913f-102">SYNOPSIS</span></span>
<span data-ttu-id="b913f-103">**Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet 'i yönetilen veritabanının uzun süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b913f-103">The **Set-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet sets a managed database's long term retention policy.</span></span>

## <span data-ttu-id="b913f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b913f-104">SYNTAX</span></span>

### <span data-ttu-id="b913f-105">WeeklyRetentionRequired (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b913f-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b913f-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="b913f-106">RemovePolicy</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b913f-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="b913f-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-InstanceName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b913f-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="b913f-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b913f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b913f-109">DESCRIPTION</span></span>
<span data-ttu-id="b913f-110">**Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet 'i, bu yönetilen veritabanı için uzun süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b913f-110">The **Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy for this managed database.</span></span>

## <span data-ttu-id="b913f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b913f-111">EXAMPLES</span></span>

### <span data-ttu-id="b913f-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b913f-112">Example 1</span></span>
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

<span data-ttu-id="b913f-113">Veritabanının uzun süreli bekletme haftalık ilkesini bir hafta olarak yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="b913f-113">Configures the database's long term retention weekly policy to one week.</span></span>

### <span data-ttu-id="b913f-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="b913f-114">Example 2</span></span>
```
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


<span data-ttu-id="b913f-115">Bu komut, veritabanından uzun süreli bekletme ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b913f-115">This command removes the long term retention policy from the database.</span></span>
## <span data-ttu-id="b913f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b913f-116">PARAMETERS</span></span>

### <span data-ttu-id="b913f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b913f-117">-DatabaseName</span></span>
<span data-ttu-id="b913f-118">Kullanılacak Azure yönetilen veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="b913f-118">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="b913f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b913f-119">-DefaultProfile</span></span>
<span data-ttu-id="b913f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b913f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b913f-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b913f-121">-InstanceName</span></span>
<span data-ttu-id="b913f-122">Veritabanının ait olduğu Azure yönetilen örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="b913f-122">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="b913f-123">-Monthlyalıkoyma</span><span class="sxs-lookup"><span data-stu-id="b913f-123">-MonthlyRetention</span></span>
<span data-ttu-id="b913f-124">Aylık bekletme.</span><span class="sxs-lookup"><span data-stu-id="b913f-124">The Monthly Retention.</span></span>
<span data-ttu-id="b913f-125">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="b913f-125">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b913f-126">En az 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="b913f-126">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b913f-127">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="b913f-127">-RemovePolicy</span></span>
<span data-ttu-id="b913f-128">Sağlanmışsa, veritabanı ilkesi temizlenir.</span><span class="sxs-lookup"><span data-stu-id="b913f-128">If provided, the policy for the database will be cleared.</span></span>

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

### <span data-ttu-id="b913f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b913f-129">-ResourceGroupName</span></span>
<span data-ttu-id="b913f-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b913f-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b913f-131">-Weeklyalımesi</span><span class="sxs-lookup"><span data-stu-id="b913f-131">-WeeklyRetention</span></span>
<span data-ttu-id="b913f-132">Haftalık bekletme.</span><span class="sxs-lookup"><span data-stu-id="b913f-132">The Weekly Retention.</span></span>
<span data-ttu-id="b913f-133">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="b913f-133">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b913f-134">En az 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="b913f-134">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b913f-135">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="b913f-135">-WeekOfYear</span></span>
<span data-ttu-id="b913f-136">Yıllık bekletmenin kaydedileceği yılın haftası, 1-52.</span><span class="sxs-lookup"><span data-stu-id="b913f-136">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b913f-137">-Yıllıkbekletme</span><span class="sxs-lookup"><span data-stu-id="b913f-137">-YearlyRetention</span></span>
<span data-ttu-id="b913f-138">Yıllık bekletme.</span><span class="sxs-lookup"><span data-stu-id="b913f-138">The Yearly Retention.</span></span>
<span data-ttu-id="b913f-139">ISO 8601 dizesi yerine yalnızca bir sayı geçirilirse, günler birimler olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="b913f-139">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="b913f-140">En az 7 gün ve en fazla 10 yıldır.</span><span class="sxs-lookup"><span data-stu-id="b913f-140">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b913f-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="b913f-141">-Confirm</span></span>
<span data-ttu-id="b913f-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b913f-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b913f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b913f-143">-WhatIf</span></span>
<span data-ttu-id="b913f-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b913f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b913f-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b913f-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b913f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b913f-146">CommonParameters</span></span>
<span data-ttu-id="b913f-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b913f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b913f-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b913f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b913f-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b913f-149">INPUTS</span></span>

### <span data-ttu-id="b913f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="b913f-150">System.String</span></span>

### <span data-ttu-id="b913f-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="b913f-151">System.Int32</span></span>

## <span data-ttu-id="b913f-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b913f-152">OUTPUTS</span></span>

### <span data-ttu-id="b913f-153">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b913f-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="b913f-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b913f-154">NOTES</span></span>

## <span data-ttu-id="b913f-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b913f-155">RELATED LINKS</span></span>

[<span data-ttu-id="b913f-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b913f-156">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b913f-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b913f-157">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b913f-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b913f-158">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b913f-159">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b913f-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)