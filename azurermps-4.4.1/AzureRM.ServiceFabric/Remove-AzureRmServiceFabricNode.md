---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: cbf23af4c98e8174091b467e6e05ed5de6ae20c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589092"
---
# <span data-ttu-id="42faf-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="42faf-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="42faf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42faf-102">SYNOPSIS</span></span>
<span data-ttu-id="42faf-103">Belirli düğüm türünden düğümleri kümeden kaldırma.</span><span class="sxs-lookup"><span data-stu-id="42faf-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42faf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42faf-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToRemove <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42faf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="42faf-105">DESCRIPTION</span></span>
<span data-ttu-id="42faf-106">Bir kümeden belirli bir düğüm türünden düğümleri kaldırmak için **Remove-AzureRmServiceFabricNode** öğesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="42faf-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="42faf-107">Kaldırma işlemi yalnızca küme durumu ölçümlerine uyuyorsa devam eder.</span><span class="sxs-lookup"><span data-stu-id="42faf-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="42faf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42faf-108">EXAMPLES</span></span>

### <span data-ttu-id="42faf-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="42faf-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="42faf-110">Bu komut, ' NT1 ' NodeType 'daki 2 düğümü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="42faf-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="42faf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42faf-111">PARAMETERS</span></span>

### <span data-ttu-id="42faf-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="42faf-112">-Name</span></span>
<span data-ttu-id="42faf-113">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="42faf-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="42faf-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="42faf-114">-NodeType</span></span>
<span data-ttu-id="42faf-115">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="42faf-115">Node type name.</span></span>

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

### <span data-ttu-id="42faf-116">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="42faf-116">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="42faf-117">Kaldırılacak düğüm sayısı.</span><span class="sxs-lookup"><span data-stu-id="42faf-117">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="42faf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42faf-118">-ResourceGroupName</span></span>
<span data-ttu-id="42faf-119">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="42faf-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="42faf-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="42faf-120">-Confirm</span></span>
<span data-ttu-id="42faf-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42faf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42faf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42faf-122">-WhatIf</span></span>
<span data-ttu-id="42faf-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42faf-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42faf-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42faf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42faf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42faf-125">-DefaultProfile</span></span>
<span data-ttu-id="42faf-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42faf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42faf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42faf-127">CommonParameters</span></span>
<span data-ttu-id="42faf-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42faf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42faf-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42faf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42faf-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42faf-130">INPUTS</span></span>

### <span data-ttu-id="42faf-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="42faf-131">System.Int32</span></span>
<span data-ttu-id="42faf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="42faf-132">System.String</span></span>

## <span data-ttu-id="42faf-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42faf-133">OUTPUTS</span></span>

### <span data-ttu-id="42faf-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="42faf-134">System.Object</span></span>

## <span data-ttu-id="42faf-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42faf-135">NOTES</span></span>

## <span data-ttu-id="42faf-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42faf-136">RELATED LINKS</span></span>

[<span data-ttu-id="42faf-137">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="42faf-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
