---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstancePool.md
ms.openlocfilehash: b10187938613f9ab6e0c12cb0d83162450be8445
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098423"
---
# <span data-ttu-id="3e172-101">Remove-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="3e172-101">Remove-AzSqlInstancePool</span></span>

## <span data-ttu-id="3e172-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e172-102">SYNOPSIS</span></span>
<span data-ttu-id="3e172-103">Azure SQL örneği havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3e172-103">Removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="3e172-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e172-104">SYNTAX</span></span>

### <span data-ttu-id="3e172-105">DeleteByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3e172-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e172-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e172-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e172-107">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3e172-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e172-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e172-108">DESCRIPTION</span></span>
<span data-ttu-id="3e172-109">**Remove-Azsqlınstancepool** cmdlet 'ı BIR Azure SQL örnek havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3e172-109">The **Remove-AzSqlInstancePool** cmdlet removes an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="3e172-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e172-110">EXAMPLES</span></span>

### <span data-ttu-id="3e172-111">Örnek 1: örnek havuzunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="3e172-111">Example 1: Remove an instance pool</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
```

### <span data-ttu-id="3e172-112">Örnek 2: kaynak tanımlayıcısına göre örnek havuzunu kaldırma</span><span class="sxs-lookup"><span data-stu-id="3e172-112">Example 2: Remove an instance pool by its resource identifier</span></span>
```powershell
PS C:\> Remove-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
```

### <span data-ttu-id="3e172-113">Örnek 3: örnek havuz nesnesiyle örnek havuzu kaldırma</span><span class="sxs-lookup"><span data-stu-id="3e172-113">Example 3: Remove an instance pool by an instance pool object</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroup resourcegroup01 -Name instancePool0
PS C:\> Remove-AzSqlInstancePool -InputObject $instancePool
```

<span data-ttu-id="3e172-114">Bu komut, instancePool0 adlı bir örnek havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3e172-114">This command removes an instance pool named instancePool0.</span></span>

## <span data-ttu-id="3e172-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e172-115">PARAMETERS</span></span>

### <span data-ttu-id="3e172-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e172-116">-DefaultProfile</span></span>
<span data-ttu-id="3e172-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e172-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e172-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e172-118">-InputObject</span></span>
<span data-ttu-id="3e172-119">Kaldırılacak örnek havuzu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3e172-119">The instance pool object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e172-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e172-120">-Name</span></span>
<span data-ttu-id="3e172-121">Örnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="3e172-121">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e172-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e172-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e172-123">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3e172-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e172-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3e172-124">-ResourceId</span></span>
<span data-ttu-id="3e172-125">Kaldırılacak örnek havuzu kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3e172-125">The instance pool resource id to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e172-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e172-126">-Confirm</span></span>
<span data-ttu-id="3e172-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e172-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e172-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e172-128">-WhatIf</span></span>
<span data-ttu-id="3e172-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e172-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e172-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e172-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e172-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e172-131">CommonParameters</span></span>
<span data-ttu-id="3e172-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e172-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e172-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3e172-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e172-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e172-134">INPUTS</span></span>

### <span data-ttu-id="3e172-135">Microsoft.Azure.Commands.Sql.Instance_Pools. model. azures, ınstancepoolmodel</span><span class="sxs-lookup"><span data-stu-id="3e172-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="3e172-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3e172-136">System.String</span></span>

## <span data-ttu-id="3e172-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e172-137">OUTPUTS</span></span>

### <span data-ttu-id="3e172-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="3e172-138">System.Object</span></span>
## <span data-ttu-id="3e172-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e172-139">NOTES</span></span>

## <span data-ttu-id="3e172-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e172-140">RELATED LINKS</span></span>
