---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 56a6afff6551ae0191ac1f17d3a52c47940e045a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590845"
---
# <span data-ttu-id="d05dc-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="d05dc-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="d05dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d05dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d05dc-103">Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="d05dc-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d05dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d05dc-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d05dc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d05dc-105">DESCRIPTION</span></span>
<span data-ttu-id="d05dc-106">, Kümenin dayanıklılık veya SKU 'YU güncelleştirmek için **Update-Azurermservicefabricdayanıklılık** 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="d05dc-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="d05dc-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d05dc-107">EXAMPLES</span></span>

### <span data-ttu-id="d05dc-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d05dc-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="d05dc-109">Bu komut, NodeType 'in dayanıklılık katmanını ' NT1 ' ile gümüş 'ya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d05dc-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="d05dc-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d05dc-110">PARAMETERS</span></span>

### <span data-ttu-id="d05dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d05dc-111">-DefaultProfile</span></span>
<span data-ttu-id="d05dc-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d05dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d05dc-113">-Dur, Itylevel</span><span class="sxs-lookup"><span data-stu-id="d05dc-113">-DurabilityLevel</span></span>
<span data-ttu-id="d05dc-114">Dayanıklılık düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="d05dc-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d05dc-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d05dc-115">-Name</span></span>
<span data-ttu-id="d05dc-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d05dc-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d05dc-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="d05dc-117">-NodeType</span></span>
<span data-ttu-id="d05dc-118">Hizmet yapısı düğüm türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d05dc-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="d05dc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d05dc-119">-ResourceGroupName</span></span>
<span data-ttu-id="d05dc-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d05dc-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d05dc-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="d05dc-121">-Sku</span></span>
<span data-ttu-id="d05dc-122">Düğüm türünün SKU adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="d05dc-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d05dc-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="d05dc-123">-Confirm</span></span>
<span data-ttu-id="d05dc-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d05dc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d05dc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d05dc-125">-WhatIf</span></span>
<span data-ttu-id="d05dc-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d05dc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d05dc-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d05dc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d05dc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d05dc-128">CommonParameters</span></span>
<span data-ttu-id="d05dc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d05dc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d05dc-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d05dc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d05dc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d05dc-131">INPUTS</span></span>

### <span data-ttu-id="d05dc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d05dc-132">System.String</span></span>
<span data-ttu-id="d05dc-133">Parametreler: NodeType (ByValue), STB (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d05dc-133">Parameters: NodeType (ByValue), Sku (ByValue)</span></span>

### <span data-ttu-id="d05dc-134">Microsoft. Azure. Commands. ServiceFabric. modeller. Durkomutlarıdüzey</span><span class="sxs-lookup"><span data-stu-id="d05dc-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="d05dc-135">Parametreler: Durumitylevel (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d05dc-135">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="d05dc-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d05dc-136">OUTPUTS</span></span>

### <span data-ttu-id="d05dc-137">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="d05dc-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d05dc-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d05dc-138">NOTES</span></span>

## <span data-ttu-id="d05dc-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d05dc-139">RELATED LINKS</span></span>
