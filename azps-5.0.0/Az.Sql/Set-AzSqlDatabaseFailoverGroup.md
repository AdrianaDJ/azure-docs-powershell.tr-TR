---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279785"
---
# <span data-ttu-id="7b3ed-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7b3ed-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="7b3ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b3ed-102">SYNOPSIS</span></span>
<span data-ttu-id="7b3ed-103">Azure SQL veritabanı yük devretme grubunun yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="7b3ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b3ed-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b3ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b3ed-105">DESCRIPTION</span></span>
<span data-ttu-id="7b3ed-106">Bu komut, bir Azure SQL veritabanı yük devretme grubunun yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="7b3ed-107">Komutu yürütmek için yük devretme grubunun birincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="7b3ed-108">Gruptaki veritabanı kümesini denetlemek için bunun yerine ' Add-AzSqlDatabaseToFailoverGroup ' ve ' Remove-AzSqlDatabaseFromFailoverGroup ' seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="7b3ed-109">Yük devretme grupları özelliğinin önizlemesi sırasında, '-GracePeriodWithDataLossHours ' parametresinde yalnızca 1 saat veya daha büyük değerler desteklenir.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="7b3ed-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b3ed-110">EXAMPLES</span></span>

### <span data-ttu-id="7b3ed-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7b3ed-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="7b3ed-112">Bir yük devretme grubunun yük devretme ilkesini ' otomatik ' olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="7b3ed-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7b3ed-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="7b3ed-114">Failover grubundaki yük devretme grubunun yük devretme ilkesini ' Manual ' olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="7b3ed-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b3ed-115">PARAMETERS</span></span>

### <span data-ttu-id="7b3ed-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="7b3ed-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="7b3ed-117">İkincil sunucudaki kesintilerin salt okunur uç noktasının otomatik yük devretmesini tetiklemesini sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="7b3ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b3ed-118">-DefaultProfile</span></span>
<span data-ttu-id="7b3ed-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7b3ed-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b3ed-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3ed-120">-FailoverGroupName</span></span>
<span data-ttu-id="7b3ed-121">Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="7b3ed-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="7b3ed-122">-FailoverPolicy</span></span>
<span data-ttu-id="7b3ed-123">Azure SQL veritabanı yük devretme grubunun yük devretme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="7b3ed-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="7b3ed-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="7b3ed-125">Birincil sunucuda kesinti gerçekleşmediğinde otomatik yük devretme öncesindeki Aralık.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="7b3ed-126">Bu, yetkisiz kullanım süresi dolmadan Azure SQL veritabanının otomatik yük devretmeyi başlatamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="7b3ed-127">Lütfen AllowDataLoss seçeneğiyle birlikte çalışma işleminin, zaman uyumsuz eşitlemenin doğası nedeniyle veri kaybına neden olabileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="7b3ed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b3ed-128">-ResourceGroupName</span></span>
<span data-ttu-id="7b3ed-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="7b3ed-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7b3ed-130">-ServerName</span></span>
<span data-ttu-id="7b3ed-131">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="7b3ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b3ed-132">CommonParameters</span></span>
<span data-ttu-id="7b3ed-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b3ed-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7b3ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b3ed-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b3ed-135">INPUTS</span></span>

### <span data-ttu-id="7b3ed-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7b3ed-136">System.String</span></span>

## <span data-ttu-id="7b3ed-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b3ed-137">OUTPUTS</span></span>

### <span data-ttu-id="7b3ed-138">Microsoft. Azure. Commands. Sql. FailoverGroup. model. Azuressqlfailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="7b3ed-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="7b3ed-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b3ed-139">NOTES</span></span>

## <span data-ttu-id="7b3ed-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b3ed-140">RELATED LINKS</span></span>

[<span data-ttu-id="7b3ed-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7b3ed-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7b3ed-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7b3ed-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7b3ed-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7b3ed-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="7b3ed-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7b3ed-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="7b3ed-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7b3ed-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7b3ed-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7b3ed-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7b3ed-147">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="7b3ed-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
