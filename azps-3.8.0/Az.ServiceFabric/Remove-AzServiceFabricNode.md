---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 96706ef98a0b21bab06e2c6e8fae947dcd205271
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097150"
---
# <span data-ttu-id="ed9a9-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ed9a9-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="ed9a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9a9-103">Belirli düğüm türünden düğümleri kümeden kaldırma.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="ed9a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed9a9-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed9a9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed9a9-106">Bir kümeden belirli bir düğüm türünden düğümleri kaldırmak için **Remove-AzServiceFabricNode** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="ed9a9-107">Kaldırma işlemi yalnızca küme durumu ölçümlerine uyuyorsa devam eder.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="ed9a9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed9a9-108">EXAMPLES</span></span>

### <span data-ttu-id="ed9a9-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed9a9-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="ed9a9-110">Bu komut, ' NT1 ' NodeType 'daki 2 düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="ed9a9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed9a9-111">PARAMETERS</span></span>

### <span data-ttu-id="ed9a9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9a9-112">-DefaultProfile</span></span>
<span data-ttu-id="ed9a9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed9a9-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed9a9-114">-Name</span></span>
<span data-ttu-id="ed9a9-115">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="ed9a9-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="ed9a9-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ed9a9-116">-NodeType</span></span>
<span data-ttu-id="ed9a9-117">Düğüm türü adı</span><span class="sxs-lookup"><span data-stu-id="ed9a9-117">Node type name</span></span>

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

### <span data-ttu-id="ed9a9-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="ed9a9-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="ed9a9-119">Eklenecek düğümlerin sayısı</span><span class="sxs-lookup"><span data-stu-id="ed9a9-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="ed9a9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed9a9-120">-ResourceGroupName</span></span>
<span data-ttu-id="ed9a9-121">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ed9a9-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed9a9-122">-Confirm</span></span>
<span data-ttu-id="ed9a9-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed9a9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed9a9-124">-WhatIf</span></span>
<span data-ttu-id="ed9a9-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed9a9-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed9a9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9a9-127">CommonParameters</span></span>
<span data-ttu-id="ed9a9-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed9a9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9a9-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed9a9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9a9-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed9a9-130">INPUTS</span></span>

### <span data-ttu-id="ed9a9-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ed9a9-131">System.Int32</span></span>

### <span data-ttu-id="ed9a9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ed9a9-132">System.String</span></span>

## <span data-ttu-id="ed9a9-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed9a9-133">OUTPUTS</span></span>

### <span data-ttu-id="ed9a9-134">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="ed9a9-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ed9a9-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed9a9-135">NOTES</span></span>

## <span data-ttu-id="ed9a9-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed9a9-136">RELATED LINKS</span></span>

[<span data-ttu-id="ed9a9-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ed9a9-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
