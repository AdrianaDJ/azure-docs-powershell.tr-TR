---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c5dd678a851e663b04746bb4a5780624ea4c5f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593626"
---
# <span data-ttu-id="c9dcc-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c9dcc-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="c9dcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9dcc-102">SYNOPSIS</span></span>
<span data-ttu-id="c9dcc-103">Bu komut yeni bir Azure SQL veritabanı yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9dcc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9dcc-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9dcc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9dcc-105">DESCRIPTION</span></span>
<span data-ttu-id="c9dcc-106">Belirtilen sunucular için yeni bir Azure SQL veritabanı yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="c9dcc-107">Bir Azure SQL veritabanı TDS uç noktası FailoverGroupName. SqlDatabaseDnsSuffix (örneğin, FailoverGroupName.database.windows.net) ve FailoverGroupName. Secondary. SqlDatabaseDnsSuffix 'da oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="c9dcc-108">Bu uç noktalar, sırasıyla yük devretme grubundaki birincil ve ikincil sunuculara bağlanmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="c9dcc-109">Birincil sunucu bir kesinti ile etkileniyorsa uç noktaların ve veritabanlarının otomatik yük devretmesi, yük devretme grubunun yerine çalışma ilkesi ve yetkisiz kullanım süresi tarafından dikte edilir.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="c9dcc-110">Yeni oluşturulan yük devretme grupları herhangi bir veritabanı içermiyor.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="c9dcc-111">Bir yük devretme grubundaki veritabanı kümesini denetlemek için ' Add-AzureRmSqlDatabaseToFailoverGroup ' ve ' Remove-AzureRmSqlDatabaseFromFailoverGroup ' cmdlet 'lerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="c9dcc-112">Yük devretme grupları özelliğinin önizlemesi sırasında, '-GracePeriodWithDataLossHours ' parametresinde yalnızca 1 saat veya daha büyük değerler desteklenir.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="c9dcc-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9dcc-113">EXAMPLES</span></span>

### <span data-ttu-id="c9dcc-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c9dcc-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="c9dcc-115">Bu komut, aynı kaynak grubundaki iki sunucu için ' otomatik ' yerine çalışma ilkesini içeren yeni bir yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="c9dcc-116">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c9dcc-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="c9dcc-117">Bu komut, farklı kaynak gruplarındaki iki sunucu için ' Manual ' yük devretme ilkesini içeren yeni bir yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="c9dcc-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9dcc-118">PARAMETERS</span></span>

### <span data-ttu-id="c9dcc-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="c9dcc-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="c9dcc-120">İkincil sunucudaki bir kesinti, salt okunur uç noktasının otomatik yük devretmesini tetiklememelidir.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="c9dcc-121">Bu özellik henüz desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="c9dcc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9dcc-122">-DefaultProfile</span></span>
<span data-ttu-id="c9dcc-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c9dcc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9dcc-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="c9dcc-124">-FailoverGroupName</span></span>
<span data-ttu-id="c9dcc-125">Oluşturulacak Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="c9dcc-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="c9dcc-126">-FailoverPolicy</span></span>
<span data-ttu-id="c9dcc-127">Azure SQL veritabanı yük devretme grubunun yük devretme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="c9dcc-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="c9dcc-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="c9dcc-129">Birincil sunucuda kesinti gerçekleştiğinden ve yük devretmenin veri kaybı olmadan tamamlanabilmesi için otomatik yük devretmenin ilk aralığı.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="c9dcc-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9dcc-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c9dcc-131">Azure SQL veritabanı yük devretme grubunun ikincil kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="c9dcc-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c9dcc-132">-PartnerServerName</span></span>
<span data-ttu-id="c9dcc-133">Azure SQL veritabanı yük devretme grubunun ikincil sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="c9dcc-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9dcc-134">-ResourceGroupName</span></span>
<span data-ttu-id="c9dcc-135">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="c9dcc-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9dcc-136">-ServerName</span></span>
<span data-ttu-id="c9dcc-137">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="c9dcc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9dcc-138">CommonParameters</span></span>
<span data-ttu-id="c9dcc-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9dcc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9dcc-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9dcc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9dcc-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9dcc-141">INPUTS</span></span>

### <span data-ttu-id="c9dcc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c9dcc-142">System.String</span></span>

## <span data-ttu-id="c9dcc-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9dcc-143">OUTPUTS</span></span>

### <span data-ttu-id="c9dcc-144">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="c9dcc-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="c9dcc-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9dcc-145">NOTES</span></span>

## <span data-ttu-id="c9dcc-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9dcc-146">RELATED LINKS</span></span>

[<span data-ttu-id="c9dcc-147">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c9dcc-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c9dcc-148">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c9dcc-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c9dcc-149">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c9dcc-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="c9dcc-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c9dcc-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="c9dcc-151">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c9dcc-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c9dcc-152">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c9dcc-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c9dcc-153">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c9dcc-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
