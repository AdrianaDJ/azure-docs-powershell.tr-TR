---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 36cad62f67be4273d363277e52f4dc8d2c91373c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593648"
---
# <span data-ttu-id="c57e3-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="c57e3-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="c57e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c57e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c57e3-103">Bir kümeden tam bir düğüm türü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c57e3-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c57e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c57e3-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c57e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c57e3-105">DESCRIPTION</span></span>
<span data-ttu-id="c57e3-106">**Remove-AzureRmServiceFabricNodeType** öğesini kullanarak belirli bir düğüm türünden tüm düğümleri ve bir kümeden düğüm türünü kaldırın.</span><span class="sxs-lookup"><span data-stu-id="c57e3-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="c57e3-107">Bu komut, birincil düğüm türünü silmek için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="c57e3-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="c57e3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c57e3-108">EXAMPLES</span></span>

### <span data-ttu-id="c57e3-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c57e3-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="c57e3-110">Bu komut, kümenizdeki ' NT1 ' NodeType öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c57e3-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="c57e3-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c57e3-111">PARAMETERS</span></span>

### <span data-ttu-id="c57e3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c57e3-112">-DefaultProfile</span></span>
<span data-ttu-id="c57e3-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c57e3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c57e3-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="c57e3-114">-Name</span></span>
<span data-ttu-id="c57e3-115">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c57e3-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c57e3-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c57e3-116">-NodeType</span></span>
<span data-ttu-id="c57e3-117">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="c57e3-117">The node type name.</span></span>

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

### <span data-ttu-id="c57e3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c57e3-118">-ResourceGroupName</span></span>
<span data-ttu-id="c57e3-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c57e3-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c57e3-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="c57e3-120">-Confirm</span></span>
<span data-ttu-id="c57e3-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c57e3-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c57e3-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c57e3-122">-WhatIf</span></span>
<span data-ttu-id="c57e3-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c57e3-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c57e3-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c57e3-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c57e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c57e3-125">CommonParameters</span></span>
<span data-ttu-id="c57e3-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c57e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c57e3-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c57e3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c57e3-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c57e3-128">INPUTS</span></span>

### <span data-ttu-id="c57e3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c57e3-129">System.String</span></span>
<span data-ttu-id="c57e3-130">Parametreler: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c57e3-130">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="c57e3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c57e3-131">OUTPUTS</span></span>

### <span data-ttu-id="c57e3-132">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c57e3-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c57e3-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c57e3-133">NOTES</span></span>

## <span data-ttu-id="c57e3-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c57e3-134">RELATED LINKS</span></span>
