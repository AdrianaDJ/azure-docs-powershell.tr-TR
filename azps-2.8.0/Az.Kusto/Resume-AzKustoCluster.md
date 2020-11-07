---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: ce2fbe2f598ca6d08033c397a988f140379fda96
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751585"
---
# <span data-ttu-id="0240f-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="0240f-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="0240f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0240f-102">SYNOPSIS</span></span>
<span data-ttu-id="0240f-103">Askıya alınan bir kusto kümesini sürdürün.</span><span class="sxs-lookup"><span data-stu-id="0240f-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="0240f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0240f-104">SYNTAX</span></span>

### <span data-ttu-id="0240f-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0240f-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0240f-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0240f-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0240f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0240f-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0240f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0240f-108">DESCRIPTION</span></span>
<span data-ttu-id="0240f-109">Askıya alınan bir kusto kümesini sürdürün.</span><span class="sxs-lookup"><span data-stu-id="0240f-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="0240f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0240f-110">EXAMPLES</span></span>

### <span data-ttu-id="0240f-111">Örnek 1-askıya alınan bir kusto kümesini adla Sürdür</span><span class="sxs-lookup"><span data-stu-id="0240f-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="0240f-112">Yukarıdaki komut, "mykustocluster" kaynak grubunda bulunan "" adlı askıya alınmış kusto kümesini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="0240f-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="0240f-113">Örnek 2-askıya alınan bir kusto kümesini boruları kullanarak sürdürme</span><span class="sxs-lookup"><span data-stu-id="0240f-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="0240f-114">Yukarıdaki komut, cmdlet 'i kullanarak "mykustocluster" kaynak grubunda bulunan "" adlı kusto kümesini alır `Get-AzKustoCluster` ve sonra da sonucu `Resume-AzKustoCluster` devam ettirmek için buna yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="0240f-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="0240f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0240f-115">PARAMETERS</span></span>

### <span data-ttu-id="0240f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0240f-116">-DefaultProfile</span></span>
<span data-ttu-id="0240f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0240f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0240f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0240f-118">-InputObject</span></span>
<span data-ttu-id="0240f-119">Kusto küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0240f-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="0240f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0240f-120">-Name</span></span>
<span data-ttu-id="0240f-121">Devam edilecek kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="0240f-121">Name of cluster to be resume.</span></span>

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

### <span data-ttu-id="0240f-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0240f-122">-PassThru</span></span>
<span data-ttu-id="0240f-123">Belirtilen kümenin başarıyla sürdürülemez olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="0240f-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="0240f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0240f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0240f-125">Kümenin bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0240f-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0240f-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0240f-126">-ResourceId</span></span>
<span data-ttu-id="0240f-127">Kusto küme RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="0240f-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="0240f-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0240f-128">-Confirm</span></span>
<span data-ttu-id="0240f-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0240f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0240f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0240f-130">-WhatIf</span></span>
<span data-ttu-id="0240f-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0240f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0240f-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0240f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0240f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0240f-133">CommonParameters</span></span>
<span data-ttu-id="0240f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0240f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0240f-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0240f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0240f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0240f-136">INPUTS</span></span>

### <span data-ttu-id="0240f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0240f-137">System.String</span></span>

### <span data-ttu-id="0240f-138">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="0240f-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="0240f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0240f-139">OUTPUTS</span></span>

### <span data-ttu-id="0240f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0240f-140">System.Boolean</span></span>

## <span data-ttu-id="0240f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0240f-141">NOTES</span></span>

## <span data-ttu-id="0240f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0240f-142">RELATED LINKS</span></span>
