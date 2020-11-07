---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: d0de428417d59fc6103b9198265f4a38ad04dd52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759106"
---
# <span data-ttu-id="0be78-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="0be78-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="0be78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0be78-102">SYNOPSIS</span></span>
<span data-ttu-id="0be78-103">Bir kümeden tam bir düğüm türü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="0be78-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="0be78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0be78-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0be78-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0be78-105">DESCRIPTION</span></span>
<span data-ttu-id="0be78-106">**Remove-AzServiceFabricNodeType** kullanarak belirli bir düğüm türünden tüm düğümleri ve bir kümeden düğüm türünü kaldırın.</span><span class="sxs-lookup"><span data-stu-id="0be78-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="0be78-107">Bu komut, birincil düğüm türünü silmek için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="0be78-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="0be78-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0be78-108">EXAMPLES</span></span>

### <span data-ttu-id="0be78-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0be78-109">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="0be78-110">Bu komut, kümenizdeki ' NT1 ' NodeType öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0be78-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="0be78-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0be78-111">PARAMETERS</span></span>

### <span data-ttu-id="0be78-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be78-112">-DefaultProfile</span></span>
<span data-ttu-id="0be78-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0be78-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0be78-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="0be78-114">-Name</span></span>
<span data-ttu-id="0be78-115">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="0be78-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0be78-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0be78-116">-NodeType</span></span>
<span data-ttu-id="0be78-117">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="0be78-117">The node type name.</span></span>

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

### <span data-ttu-id="0be78-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be78-118">-ResourceGroupName</span></span>
<span data-ttu-id="0be78-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0be78-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0be78-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="0be78-120">-Confirm</span></span>
<span data-ttu-id="0be78-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0be78-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0be78-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0be78-122">-WhatIf</span></span>
<span data-ttu-id="0be78-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0be78-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0be78-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0be78-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0be78-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be78-125">CommonParameters</span></span>
<span data-ttu-id="0be78-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0be78-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be78-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0be78-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be78-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0be78-128">INPUTS</span></span>

### <span data-ttu-id="0be78-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0be78-129">System.String</span></span>

## <span data-ttu-id="0be78-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0be78-130">OUTPUTS</span></span>

### <span data-ttu-id="0be78-131">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0be78-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0be78-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0be78-132">NOTES</span></span>

## <span data-ttu-id="0be78-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0be78-133">RELATED LINKS</span></span>
