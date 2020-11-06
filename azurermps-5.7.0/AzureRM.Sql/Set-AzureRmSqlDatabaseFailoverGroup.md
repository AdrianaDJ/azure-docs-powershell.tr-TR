---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: e5452ef5b6d8b2e5535c5388d5d42698aa7c261f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588701"
---
# <span data-ttu-id="99e59-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="99e59-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="99e59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99e59-102">SYNOPSIS</span></span>
<span data-ttu-id="99e59-103">Azure SQL veritabanı yük devretme grubunun yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="99e59-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99e59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99e59-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99e59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99e59-105">DESCRIPTION</span></span>
<span data-ttu-id="99e59-106">Bu komut, bir Azure SQL veritabanı yük devretme grubunun yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="99e59-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="99e59-107">Komutu yürütmek için yük devretme grubunun birincil sunucusu kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="99e59-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="99e59-108">Gruptaki veritabanı kümesini denetlemek için bunun yerine ' Add-AzureRmSqlDatabaseToFailoverGroup ' ve ' Remove-AzureRmSqlDatabaseFromFailoverGroup ' seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="99e59-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="99e59-109">Yük devretme grupları özelliğinin önizlemesi sırasında, '-GracePeriodWithDataLossHours ' parametresinde yalnızca 1 saat veya daha büyük değerler desteklenir.</span><span class="sxs-lookup"><span data-stu-id="99e59-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="99e59-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99e59-110">EXAMPLES</span></span>

### <span data-ttu-id="99e59-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="99e59-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="99e59-112">Bir yük devretme grubunun yük devretme ilkesini ' otomatik ' olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="99e59-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="99e59-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="99e59-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="99e59-114">Failover grubundaki yük devretme grubunun yük devretme ilkesini ' Manual ' olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="99e59-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="99e59-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99e59-115">PARAMETERS</span></span>

### <span data-ttu-id="99e59-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="99e59-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="99e59-117">İkincil sunucudaki kesintilerin salt okunur uç noktasının otomatik yük devretmesini tetiklemesini sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="99e59-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="99e59-118">Bu özellik henüz desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="99e59-118">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e59-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e59-119">-DefaultProfile</span></span>
<span data-ttu-id="99e59-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="99e59-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99e59-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="99e59-121">-FailoverGroupName</span></span>
<span data-ttu-id="99e59-122">Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="99e59-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="99e59-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="99e59-123">-FailoverPolicy</span></span>
<span data-ttu-id="99e59-124">Azure SQL veritabanı yük devretme grubunun yük devretme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="99e59-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e59-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="99e59-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="99e59-126">Birincil sunucuda kesinti gerçekleşmediğinde otomatik yük devretme öncesindeki Aralık.</span><span class="sxs-lookup"><span data-stu-id="99e59-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="99e59-127">Bu, yetkisiz kullanım süresi dolmadan Azure SQL veritabanının otomatik yük devretmeyi başlatamadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99e59-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="99e59-128">Lütfen AllowDataLoss seçeneğiyle birlikte çalışma işleminin, zaman uyumsuz eşitlemenin doğası nedeniyle veri kaybına neden olabileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="99e59-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99e59-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e59-129">-ResourceGroupName</span></span>
<span data-ttu-id="99e59-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="99e59-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="99e59-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="99e59-131">-ServerName</span></span>
<span data-ttu-id="99e59-132">Yük devretme grubundaki birincil Azure SQL veritabanı sunucusunun adı.</span><span class="sxs-lookup"><span data-stu-id="99e59-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="99e59-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e59-133">CommonParameters</span></span>
<span data-ttu-id="99e59-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99e59-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e59-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e59-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e59-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99e59-136">INPUTS</span></span>

### <span data-ttu-id="99e59-137">System. String</span><span class="sxs-lookup"><span data-stu-id="99e59-137">System.String</span></span>

## <span data-ttu-id="99e59-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99e59-138">OUTPUTS</span></span>

### <span data-ttu-id="99e59-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="99e59-139">System.Object</span></span>

## <span data-ttu-id="99e59-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99e59-140">NOTES</span></span>

## <span data-ttu-id="99e59-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99e59-141">RELATED LINKS</span></span>

[<span data-ttu-id="99e59-142">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="99e59-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="99e59-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="99e59-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="99e59-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="99e59-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="99e59-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="99e59-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="99e59-146">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="99e59-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="99e59-147">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="99e59-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="99e59-148">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="99e59-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
