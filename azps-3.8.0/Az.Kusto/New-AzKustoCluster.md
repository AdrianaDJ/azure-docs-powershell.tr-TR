---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9c18597da52900794e5f891fb06385249c173a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096610"
---
# <span data-ttu-id="5eef1-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="5eef1-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="5eef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eef1-102">SYNOPSIS</span></span>
<span data-ttu-id="5eef1-103">Yeni bir kusto kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5eef1-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="5eef1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5eef1-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5eef1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5eef1-105">DESCRIPTION</span></span>
<span data-ttu-id="5eef1-106">Yeni bir kusto kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5eef1-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="5eef1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5eef1-107">EXAMPLES</span></span>

### <span data-ttu-id="5eef1-108">Örnek 1-yeni kusto kümesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="5eef1-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="5eef1-109">Yukarıdaki komut, "testrg" kaynak grubunda "mykustocluster" adlı yeni bir kusto kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5eef1-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="5eef1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5eef1-110">PARAMETERS</span></span>

### <span data-ttu-id="5eef1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eef1-111">-DefaultProfile</span></span>
<span data-ttu-id="5eef1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5eef1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5eef1-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="5eef1-113">-Location</span></span>
<span data-ttu-id="5eef1-114">Kümenin oluşturulması gereken Azure bölgesi.</span><span class="sxs-lookup"><span data-stu-id="5eef1-114">Azure region where the cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5eef1-115">-Name</span></span>
<span data-ttu-id="5eef1-116">Oluşturulacak kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="5eef1-116">Name of the cluster to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eef1-117">-ResourceGroupName</span></span>
<span data-ttu-id="5eef1-118">Kümeyi oluşturmak istediğiniz kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5eef1-118">Name of resource group under which you want to create the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="5eef1-119">-Sku</span></span>
<span data-ttu-id="5eef1-120">Kümeyi oluşturmak için kullanılan SKU adı</span><span class="sxs-lookup"><span data-stu-id="5eef1-120">Name of the Sku used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-121">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5eef1-121">-Tag</span></span>
<span data-ttu-id="5eef1-122">Bu kümeyle ilişkilendirilmiş etiketlerin dize sözlüğü</span><span class="sxs-lookup"><span data-stu-id="5eef1-122">A string,string dictionary of tags associated with this cluster</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-123">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="5eef1-123">-Tier</span></span>
<span data-ttu-id="5eef1-124">Kümeyi oluşturmak için kullanılan katmanın adı</span><span class="sxs-lookup"><span data-stu-id="5eef1-124">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eef1-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="5eef1-125">-Confirm</span></span>
<span data-ttu-id="5eef1-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5eef1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eef1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eef1-127">-WhatIf</span></span>
<span data-ttu-id="5eef1-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5eef1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eef1-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5eef1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eef1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eef1-130">CommonParameters</span></span>
<span data-ttu-id="5eef1-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5eef1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eef1-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eef1-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eef1-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5eef1-133">INPUTS</span></span>

### <span data-ttu-id="5eef1-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5eef1-134">None</span></span>

## <span data-ttu-id="5eef1-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5eef1-135">OUTPUTS</span></span>

### <span data-ttu-id="5eef1-136">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="5eef1-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="5eef1-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5eef1-137">NOTES</span></span>

## <span data-ttu-id="5eef1-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5eef1-138">RELATED LINKS</span></span>
