---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: aca27be11fde78df8abad1d7cdcfeff4232b60d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763615"
---
# <span data-ttu-id="a8d5a-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a8d5a-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="a8d5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d5a-103">Kümedeki belirli bir düğüme düğüm ekleme.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8d5a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a8d5a-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToAdd <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8d5a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a8d5a-105">DESCRIPTION</span></span>
<span data-ttu-id="a8d5a-106">Belirli bir düğüm türüne düğüm eklemek için **Add-AzureRmServiceFabricNode** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="a8d5a-107">Yalnızca düğüm türüne eklemek istediğiniz düğüm sayısını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="a8d5a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a8d5a-108">EXAMPLES</span></span>

### <span data-ttu-id="a8d5a-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a8d5a-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="a8d5a-110">Bu komut, ' N1 ' düğüm türüne 2 düğüm ekler.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="a8d5a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a8d5a-111">PARAMETERS</span></span>

### <span data-ttu-id="a8d5a-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="a8d5a-112">-Name</span></span>
<span data-ttu-id="a8d5a-113">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a8d5a-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="a8d5a-114">-NodeType</span></span>
<span data-ttu-id="a8d5a-115">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-115">Node type name.</span></span>

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

### <span data-ttu-id="a8d5a-116">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="a8d5a-116">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="a8d5a-117">VM örneği numarası.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-117">VM instance number.</span></span>

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

### <span data-ttu-id="a8d5a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8d5a-118">-ResourceGroupName</span></span>
<span data-ttu-id="a8d5a-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a8d5a-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="a8d5a-120">-Confirm</span></span>
<span data-ttu-id="a8d5a-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8d5a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8d5a-122">-WhatIf</span></span>
<span data-ttu-id="a8d5a-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8d5a-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8d5a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d5a-125">-DefaultProfile</span></span>
<span data-ttu-id="a8d5a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8d5a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d5a-127">CommonParameters</span></span>
<span data-ttu-id="a8d5a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a8d5a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d5a-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8d5a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d5a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a8d5a-130">INPUTS</span></span>

### <span data-ttu-id="a8d5a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a8d5a-131">System.String</span></span>

## <span data-ttu-id="a8d5a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a8d5a-132">OUTPUTS</span></span>

### <span data-ttu-id="a8d5a-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="a8d5a-133">System.Object</span></span>

## <span data-ttu-id="a8d5a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a8d5a-134">NOTES</span></span>

## <span data-ttu-id="a8d5a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a8d5a-135">RELATED LINKS</span></span>

[<span data-ttu-id="a8d5a-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="a8d5a-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
