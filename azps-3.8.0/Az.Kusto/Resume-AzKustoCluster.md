---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/resume-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Resume-AzKustoCluster.md
ms.openlocfilehash: 94e5525b1d783eea794b7e98e76e809b9d7e0f3b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096601"
---
# <span data-ttu-id="79e59-101">Resume-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="79e59-101">Resume-AzKustoCluster</span></span>

## <span data-ttu-id="79e59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e59-102">SYNOPSIS</span></span>
<span data-ttu-id="79e59-103">Askıya alınan bir kusto kümesini sürdürün.</span><span class="sxs-lookup"><span data-stu-id="79e59-103">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="79e59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79e59-104">SYNTAX</span></span>

### <span data-ttu-id="79e59-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79e59-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzKustoCluster [[-ResourceGroupName] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e59-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="79e59-106">ByResourceId</span></span>
```
Resume-AzKustoCluster [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e59-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="79e59-107">ByInputObject</span></span>
```
Resume-AzKustoCluster [-InputObject] <PSKustoCluster> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79e59-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="79e59-108">DESCRIPTION</span></span>
<span data-ttu-id="79e59-109">Askıya alınan bir kusto kümesini sürdürün.</span><span class="sxs-lookup"><span data-stu-id="79e59-109">Resume a suspended Kusto cluster.</span></span>

## <span data-ttu-id="79e59-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79e59-110">EXAMPLES</span></span>

### <span data-ttu-id="79e59-111">Örnek 1-askıya alınan bir kusto kümesini adla Sürdür</span><span class="sxs-lookup"><span data-stu-id="79e59-111">Example 1 - Resume a suspended Kusto cluster by name</span></span>

```
PS C:\> Resume-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster
```

<span data-ttu-id="79e59-112">Yukarıdaki komut, "mykustocluster" kaynak grubunda bulunan "" adlı askıya alınmış kusto kümesini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="79e59-112">The above command resumes the suspended Kusto cluster named "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="79e59-113">Örnek 2-askıya alınan bir kusto kümesini boruları kullanarak sürdürme</span><span class="sxs-lookup"><span data-stu-id="79e59-113">Example 2 - Resume a suspended Kusto cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Resume-AzKustoCluster
```

<span data-ttu-id="79e59-114">Yukarıdaki komut, cmdlet 'i kullanarak "mykustocluster" kaynak grubunda bulunan "" adlı kusto kümesini alır `Get-AzKustoCluster` ve sonra da sonucu `Resume-AzKustoCluster` devam ettirmek için buna yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="79e59-114">The above command gets the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Resume-AzKustoCluster` to resume it.</span></span>

## <span data-ttu-id="79e59-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79e59-115">PARAMETERS</span></span>

### <span data-ttu-id="79e59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e59-116">-DefaultProfile</span></span>
<span data-ttu-id="79e59-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79e59-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79e59-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79e59-118">-InputObject</span></span>
<span data-ttu-id="79e59-119">Kusto küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="79e59-119">Kusto cluster object.</span></span>

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

### <span data-ttu-id="79e59-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="79e59-120">-Name</span></span>
<span data-ttu-id="79e59-121">Devam edilecek kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="79e59-121">Name of cluster to be resume.</span></span>

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

### <span data-ttu-id="79e59-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="79e59-122">-PassThru</span></span>
<span data-ttu-id="79e59-123">Belirtilen kümenin başarıyla sürdürülemez olup olmadığını döndürün.</span><span class="sxs-lookup"><span data-stu-id="79e59-123">Return whether the specified cluster was successfully resumed or not.</span></span>

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

### <span data-ttu-id="79e59-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e59-124">-ResourceGroupName</span></span>
<span data-ttu-id="79e59-125">Kümenin bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="79e59-125">Name of resource group under which the cluster exists.</span></span>

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

### <span data-ttu-id="79e59-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="79e59-126">-ResourceId</span></span>
<span data-ttu-id="79e59-127">Kusto küme RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="79e59-127">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="79e59-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="79e59-128">-Confirm</span></span>
<span data-ttu-id="79e59-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79e59-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79e59-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e59-130">-WhatIf</span></span>
<span data-ttu-id="79e59-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79e59-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79e59-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79e59-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79e59-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e59-133">CommonParameters</span></span>
<span data-ttu-id="79e59-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79e59-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e59-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79e59-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e59-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79e59-136">INPUTS</span></span>

### <span data-ttu-id="79e59-137">System. String</span><span class="sxs-lookup"><span data-stu-id="79e59-137">System.String</span></span>

### <span data-ttu-id="79e59-138">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="79e59-138">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="79e59-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79e59-139">OUTPUTS</span></span>

### <span data-ttu-id="79e59-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79e59-140">System.Boolean</span></span>

## <span data-ttu-id="79e59-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79e59-141">NOTES</span></span>

## <span data-ttu-id="79e59-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79e59-142">RELATED LINKS</span></span>