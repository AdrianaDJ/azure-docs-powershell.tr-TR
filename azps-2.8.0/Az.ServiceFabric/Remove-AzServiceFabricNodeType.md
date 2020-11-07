---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: b83e6738ec16b8f2700f71e066430148332ca3ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932418"
---
# <span data-ttu-id="fa6ae-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="fa6ae-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="fa6ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="fa6ae-103">Bir kümeden tam bir düğüm türü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="fa6ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa6ae-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa6ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa6ae-105">DESCRIPTION</span></span>
<span data-ttu-id="fa6ae-106">**Remove-AzServiceFabricNodeType** kullanarak belirli bir düğüm türünden tüm düğümleri ve bir kümeden düğüm türünü kaldırın.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="fa6ae-107">Bu komut, birincil düğüm türünü silmek için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="fa6ae-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa6ae-108">EXAMPLES</span></span>

### <span data-ttu-id="fa6ae-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fa6ae-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="fa6ae-110">Bu komut, kümenizdeki ' NT1 ' NodeType öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="fa6ae-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa6ae-111">PARAMETERS</span></span>

### <span data-ttu-id="fa6ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa6ae-112">-DefaultProfile</span></span>
<span data-ttu-id="fa6ae-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa6ae-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa6ae-114">-Name</span></span>
<span data-ttu-id="fa6ae-115">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="fa6ae-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="fa6ae-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="fa6ae-116">-NodeType</span></span>
<span data-ttu-id="fa6ae-117">Düğüm türü adı</span><span class="sxs-lookup"><span data-stu-id="fa6ae-117">The node type name</span></span>

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

### <span data-ttu-id="fa6ae-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa6ae-118">-ResourceGroupName</span></span>
<span data-ttu-id="fa6ae-119">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="fa6ae-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa6ae-120">-Confirm</span></span>
<span data-ttu-id="fa6ae-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa6ae-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa6ae-122">-WhatIf</span></span>
<span data-ttu-id="fa6ae-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa6ae-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa6ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa6ae-125">CommonParameters</span></span>
<span data-ttu-id="fa6ae-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa6ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa6ae-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa6ae-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa6ae-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa6ae-128">INPUTS</span></span>

### <span data-ttu-id="fa6ae-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fa6ae-129">System.String</span></span>

## <span data-ttu-id="fa6ae-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa6ae-130">OUTPUTS</span></span>

### <span data-ttu-id="fa6ae-131">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fa6ae-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fa6ae-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa6ae-132">NOTES</span></span>

## <span data-ttu-id="fa6ae-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa6ae-133">RELATED LINKS</span></span>
