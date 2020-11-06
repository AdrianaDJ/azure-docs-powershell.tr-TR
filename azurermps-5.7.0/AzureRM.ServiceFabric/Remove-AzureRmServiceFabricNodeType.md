---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: f825d1ba1621a00be6196219d99dc188496ea5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587429"
---
# <span data-ttu-id="018db-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="018db-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="018db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="018db-102">SYNOPSIS</span></span>
<span data-ttu-id="018db-103">Bir kümeden tam bir düğüm türü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="018db-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="018db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="018db-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="018db-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="018db-105">DESCRIPTION</span></span>
<span data-ttu-id="018db-106">**Remove-AzureRmServiceFabricNodeType** öğesini kullanarak belirli bir düğüm türünden tüm düğümleri ve bir kümeden düğüm türünü kaldırın.</span><span class="sxs-lookup"><span data-stu-id="018db-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="018db-107">Bu komut, birincil düğüm türünü silmek için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="018db-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="018db-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="018db-108">EXAMPLES</span></span>

### <span data-ttu-id="018db-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="018db-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="018db-110">Bu komut, kümenizdeki ' NT1 ' NodeType öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="018db-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="018db-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="018db-111">PARAMETERS</span></span>

### <span data-ttu-id="018db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018db-112">-DefaultProfile</span></span>
<span data-ttu-id="018db-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="018db-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="018db-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="018db-114">-Name</span></span>
<span data-ttu-id="018db-115">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="018db-115">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="018db-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="018db-116">-NodeType</span></span>
<span data-ttu-id="018db-117">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="018db-117">The node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="018db-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018db-118">-ResourceGroupName</span></span>
<span data-ttu-id="018db-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="018db-119">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="018db-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="018db-120">-Confirm</span></span>
<span data-ttu-id="018db-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="018db-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="018db-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="018db-122">-WhatIf</span></span>
<span data-ttu-id="018db-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="018db-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="018db-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="018db-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="018db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018db-125">CommonParameters</span></span>
<span data-ttu-id="018db-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="018db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018db-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="018db-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018db-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="018db-128">INPUTS</span></span>

### <span data-ttu-id="018db-129">System. String</span><span class="sxs-lookup"><span data-stu-id="018db-129">System.String</span></span>

## <span data-ttu-id="018db-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="018db-130">OUTPUTS</span></span>

### <span data-ttu-id="018db-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="018db-131">System.Object</span></span>

## <span data-ttu-id="018db-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="018db-132">NOTES</span></span>

## <span data-ttu-id="018db-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="018db-133">RELATED LINKS</span></span>

