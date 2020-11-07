---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 04ed033559abe6fe6a60922f7b11a498ff4026bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933844"
---
# <span data-ttu-id="48e84-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="48e84-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="48e84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48e84-102">SYNOPSIS</span></span>
<span data-ttu-id="48e84-103">Bu komut yeni bir Azure SQL veritabanı örneği yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48e84-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="48e84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48e84-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup -Name <String> [-PartnerResourceGroupName <String>] [-PartnerSubscriptionId <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48e84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48e84-105">DESCRIPTION</span></span>
<span data-ttu-id="48e84-106">Belirtilen bölgeler arasında belirtilen yönetilen örnek çiftiyle yeni bir Azure SQL veritabanı örneği yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48e84-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="48e84-107">Name. SqlDatabaseDnsSuffix (örneğin, Name.database.windows.net) ve Name. Secondary. SqlDatabaseDnsSuffix konumunda iki Azure SQL veritabanı TDS uç noktası oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="48e84-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="48e84-108">Bu uç noktalar, sırasıyla yük devretme grubunun birincil ve ikincil bölgelerine bağlanmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="48e84-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="48e84-109">Birincil bölge bir kesinti ile etkileniyorsa, uç noktaları ve veritabanlarının otomatik yük devretmesi, örnek yük devretme grubunun yerine çalışma ilkesi ve mehil süresi tarafından dikte edilmiş olarak tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="48e84-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="48e84-110">Örnek yük devretme grupları özelliğinin önizlemesi sırasında, '-GracePeriodWithDataLossHours ' parametresinde yalnızca 1 saat veya daha büyük değerler desteklenir.</span><span class="sxs-lookup"><span data-stu-id="48e84-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="48e84-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48e84-111">EXAMPLES</span></span>

### <span data-ttu-id="48e84-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="48e84-112">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="48e84-113">Bu komut, yönetilen örnek çifti için ' otomatik ' yerine çalışma ilkesini içeren yeni bir örnek yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48e84-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="48e84-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="48e84-114">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="48e84-115">Bu komut, yönetilen örnek çiftinin yerine çalışma ilkesi ' Manual ' içeren yeni bir örnek yük devretme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48e84-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

## <span data-ttu-id="48e84-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48e84-116">PARAMETERS</span></span>

### <span data-ttu-id="48e84-117">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="48e84-117">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="48e84-118">İkincil sunucudaki bir kesinti, salt okunur uç noktasının otomatik yük devretmesini tetiklememelidir.</span><span class="sxs-lookup"><span data-stu-id="48e84-118">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="48e84-119">Bu özellik henüz desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="48e84-119">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="48e84-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48e84-120">-DefaultProfile</span></span>
<span data-ttu-id="48e84-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48e84-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48e84-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="48e84-122">-FailoverPolicy</span></span>
<span data-ttu-id="48e84-123">Örnek yük devretme grubunun yük devretme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="48e84-123">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e84-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="48e84-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="48e84-125">Birincil sunucuda kesinti gerçekleştiğinden ve yük devretmenin veri kaybı olmadan tamamlanabilmesi için otomatik yük devretmenin ilk aralığı.</span><span class="sxs-lookup"><span data-stu-id="48e84-125">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e84-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="48e84-126">-Location</span></span>
<span data-ttu-id="48e84-127">Örnek yük devretme grubunun alınacağı yerel bölgenin adı.</span><span class="sxs-lookup"><span data-stu-id="48e84-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="48e84-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="48e84-128">-Name</span></span>
<span data-ttu-id="48e84-129">Oluşturulacak Azure SQL veritabanı yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="48e84-129">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e84-130">-Partnermanagedınstancename</span><span class="sxs-lookup"><span data-stu-id="48e84-130">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="48e84-131">Örnek yük devretme grubuna eklenecek ortak bölgedeki yönetilen örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="48e84-131">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e84-132">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="48e84-132">-PartnerRegion</span></span>
<span data-ttu-id="48e84-133">Örnek yük devretme grubunun iş ortağı bölgesinin adı.</span><span class="sxs-lookup"><span data-stu-id="48e84-133">The name of the partner region of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e84-134">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e84-134">-PartnerResourceGroupName</span></span>
<span data-ttu-id="48e84-135">Örnek yük devretme grubunun ikincil kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="48e84-135">The name of the secondary resource group of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e84-136">-Partnersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="48e84-136">-PartnerSubscriptionId</span></span>
<span data-ttu-id="48e84-137">Örnek yük devretme grubunun ikincil yönetilen örneğinin abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="48e84-137">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="48e84-138">Bu parametre yalnızca çapraz abonelik kurulumu için gereklidir</span><span class="sxs-lookup"><span data-stu-id="48e84-138">This parameter is only needed for cross-subscription setup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e84-139">-Primarymanagedınstancename</span><span class="sxs-lookup"><span data-stu-id="48e84-139">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="48e84-140">Örnek yük devretme grubuna eklenecek yerel bölgedeki yönetilen örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="48e84-140">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e84-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48e84-141">-ResourceGroupName</span></span>
<span data-ttu-id="48e84-142">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="48e84-142">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48e84-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="48e84-143">-Confirm</span></span>
<span data-ttu-id="48e84-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="48e84-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48e84-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48e84-145">-WhatIf</span></span>
<span data-ttu-id="48e84-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="48e84-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48e84-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="48e84-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48e84-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48e84-148">CommonParameters</span></span>
<span data-ttu-id="48e84-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48e84-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48e84-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48e84-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48e84-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48e84-151">INPUTS</span></span>

### <span data-ttu-id="48e84-152">System. String</span><span class="sxs-lookup"><span data-stu-id="48e84-152">System.String</span></span>

## <span data-ttu-id="48e84-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48e84-153">OUTPUTS</span></span>

### <span data-ttu-id="48e84-154">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="48e84-154">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="48e84-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48e84-155">NOTES</span></span>

## <span data-ttu-id="48e84-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48e84-156">RELATED LINKS</span></span>
