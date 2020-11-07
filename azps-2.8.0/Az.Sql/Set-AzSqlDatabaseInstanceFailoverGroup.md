---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 38e19e764e7a9d272db777a295f05016f0ef95af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933719"
---
# <span data-ttu-id="22542-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="22542-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="22542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22542-102">SYNOPSIS</span></span>
<span data-ttu-id="22542-103">Örnek yük devretme grubunun yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="22542-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="22542-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22542-104">SYNTAX</span></span>

### <span data-ttu-id="22542-105">Tüm (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="22542-105">SetIFGDefault (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22542-106">Kaynak kimliğinden bir örnek yük devretme grubu ayarlama</span><span class="sxs-lookup"><span data-stu-id="22542-106">Set a Instance Failover Group from Resource Id</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22542-107">Azures, ınstancefailovergroupmodel örneği tanımından bir örnek yük devretme grubu ayarlama</span><span class="sxs-lookup"><span data-stu-id="22542-107">Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22542-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="22542-108">DESCRIPTION</span></span>
<span data-ttu-id="22542-109">Bu komut, bir örnek yük devretme grubunun yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="22542-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="22542-110">Örneği yürütmek için örnek yük devretme grubunun birincil bölgesi kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="22542-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="22542-111">Örnek yük devretme grupları özelliğinin önizlemesi sırasında, '-GracePeriodWithDataLossHours ' parametresinde yalnızca 1 saat veya daha büyük değerler desteklenir.</span><span class="sxs-lookup"><span data-stu-id="22542-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="22542-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22542-112">EXAMPLES</span></span>

### <span data-ttu-id="22542-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="22542-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
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

<span data-ttu-id="22542-114">Yük devretme grubunun yük devretme ilkesini, yük devretme grubunda boru tarafından ' Manual ' olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="22542-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="22542-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22542-115">PARAMETERS</span></span>

### <span data-ttu-id="22542-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="22542-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="22542-117">İkincil sunucudaki kesintilerin salt okunur uç noktasının otomatik yük devretmesini tetiklemesini sağlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="22542-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="22542-118">Bu özellik henüz desteklenmiyor.</span><span class="sxs-lookup"><span data-stu-id="22542-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="22542-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22542-119">-DefaultProfile</span></span>
<span data-ttu-id="22542-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22542-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22542-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="22542-121">-FailoverPolicy</span></span>
<span data-ttu-id="22542-122">Örnek yük devretme grubunun yük devretme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="22542-122">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="22542-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="22542-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="22542-124">Birincil sunucuda kesinti gerçekleştiğinden ve yük devretmenin veri kaybı olmadan tamamlanabilmesi için otomatik yük devretmenin ilk aralığı.</span><span class="sxs-lookup"><span data-stu-id="22542-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="22542-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22542-125">-InputObject</span></span>
<span data-ttu-id="22542-126">Ayarlanacak örnek yük devretme grubu nesnesi</span><span class="sxs-lookup"><span data-stu-id="22542-126">The Instance Failover Group object to set</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22542-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="22542-127">-Location</span></span>
<span data-ttu-id="22542-128">Örnek yük devretme grubunun alınacağı yerel bölgenin adı.</span><span class="sxs-lookup"><span data-stu-id="22542-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault, Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22542-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="22542-129">-Name</span></span>
<span data-ttu-id="22542-130">Örnek yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="22542-130">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22542-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22542-131">-ResourceGroupName</span></span>
<span data-ttu-id="22542-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="22542-132">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22542-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="22542-133">-ResourceId</span></span>
<span data-ttu-id="22542-134">Ayarlanacak örnek yük devretme grubunun kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="22542-134">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: String
Parameter Sets: Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22542-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="22542-135">-Confirm</span></span>
<span data-ttu-id="22542-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22542-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22542-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22542-137">-WhatIf</span></span>
<span data-ttu-id="22542-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22542-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22542-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22542-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22542-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22542-140">CommonParameters</span></span>
<span data-ttu-id="22542-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22542-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22542-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22542-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22542-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22542-143">INPUTS</span></span>

### <span data-ttu-id="22542-144">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="22542-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="22542-145">System. String</span><span class="sxs-lookup"><span data-stu-id="22542-145">System.String</span></span>

## <span data-ttu-id="22542-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22542-146">OUTPUTS</span></span>

### <span data-ttu-id="22542-147">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="22542-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="22542-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22542-148">NOTES</span></span>

## <span data-ttu-id="22542-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22542-149">RELATED LINKS</span></span>
