---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937969"
---
# <span data-ttu-id="5292a-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5292a-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="5292a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5292a-102">SYNOPSIS</span></span>
<span data-ttu-id="5292a-103">Örnek yük devretme grubunun yük devretmesini yürütür.</span><span class="sxs-lookup"><span data-stu-id="5292a-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="5292a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5292a-104">SYNTAX</span></span>

### <span data-ttu-id="5292a-105">Switchınstancefailovergroupdefaultset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5292a-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5292a-106">Switchınstancefailovergroupbyresourceıdset</span><span class="sxs-lookup"><span data-stu-id="5292a-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5292a-107">Switchınstancefailovergroupbyinputobjectset</span><span class="sxs-lookup"><span data-stu-id="5292a-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5292a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5292a-108">DESCRIPTION</span></span>
<span data-ttu-id="5292a-109">Bu komut, örnek yük devretme grubundaki yönetilen örneklerin rollerini değiştirerek, belirtilen ikincil bölgeye yük devri yaparak yeni birincil bölge yapar.</span><span class="sxs-lookup"><span data-stu-id="5292a-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="5292a-110">Birincil uç noktaya bağlanan tüm yeni TDS oturumları, yeni birincil bölgeye otomatik olarak yeniden yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="5292a-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="5292a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5292a-111">EXAMPLES</span></span>

### <span data-ttu-id="5292a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5292a-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
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

<span data-ttu-id="5292a-113">Örnek yük devretme grubunda yöneltme ile veri kaybına izin vererek bir yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="5292a-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="5292a-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5292a-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
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

<span data-ttu-id="5292a-115">Verileri kaybetmeden ya da başarısız olacak ve geri dönecek bir en iyi yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="5292a-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="5292a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5292a-116">PARAMETERS</span></span>

### <span data-ttu-id="5292a-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="5292a-117">-AllowDataLoss</span></span>
<span data-ttu-id="5292a-118">Bunu yapmasanız da veri kaybına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="5292a-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="5292a-119">Bu, birincil veritabanı kullanılamaz olsa bile yük devretmenin devam etmesini sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="5292a-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5292a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5292a-120">-DefaultProfile</span></span>
<span data-ttu-id="5292a-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5292a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5292a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5292a-122">-InputObject</span></span>
<span data-ttu-id="5292a-123">Geçiş yapmak için örnek yük devretme grubu nesnesi</span><span class="sxs-lookup"><span data-stu-id="5292a-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5292a-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="5292a-124">-Location</span></span>
<span data-ttu-id="5292a-125">Örnek yük devretme grubunun alınacağı yerel bölgenin adı.</span><span class="sxs-lookup"><span data-stu-id="5292a-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5292a-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="5292a-126">-Name</span></span>
<span data-ttu-id="5292a-127">Örnek yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5292a-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5292a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5292a-128">-ResourceGroupName</span></span>
<span data-ttu-id="5292a-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5292a-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5292a-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="5292a-130">-ResourceId</span></span>
<span data-ttu-id="5292a-131">Geçiş yapmak için örnek yük devretme grubunun kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5292a-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5292a-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="5292a-132">-Confirm</span></span>
<span data-ttu-id="5292a-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5292a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5292a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5292a-134">-WhatIf</span></span>
<span data-ttu-id="5292a-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5292a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5292a-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5292a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5292a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5292a-137">CommonParameters</span></span>
<span data-ttu-id="5292a-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5292a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5292a-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5292a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5292a-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5292a-140">INPUTS</span></span>

### <span data-ttu-id="5292a-141">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="5292a-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="5292a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5292a-142">System.String</span></span>

## <span data-ttu-id="5292a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5292a-143">OUTPUTS</span></span>

### <span data-ttu-id="5292a-144">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="5292a-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="5292a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5292a-145">NOTES</span></span>

## <span data-ttu-id="5292a-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5292a-146">RELATED LINKS</span></span>
