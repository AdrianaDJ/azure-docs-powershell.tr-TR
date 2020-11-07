---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: 687be1ddd20c431e5226fe7f0516cc480e79fce8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762444"
---
# <span data-ttu-id="788ed-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="788ed-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="788ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="788ed-102">SYNOPSIS</span></span>
<span data-ttu-id="788ed-103">Kümedeki belirli bir düğüme düğüm ekleme.</span><span class="sxs-lookup"><span data-stu-id="788ed-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="788ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="788ed-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="788ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="788ed-105">DESCRIPTION</span></span>
<span data-ttu-id="788ed-106">Belirli bir düğüm türüne düğüm eklemek için **Add-AzureRmServiceFabricNode** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="788ed-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="788ed-107">Yalnızca düğüm türüne eklemek istediğiniz düğüm sayısını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="788ed-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="788ed-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="788ed-108">EXAMPLES</span></span>

### <span data-ttu-id="788ed-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="788ed-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="788ed-110">Bu komut, ' N1 ' düğüm türüne 2 düğüm ekler.</span><span class="sxs-lookup"><span data-stu-id="788ed-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="788ed-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="788ed-111">PARAMETERS</span></span>

### <span data-ttu-id="788ed-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788ed-112">-DefaultProfile</span></span>
<span data-ttu-id="788ed-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="788ed-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788ed-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="788ed-114">-Name</span></span>
<span data-ttu-id="788ed-115">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="788ed-115">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="788ed-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="788ed-116">-NodeType</span></span>
<span data-ttu-id="788ed-117">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="788ed-117">Node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="788ed-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="788ed-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="788ed-119">VM örneği numarası.</span><span class="sxs-lookup"><span data-stu-id="788ed-119">VM instance number.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="788ed-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="788ed-120">-ResourceGroupName</span></span>
<span data-ttu-id="788ed-121">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="788ed-121">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="788ed-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="788ed-122">-Confirm</span></span>
<span data-ttu-id="788ed-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="788ed-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="788ed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788ed-124">-WhatIf</span></span>
<span data-ttu-id="788ed-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="788ed-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="788ed-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="788ed-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="788ed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788ed-127">CommonParameters</span></span>
<span data-ttu-id="788ed-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="788ed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788ed-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="788ed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788ed-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="788ed-130">INPUTS</span></span>

### <span data-ttu-id="788ed-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="788ed-131">System.Int32</span></span>
<span data-ttu-id="788ed-132">Parametreler: NumberOfNodesToAdd (ByValue)</span><span class="sxs-lookup"><span data-stu-id="788ed-132">Parameters: NumberOfNodesToAdd (ByValue)</span></span>

### <span data-ttu-id="788ed-133">System. String</span><span class="sxs-lookup"><span data-stu-id="788ed-133">System.String</span></span>
<span data-ttu-id="788ed-134">Parametreler: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="788ed-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="788ed-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="788ed-135">OUTPUTS</span></span>

### <span data-ttu-id="788ed-136">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="788ed-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="788ed-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="788ed-137">NOTES</span></span>

## <span data-ttu-id="788ed-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="788ed-138">RELATED LINKS</span></span>

[<span data-ttu-id="788ed-139">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="788ed-139">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
