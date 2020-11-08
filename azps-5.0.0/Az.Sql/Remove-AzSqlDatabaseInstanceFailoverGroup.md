---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276634"
---
# <span data-ttu-id="63753-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="63753-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="63753-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63753-102">SYNOPSIS</span></span>
<span data-ttu-id="63753-103">Örnek yük devretme grubunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63753-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="63753-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63753-104">SYNTAX</span></span>

### <span data-ttu-id="63753-105">Removeıfgdefaultset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63753-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63753-106">Removeınstancefailovergroupbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="63753-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63753-107">Removeınstancefailovergroupbyazurestarınstancefailovergroupmodelset</span><span class="sxs-lookup"><span data-stu-id="63753-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63753-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="63753-108">DESCRIPTION</span></span>
<span data-ttu-id="63753-109">Bu komut, belirtilen ada sahip örnek yük devretme grubunu kaldırır ve tüm veritabanlarını aynen bırakır.</span><span class="sxs-lookup"><span data-stu-id="63753-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="63753-110">DNS 'den dinleyici uç noktasının kaydı silinir.</span><span class="sxs-lookup"><span data-stu-id="63753-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="63753-111">Örneği yürütmek için örnek yük devretme grubunun birincil bölgesi kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="63753-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="63753-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63753-112">EXAMPLES</span></span>

### <span data-ttu-id="63753-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63753-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="63753-114">Örnek yük devretme grubunu kaldırma.</span><span class="sxs-lookup"><span data-stu-id="63753-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="63753-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63753-115">PARAMETERS</span></span>

### <span data-ttu-id="63753-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63753-116">-DefaultProfile</span></span>
<span data-ttu-id="63753-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63753-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63753-118">-Force</span><span class="sxs-lookup"><span data-stu-id="63753-118">-Force</span></span>
<span data-ttu-id="63753-119">Eylemi gerçekleştirmek için onay iletisini atlayın.</span><span class="sxs-lookup"><span data-stu-id="63753-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="63753-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63753-120">-InputObject</span></span>
<span data-ttu-id="63753-121">Kaldırılacak örnek yük devretme grubu nesnesi</span><span class="sxs-lookup"><span data-stu-id="63753-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63753-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="63753-122">-Location</span></span>
<span data-ttu-id="63753-123">Örnek yük devretme grubunun alınacağı yerel bölgenin adı.</span><span class="sxs-lookup"><span data-stu-id="63753-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63753-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="63753-124">-Name</span></span>
<span data-ttu-id="63753-125">Kaldırılacak örnek yük devretme grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="63753-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63753-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="63753-126">-PassThru</span></span>
<span data-ttu-id="63753-127">Cmdlet yürütme çıkışının geçirileceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="63753-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="63753-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63753-128">-ResourceGroupName</span></span>
<span data-ttu-id="63753-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="63753-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63753-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="63753-130">-ResourceId</span></span>
<span data-ttu-id="63753-131">Kaldırılacak örnek yük devretme grubunun kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="63753-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63753-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="63753-132">-Confirm</span></span>
<span data-ttu-id="63753-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="63753-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63753-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63753-134">-WhatIf</span></span>
<span data-ttu-id="63753-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63753-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63753-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="63753-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63753-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63753-137">CommonParameters</span></span>
<span data-ttu-id="63753-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63753-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63753-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="63753-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63753-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63753-140">INPUTS</span></span>

### <span data-ttu-id="63753-141">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="63753-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="63753-142">System. String</span><span class="sxs-lookup"><span data-stu-id="63753-142">System.String</span></span>

## <span data-ttu-id="63753-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63753-143">OUTPUTS</span></span>

### <span data-ttu-id="63753-144">Microsoft. Azure. Commands. Sql. ınstancefailovergroup. model. azures, ınstancefailovergroupmodel</span><span class="sxs-lookup"><span data-stu-id="63753-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="63753-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63753-145">NOTES</span></span>

## <span data-ttu-id="63753-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63753-146">RELATED LINKS</span></span>
