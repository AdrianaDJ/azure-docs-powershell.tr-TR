---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/suspend-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Suspend-AzKustoCluster.md
ms.openlocfilehash: 17c730fb65e50aeeff33e616b7be596745d67ac0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096600"
---
# <span data-ttu-id="8abf9-101">Suspend-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8abf9-101">Suspend-AzKustoCluster</span></span>

## <span data-ttu-id="8abf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8abf9-102">SYNOPSIS</span></span>
<span data-ttu-id="8abf9-103">Var olan kusto kümesini askıya alma.</span><span class="sxs-lookup"><span data-stu-id="8abf9-103">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="8abf9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8abf9-104">SYNTAX</span></span>

### <span data-ttu-id="8abf9-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8abf9-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8abf9-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="8abf9-106">ByResourceId</span></span>
```
Suspend-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8abf9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8abf9-107">ByInputObject</span></span>
```
Suspend-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8abf9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8abf9-108">DESCRIPTION</span></span>
<span data-ttu-id="8abf9-109">Var olan kusto kümesini askıya alma.</span><span class="sxs-lookup"><span data-stu-id="8abf9-109">Suspend an existing Kusto cluster.</span></span>

## <span data-ttu-id="8abf9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8abf9-110">EXAMPLES</span></span>

### <span data-ttu-id="8abf9-111">Örnek 1-varolan bir kusto kümesini adla askıya alma</span><span class="sxs-lookup"><span data-stu-id="8abf9-111">Example 1 - Suspend an existing Kusto cluster by name</span></span>

```
PS C:\> Suspend-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="8abf9-112">Yukarıdaki komut, "testrg" kaynak grubunda bulunan "mykustocluster" adlı kusto kümesini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="8abf9-112">The above command suspends the Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="8abf9-113">Örnek 2-varolan bir kusto kümesini boruları kullanarak askıya alma</span><span class="sxs-lookup"><span data-stu-id="8abf9-113">Example 2 - Suspend an existing Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Suspend-AzKustoCluster
```

<span data-ttu-id="8abf9-114">Yukarıdaki komut, cmdlet 'i kullanarak "mykustocluster" kaynak grubunda bulunan "" adlı kusto kümesini alır `Get-AzKustoCluster` ve sonra da sonucu askıya almak için yol gösterir `Suspend-AzKustoCluster` .</span><span class="sxs-lookup"><span data-stu-id="8abf9-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Suspend-AzKustoCluster` to suspend it.</span></span>

## <span data-ttu-id="8abf9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8abf9-115">PARAMETERS</span></span>

### <span data-ttu-id="8abf9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8abf9-116">-DefaultProfile</span></span>
<span data-ttu-id="8abf9-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8abf9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8abf9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8abf9-118">-InputObject</span></span>
<span data-ttu-id="8abf9-119">Kusto küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8abf9-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="8abf9-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="8abf9-120">-Name</span></span>
<span data-ttu-id="8abf9-121">Askıya alınacak kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="8abf9-121">Name of cluster to be suspend.</span></span>

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

### <span data-ttu-id="8abf9-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8abf9-122">-PassThru</span></span>
<span data-ttu-id="8abf9-123">Belirtilen kümenin başarıyla askıya alınıp alınmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="8abf9-123">Return whether the specified cluster was successfully suspended or not.</span></span>

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

### <span data-ttu-id="8abf9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8abf9-124">-ResourceGroupName</span></span>
<span data-ttu-id="8abf9-125">Kümenin bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8abf9-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="8abf9-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8abf9-126">-ResourceId</span></span>
<span data-ttu-id="8abf9-127">Kusto küme RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="8abf9-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="8abf9-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="8abf9-128">-Confirm</span></span>
<span data-ttu-id="8abf9-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8abf9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8abf9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8abf9-130">-WhatIf</span></span>
<span data-ttu-id="8abf9-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8abf9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8abf9-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8abf9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8abf9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8abf9-133">CommonParameters</span></span>
<span data-ttu-id="8abf9-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8abf9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8abf9-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8abf9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8abf9-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8abf9-136">INPUTS</span></span>

### <span data-ttu-id="8abf9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8abf9-137">System.String</span></span>

### <span data-ttu-id="8abf9-138">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8abf9-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="8abf9-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8abf9-139">OUTPUTS</span></span>

### <span data-ttu-id="8abf9-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8abf9-140">System.Boolean</span></span>

## <span data-ttu-id="8abf9-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8abf9-141">NOTES</span></span>

## <span data-ttu-id="8abf9-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8abf9-142">RELATED LINKS</span></span>
