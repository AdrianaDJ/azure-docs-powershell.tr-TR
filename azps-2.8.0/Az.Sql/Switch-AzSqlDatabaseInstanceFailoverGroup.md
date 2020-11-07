---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7d52c80bba03d0e88d6e5302647fd9e6de94675f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933991"
---
# <span data-ttu-id="0d1c4-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="0d1c4-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="0d1c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d1c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1c4-103">Örnek yük devretme grubunun yük devretmesini yürütür.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="0d1c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d1c4-104">SYNTAX</span></span>

### <span data-ttu-id="0d1c4-105">Switchifvarsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0d1c4-105">SwitchIFGDefault (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d1c4-106">Kaynak kimliğinden örnek yük devretme grubuna geçme</span><span class="sxs-lookup"><span data-stu-id="0d1c4-106">Switch a Instance Failover Group from Resource Id</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d1c4-107">Bir örnek yük devretme grubuna geçiş yapma</span><span class="sxs-lookup"><span data-stu-id="0d1c4-107">Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d1c4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d1c4-108">DESCRIPTION</span></span>
<span data-ttu-id="0d1c4-109">Bu komut, örnek yük devretme grubundaki yönetilen örneklerin rollerini değiştirerek, belirtilen ikincil bölgeye yük devri yaparak yeni birincil bölge yapar.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="0d1c4-110">Birincil uç noktaya bağlanan tüm yeni TDS oturumları, yeni birincil bölgeye otomatik olarak yeniden yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="0d1c4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d1c4-111">EXAMPLES</span></span>

### <span data-ttu-id="0d1c4-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0d1c4-112">Example 1</span></span>
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

<span data-ttu-id="0d1c4-113">Örnek yük devretme grubunda yöneltme ile veri kaybına izin vererek bir yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="0d1c4-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0d1c4-114">Example 2</span></span>
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

<span data-ttu-id="0d1c4-115">Verileri kaybetmeden ya da başarısız olacak ve geri dönecek bir en iyi yük devretme işlemi yapın.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="0d1c4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d1c4-116">PARAMETERS</span></span>

### <span data-ttu-id="0d1c4-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="0d1c4-117">-AllowDataLoss</span></span>
<span data-ttu-id="0d1c4-118">Bunu yapmasanız da veri kaybına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="0d1c4-119">Bu, birincil veritabanı kullanılamaz olsa bile yük devretmenin devam etmesini sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1c4-120">-DefaultProfile</span></span>
<span data-ttu-id="0d1c4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d1c4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d1c4-122">-InputObject</span></span>
<span data-ttu-id="0d1c4-123">Geçiş yapmak için örnek yük devretme grubu nesnesi</span><span class="sxs-lookup"><span data-stu-id="0d1c4-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Switch a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="0d1c4-124">-Location</span></span>
<span data-ttu-id="0d1c4-125">Örnek yük devretme grubunun alınacağı yerel bölgenin adı.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault, Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d1c4-126">-Name</span></span>
<span data-ttu-id="0d1c4-127">Örnek yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1c4-128">-ResourceGroupName</span></span>
<span data-ttu-id="0d1c4-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SwitchIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0d1c4-130">-ResourceId</span></span>
<span data-ttu-id="0d1c4-131">Geçiş yapmak için örnek yük devretme grubunun kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: String
Parameter Sets: Switch a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d1c4-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d1c4-132">-Confirm</span></span>
<span data-ttu-id="0d1c4-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d1c4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d1c4-134">-WhatIf</span></span>
<span data-ttu-id="0d1c4-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d1c4-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d1c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1c4-137">CommonParameters</span></span>
<span data-ttu-id="0d1c4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d1c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1c4-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d1c4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1c4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d1c4-140">INPUTS</span></span>

### <span data-ttu-id="0d1c4-141">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="0d1c4-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="0d1c4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0d1c4-142">System.String</span></span>

## <span data-ttu-id="0d1c4-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d1c4-143">OUTPUTS</span></span>

### <span data-ttu-id="0d1c4-144">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="0d1c4-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="0d1c4-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d1c4-145">NOTES</span></span>

## <span data-ttu-id="0d1c4-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d1c4-146">RELATED LINKS</span></span>
