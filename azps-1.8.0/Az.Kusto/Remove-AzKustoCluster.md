---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoCluster.md
ms.openlocfilehash: 3556ff99dafe804ab78899f8b0eefc64db4ca82b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916155"
---
# <span data-ttu-id="3c8a3-101">Remove-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3c8a3-101">Remove-AzKustoCluster</span></span>

## <span data-ttu-id="3c8a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="3c8a3-103">Var olan bir kusto kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-103">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="3c8a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c8a3-104">SYNTAX</span></span>

### <span data-ttu-id="3c8a3-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3c8a3-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c8a3-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="3c8a3-106">ByResourceId</span></span>
```
Remove-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c8a3-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c8a3-107">ByInputObject</span></span>
```
Remove-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c8a3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c8a3-108">DESCRIPTION</span></span>
<span data-ttu-id="3c8a3-109">Var olan bir kusto kümesini siler.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-109">Deletes an existing Kusto cluster.</span></span>

## <span data-ttu-id="3c8a3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c8a3-110">EXAMPLES</span></span>

### <span data-ttu-id="3c8a3-111">Örnek 1-varolan bir kusto kümesini adla silme</span><span class="sxs-lookup"><span data-stu-id="3c8a3-111">Example 1 - Delete an existing Kusto cluster by name</span></span>

```
PS C:\> Remove-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="3c8a3-112">Yukarıdaki komut "mykustocluster" adlı kusto kümesini "testrg" kaynak grubunda siler.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-112">The above command deletes the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="3c8a3-113">Örnek 2-şeridi kullanarak mevcut bir kusto kümesini silme</span><span class="sxs-lookup"><span data-stu-id="3c8a3-113">Example 2 - Delete an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Remove-AzKustoCluster
```

<span data-ttu-id="3c8a3-114">Yukarıdaki komut, cmdlet 'i kullanarak "mykustocluster" kaynak grubundaki "" adlı kusto kümesini alır `Get-AzKustoCluster` ve sonra da sonucu `Remove-AzKustoCluster` silmek için bunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-114">The above command gets the Kusto cluster named "mykustocluster" in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Remove-AzKustoCluster` to delete it.</span></span>

## <span data-ttu-id="3c8a3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c8a3-115">PARAMETERS</span></span>

### <span data-ttu-id="3c8a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c8a3-116">-DefaultProfile</span></span>
<span data-ttu-id="3c8a3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c8a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c8a3-118">-InputObject</span></span>
<span data-ttu-id="3c8a3-119">Kusto küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-119">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c8a3-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c8a3-120">-Name</span></span>
<span data-ttu-id="3c8a3-121">Kaldırılacak kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-121">Name of cluster to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8a3-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3c8a3-122">-PassThru</span></span>
<span data-ttu-id="3c8a3-123">Belirtilen kümenin başarıyla silinip silinmediğini döndürün.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-123">Return whether the specified cluster was successfully deleted or not.</span></span>

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

### <span data-ttu-id="3c8a3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c8a3-124">-ResourceGroupName</span></span>
<span data-ttu-id="3c8a3-125">Kümenin bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c8a3-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3c8a3-126">-ResourceId</span></span>
<span data-ttu-id="3c8a3-127">Kusto küme RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c8a3-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c8a3-128">-Confirm</span></span>
<span data-ttu-id="3c8a3-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c8a3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c8a3-130">-WhatIf</span></span>
<span data-ttu-id="3c8a3-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c8a3-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c8a3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c8a3-133">CommonParameters</span></span>
<span data-ttu-id="3c8a3-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c8a3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c8a3-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c8a3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c8a3-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c8a3-136">INPUTS</span></span>

### <span data-ttu-id="3c8a3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3c8a3-137">System.String</span></span>

### <span data-ttu-id="3c8a3-138">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3c8a3-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="3c8a3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c8a3-139">OUTPUTS</span></span>

### <span data-ttu-id="3c8a3-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c8a3-140">System.Boolean</span></span>

## <span data-ttu-id="3c8a3-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c8a3-141">NOTES</span></span>

## <span data-ttu-id="3c8a3-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c8a3-142">RELATED LINKS</span></span>