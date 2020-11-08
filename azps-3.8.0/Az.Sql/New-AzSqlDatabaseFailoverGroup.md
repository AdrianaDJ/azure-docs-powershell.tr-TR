---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c1164f7c4875d6cdd00ca13236c1d8e6d4b07cb3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096223"
---
# <span data-ttu-id="be44c-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="be44c-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="be44c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be44c-102">SYNOPSIS</span></span>
<span data-ttu-id="be44c-103">Bu komut yeni bir Azure SQL veritabanı yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be44c-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="be44c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be44c-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be44c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be44c-105">DESCRIPTION</span></span>
<span data-ttu-id="be44c-106">Belirtilen sunucular için yeni bir Azure SQL veritabanı yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be44c-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="be44c-107">Bir Azure SQL veritabanı TDS uç noktası FailoverGroupName. SqlDatabaseDnsSuffix (örneğin, FailoverGroupName.database.windows.net) ve FailoverGroupName. Secondary. SqlDatabaseDnsSuffix 'da oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="be44c-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="be44c-108">Bu uç noktalar, sırasıyla yük devretme grubundaki birincil ve ikincil sunuculara bağlanmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="be44c-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="be44c-109">Birincil sunucu bir kesinti ile etkileniyorsa uç noktaların ve veritabanlarının otomatik yük devretmesi, yük devretme grubunun yerine çalışma ilkesi ve yetkisiz kullanım süresi tarafından dikte edilir.</span><span class="sxs-lookup"><span data-stu-id="be44c-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="be44c-110">Yeni oluşturulan yük devretme grupları herhangi bir veritabanı içermiyor.</span><span class="sxs-lookup"><span data-stu-id="be44c-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="be44c-111">Bir yük devretme grubundaki veritabanı kümesini denetlemek için ' Add-AzSqlDatabaseToFailoverGroup ' ve ' Remove-AzSqlDatabaseFromFailoverGroup ' cmdlet 'lerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="be44c-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="be44c-112">'-GracePeriodWithDataLossHours ' parametresinde yalnızca 1 saatten büyük veya buna eşit değerler desteklenir.</span><span class="sxs-lookup"><span data-stu-id="be44c-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="be44c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be44c-113">EXAMPLES</span></span>

### <span data-ttu-id="be44c-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="be44c-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="be44c-115">Bu komut, aynı kaynak grubundaki iki sunucu için ' otomatik ' yerine çalışma ilkesini içeren yeni bir yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be44c-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="be44c-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="be44c-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="be44c-117">Bu komut, farklı kaynak gruplarındaki iki sunucu için ' Manual ' yük devretme ilkesini içeren yeni bir yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="be44c-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="be44c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be44c-118">PARAMETERS</span></span>

### <span data-ttu-id="be44c-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="be44c-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="be44c-120">İkincil sunucudaki bir kesinti, salt okunur uç noktasının otomatik yük devretmesini tetiklememelidir.</span><span class="sxs-lookup"><span data-stu-id="be44c-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="be44c-121">Bu özellik henüz desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="be44c-121">This feature is not yet supported.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be44c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be44c-122">-DefaultProfile</span></span>
<span data-ttu-id="be44c-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="be44c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be44c-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="be44c-124">-FailoverGroupName</span></span>
<span data-ttu-id="be44c-125">Oluşturulacak Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="be44c-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be44c-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="be44c-126">-FailoverPolicy</span></span>
<span data-ttu-id="be44c-127">Azure SQL veritabanı yük devretme grubunun yük devretme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="be44c-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be44c-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="be44c-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="be44c-129">Birincil sunucuda kesinti gerçekleştiğinden ve yük devretmenin veri kaybı olmadan tamamlanabilmesi için otomatik yük devretmenin ilk aralığı.</span><span class="sxs-lookup"><span data-stu-id="be44c-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be44c-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be44c-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="be44c-131">Azure SQL veritabanı yük devretme grubunun ikincil kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="be44c-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be44c-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="be44c-132">-PartnerServerName</span></span>
<span data-ttu-id="be44c-133">Azure SQL veritabanı yük devretme grubunun ikincil sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="be44c-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be44c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be44c-134">-ResourceGroupName</span></span>
<span data-ttu-id="be44c-135">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="be44c-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="be44c-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="be44c-136">-ServerName</span></span>
<span data-ttu-id="be44c-137">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="be44c-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="be44c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be44c-138">CommonParameters</span></span>
<span data-ttu-id="be44c-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be44c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be44c-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="be44c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be44c-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be44c-141">INPUTS</span></span>

### <span data-ttu-id="be44c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="be44c-142">System.String</span></span>

## <span data-ttu-id="be44c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be44c-143">OUTPUTS</span></span>

### <span data-ttu-id="be44c-144">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="be44c-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="be44c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be44c-145">NOTES</span></span>

## <span data-ttu-id="be44c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be44c-146">RELATED LINKS</span></span>

[<span data-ttu-id="be44c-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="be44c-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="be44c-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="be44c-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="be44c-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="be44c-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="be44c-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="be44c-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="be44c-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="be44c-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="be44c-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="be44c-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="be44c-153">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="be44c-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)