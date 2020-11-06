---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 9c82f0aab38fb5479f5344166a409b9b32f7447c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592395"
---
# <span data-ttu-id="ed23f-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="ed23f-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="ed23f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed23f-102">SYNOPSIS</span></span>
<span data-ttu-id="ed23f-103">Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="ed23f-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed23f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed23f-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed23f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed23f-105">DESCRIPTION</span></span>
<span data-ttu-id="ed23f-106">, Kümenin dayanıklılık veya SKU 'YU güncelleştirmek için **Update-Azurermservicefabricdayanıklılık** 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ed23f-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="ed23f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed23f-107">EXAMPLES</span></span>

### <span data-ttu-id="ed23f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed23f-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="ed23f-109">Bu komut, NodeType 'in dayanıklılık katmanını ' NT1 ' ile gümüş 'ya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="ed23f-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="ed23f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed23f-110">PARAMETERS</span></span>

### <span data-ttu-id="ed23f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed23f-111">-DefaultProfile</span></span>
<span data-ttu-id="ed23f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed23f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed23f-113">-Dur, Itylevel</span><span class="sxs-lookup"><span data-stu-id="ed23f-113">-DurabilityLevel</span></span>
<span data-ttu-id="ed23f-114">Dayanıklılık düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ed23f-114">Specify durability level.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed23f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed23f-115">-Name</span></span>
<span data-ttu-id="ed23f-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ed23f-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ed23f-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ed23f-117">-NodeType</span></span>
<span data-ttu-id="ed23f-118">Hizmet yapısı düğüm türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ed23f-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="ed23f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed23f-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed23f-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed23f-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ed23f-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="ed23f-121">-Sku</span></span>
<span data-ttu-id="ed23f-122">Düğüm türünün SKU adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ed23f-122">Specify the SKU of the node type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed23f-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed23f-123">-Confirm</span></span>
<span data-ttu-id="ed23f-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed23f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed23f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed23f-125">-WhatIf</span></span>
<span data-ttu-id="ed23f-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed23f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed23f-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed23f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed23f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed23f-128">CommonParameters</span></span>
<span data-ttu-id="ed23f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed23f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed23f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed23f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed23f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed23f-131">INPUTS</span></span>

### <span data-ttu-id="ed23f-132">Microsoft. Azure. Commands. ServiceFabric. modeller. Durkomutlarıdüzey</span><span class="sxs-lookup"><span data-stu-id="ed23f-132">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="ed23f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ed23f-133">System.String</span></span>

## <span data-ttu-id="ed23f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed23f-134">OUTPUTS</span></span>

### <span data-ttu-id="ed23f-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="ed23f-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="ed23f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed23f-136">NOTES</span></span>

## <span data-ttu-id="ed23f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed23f-137">RELATED LINKS</span></span>

