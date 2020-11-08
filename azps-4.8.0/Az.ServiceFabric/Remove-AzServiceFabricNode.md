---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 3580315755792aaaddf3b10e185413254784a3d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273950"
---
# <span data-ttu-id="95795-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="95795-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="95795-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95795-102">SYNOPSIS</span></span>
<span data-ttu-id="95795-103">Belirli düğüm türünden düğümleri kümeden kaldırma.</span><span class="sxs-lookup"><span data-stu-id="95795-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="95795-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95795-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95795-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="95795-105">DESCRIPTION</span></span>
<span data-ttu-id="95795-106">Bir kümeden belirli bir düğüm türünden düğümleri kaldırmak için **Remove-AzServiceFabricNode** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="95795-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="95795-107">Kaldırma işlemi yalnızca küme durumu ölçümlerine uyuyorsa devam eder.</span><span class="sxs-lookup"><span data-stu-id="95795-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="95795-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95795-108">EXAMPLES</span></span>

### <span data-ttu-id="95795-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="95795-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="95795-110">Bu komut, ' NT1 ' NodeType 'daki 2 düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="95795-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="95795-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95795-111">PARAMETERS</span></span>

### <span data-ttu-id="95795-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95795-112">-DefaultProfile</span></span>
<span data-ttu-id="95795-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95795-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95795-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="95795-114">-Name</span></span>
<span data-ttu-id="95795-115">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="95795-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="95795-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="95795-116">-NodeType</span></span>
<span data-ttu-id="95795-117">Düğüm türü adı</span><span class="sxs-lookup"><span data-stu-id="95795-117">Node type name</span></span>

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

### <span data-ttu-id="95795-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="95795-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="95795-119">Eklenecek düğümlerin sayısı</span><span class="sxs-lookup"><span data-stu-id="95795-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="95795-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95795-120">-ResourceGroupName</span></span>
<span data-ttu-id="95795-121">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="95795-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="95795-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="95795-122">-Confirm</span></span>
<span data-ttu-id="95795-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95795-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95795-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95795-124">-WhatIf</span></span>
<span data-ttu-id="95795-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="95795-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95795-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="95795-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95795-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95795-127">CommonParameters</span></span>
<span data-ttu-id="95795-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95795-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95795-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="95795-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95795-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95795-130">INPUTS</span></span>

### <span data-ttu-id="95795-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="95795-131">System.Int32</span></span>

### <span data-ttu-id="95795-132">System. String</span><span class="sxs-lookup"><span data-stu-id="95795-132">System.String</span></span>

## <span data-ttu-id="95795-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95795-133">OUTPUTS</span></span>

### <span data-ttu-id="95795-134">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="95795-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="95795-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95795-135">NOTES</span></span>

## <span data-ttu-id="95795-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95795-136">RELATED LINKS</span></span>

[<span data-ttu-id="95795-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="95795-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
