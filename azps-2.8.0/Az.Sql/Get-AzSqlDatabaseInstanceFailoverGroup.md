---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: dbb0cb56c50025e6b257d801957b1a75479220f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933669"
---
# <span data-ttu-id="7e411-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7e411-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="7e411-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e411-102">SYNOPSIS</span></span>
<span data-ttu-id="7e411-103">Örnek yük devretme gruplarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="7e411-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="7e411-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e411-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e411-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e411-105">DESCRIPTION</span></span>
<span data-ttu-id="7e411-106">Belirli bir örnek yük devretme grubunu alır veya kullanıcının aboneliğinin altındaki bir bölgede örnek yük devretme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="7e411-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="7e411-107">Örnek yük devretme grubundaki bölge, komutu yürütmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7e411-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="7e411-108">Döndürülen değerler, örnek yük devretme grubuna göre bu bölgedeki yönetilen örneklerin durumunu yansıtır.</span><span class="sxs-lookup"><span data-stu-id="7e411-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="7e411-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e411-109">EXAMPLES</span></span>

### <span data-ttu-id="7e411-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e411-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
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
}
```

<span data-ttu-id="7e411-111">Bölgedeki tüm yük devretme gruplarını listeler</span><span class="sxs-lookup"><span data-stu-id="7e411-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="7e411-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7e411-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
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

<span data-ttu-id="7e411-113">Belirli bir örnek yük devretme grubu edinin.</span><span class="sxs-lookup"><span data-stu-id="7e411-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="7e411-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e411-114">PARAMETERS</span></span>

### <span data-ttu-id="7e411-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e411-115">-DefaultProfile</span></span>
<span data-ttu-id="7e411-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e411-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e411-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="7e411-117">-Location</span></span>
<span data-ttu-id="7e411-118">Örnek yük devretme grubunun alınacağı yerel bölgenin adı.</span><span class="sxs-lookup"><span data-stu-id="7e411-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="7e411-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e411-119">-Name</span></span>
<span data-ttu-id="7e411-120">Alınacak örnek yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7e411-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e411-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e411-121">-ResourceGroupName</span></span>
<span data-ttu-id="7e411-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7e411-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7e411-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e411-123">CommonParameters</span></span>
<span data-ttu-id="7e411-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e411-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e411-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e411-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e411-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e411-126">INPUTS</span></span>

### <span data-ttu-id="7e411-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7e411-127">System.String</span></span>

## <span data-ttu-id="7e411-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e411-128">OUTPUTS</span></span>

### <span data-ttu-id="7e411-129">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="7e411-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="7e411-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e411-130">NOTES</span></span>

## <span data-ttu-id="7e411-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e411-131">RELATED LINKS</span></span>
