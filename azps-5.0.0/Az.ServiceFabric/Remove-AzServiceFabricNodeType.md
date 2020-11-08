---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279938"
---
# <span data-ttu-id="35f8f-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="35f8f-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="35f8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="35f8f-103">Bir kümeden tam bir düğüm türü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="35f8f-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="35f8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35f8f-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f8f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="35f8f-105">DESCRIPTION</span></span>
<span data-ttu-id="35f8f-106">**Remove-AzServiceFabricNodeType** kullanarak belirli bir düğüm türünden tüm düğümleri ve bir kümeden düğüm türünü kaldırın.</span><span class="sxs-lookup"><span data-stu-id="35f8f-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="35f8f-107">Bu komut, birincil düğüm türünü silmek için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="35f8f-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="35f8f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35f8f-108">EXAMPLES</span></span>

### <span data-ttu-id="35f8f-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="35f8f-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="35f8f-110">Bu komut, kümenizdeki ' NT1 ' NodeType öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="35f8f-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="35f8f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35f8f-111">PARAMETERS</span></span>

### <span data-ttu-id="35f8f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f8f-112">-DefaultProfile</span></span>
<span data-ttu-id="35f8f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35f8f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35f8f-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="35f8f-114">-Name</span></span>
<span data-ttu-id="35f8f-115">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="35f8f-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="35f8f-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="35f8f-116">-NodeType</span></span>
<span data-ttu-id="35f8f-117">Düğüm türü adı</span><span class="sxs-lookup"><span data-stu-id="35f8f-117">The node type name</span></span>

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

### <span data-ttu-id="35f8f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f8f-118">-ResourceGroupName</span></span>
<span data-ttu-id="35f8f-119">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="35f8f-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="35f8f-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="35f8f-120">-Confirm</span></span>
<span data-ttu-id="35f8f-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="35f8f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f8f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f8f-122">-WhatIf</span></span>
<span data-ttu-id="35f8f-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="35f8f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f8f-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="35f8f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f8f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f8f-125">CommonParameters</span></span>
<span data-ttu-id="35f8f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35f8f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f8f-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="35f8f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f8f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35f8f-128">INPUTS</span></span>

### <span data-ttu-id="35f8f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="35f8f-129">System.String</span></span>

## <span data-ttu-id="35f8f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35f8f-130">OUTPUTS</span></span>

### <span data-ttu-id="35f8f-131">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="35f8f-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="35f8f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35f8f-132">NOTES</span></span>

## <span data-ttu-id="35f8f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35f8f-133">RELATED LINKS</span></span>
