---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 8027af33b9ea4f4184c10963da69e8be3b4e3961
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933819"
---
# <span data-ttu-id="e0019-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="e0019-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="e0019-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0019-102">SYNOPSIS</span></span>
<span data-ttu-id="e0019-103">Örnek yük devretme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0019-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="e0019-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0019-104">SYNTAX</span></span>

### <span data-ttu-id="e0019-105">Removeıfgdefault (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0019-105">RemoveIFGDefault (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0019-106">Kaynak kimliğinden örnek yük devretme grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="e0019-106">Remove a Instance Failover Group from Resource Id</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0019-107">Azures, ınstancefailovergroupmodel örneği tanımından örnek yük devretme grubunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="e0019-107">Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0019-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0019-108">DESCRIPTION</span></span>
<span data-ttu-id="e0019-109">Bu komut, belirtilen ada sahip örnek yük devretme grubunu kaldırır ve tüm veritabanlarını aynen bırakır.</span><span class="sxs-lookup"><span data-stu-id="e0019-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="e0019-110">DNS 'den dinleyici uç noktasının kaydı silinir.</span><span class="sxs-lookup"><span data-stu-id="e0019-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="e0019-111">Örneği yürütmek için örnek yük devretme grubunun birincil bölgesi kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e0019-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="e0019-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0019-112">EXAMPLES</span></span>

### <span data-ttu-id="e0019-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e0019-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="e0019-114">Örnek yük devretme grubunu kaldırma.</span><span class="sxs-lookup"><span data-stu-id="e0019-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="e0019-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0019-115">PARAMETERS</span></span>

### <span data-ttu-id="e0019-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0019-116">-DefaultProfile</span></span>
<span data-ttu-id="e0019-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0019-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0019-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e0019-118">-Force</span></span>
<span data-ttu-id="e0019-119">Eylemi gerçekleştirmek için onay iletisini atlayın.</span><span class="sxs-lookup"><span data-stu-id="e0019-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="e0019-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0019-120">-InputObject</span></span>
<span data-ttu-id="e0019-121">Kaldırılacak örnek yük devretme grubu nesnesi</span><span class="sxs-lookup"><span data-stu-id="e0019-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Remove a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0019-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="e0019-122">-Location</span></span>
<span data-ttu-id="e0019-123">Örnek yük devretme grubunun alınacağı yerel bölgenin adı.</span><span class="sxs-lookup"><span data-stu-id="e0019-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault, Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0019-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="e0019-124">-Name</span></span>
<span data-ttu-id="e0019-125">Kaldırılacak örnek yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e0019-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0019-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0019-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0019-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e0019-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0019-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e0019-128">-ResourceId</span></span>
<span data-ttu-id="e0019-129">Kaldırılacak örnek yük devretme grubunun kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e0019-129">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: String
Parameter Sets: Remove a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0019-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0019-130">-Confirm</span></span>
<span data-ttu-id="e0019-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0019-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0019-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0019-132">-WhatIf</span></span>
<span data-ttu-id="e0019-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0019-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0019-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0019-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0019-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0019-135">CommonParameters</span></span>
<span data-ttu-id="e0019-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0019-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0019-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0019-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0019-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0019-138">INPUTS</span></span>

### <span data-ttu-id="e0019-139">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="e0019-139">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="e0019-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e0019-140">System.String</span></span>

## <span data-ttu-id="e0019-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0019-141">OUTPUTS</span></span>

### <span data-ttu-id="e0019-142">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="e0019-142">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="e0019-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0019-143">NOTES</span></span>

## <span data-ttu-id="e0019-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0019-144">RELATED LINKS</span></span>
