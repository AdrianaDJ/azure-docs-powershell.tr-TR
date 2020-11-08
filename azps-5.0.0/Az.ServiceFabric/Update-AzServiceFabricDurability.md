---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279605"
---
# <span data-ttu-id="46339-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="46339-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="46339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46339-102">SYNOPSIS</span></span>
<span data-ttu-id="46339-103">Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="46339-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="46339-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46339-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46339-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46339-105">DESCRIPTION</span></span>
<span data-ttu-id="46339-106">, Kümenin dayanıklılık veya SKU 'YU güncelleştirmek için **Update-Azservicefabricdayanıklılık** 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="46339-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="46339-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46339-107">EXAMPLES</span></span>

### <span data-ttu-id="46339-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="46339-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="46339-109">Bu komut, NodeType 'in dayanıklılık katmanını ' NT1 ' ile gümüş 'ya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="46339-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="46339-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46339-110">PARAMETERS</span></span>

### <span data-ttu-id="46339-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46339-111">-DefaultProfile</span></span>
<span data-ttu-id="46339-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46339-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46339-113">-Dur, Itylevel</span><span class="sxs-lookup"><span data-stu-id="46339-113">-DurabilityLevel</span></span>
<span data-ttu-id="46339-114">Dayanıklılık düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="46339-114">Specify durability level.</span></span>

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

### <span data-ttu-id="46339-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="46339-115">-Name</span></span>
<span data-ttu-id="46339-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="46339-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="46339-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="46339-117">-NodeType</span></span>
<span data-ttu-id="46339-118">Hizmet yapısı düğüm türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="46339-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="46339-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46339-119">-ResourceGroupName</span></span>
<span data-ttu-id="46339-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46339-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="46339-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="46339-121">-Sku</span></span>
<span data-ttu-id="46339-122">Düğüm türünün SKU adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="46339-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="46339-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="46339-123">-Confirm</span></span>
<span data-ttu-id="46339-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46339-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46339-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46339-125">-WhatIf</span></span>
<span data-ttu-id="46339-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46339-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46339-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46339-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46339-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46339-128">CommonParameters</span></span>
<span data-ttu-id="46339-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46339-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46339-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="46339-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46339-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46339-131">INPUTS</span></span>

### <span data-ttu-id="46339-132">System. String</span><span class="sxs-lookup"><span data-stu-id="46339-132">System.String</span></span>

### <span data-ttu-id="46339-133">Microsoft. Azure. Commands. ServiceFabric. modeller. Durkomutlarıdüzey</span><span class="sxs-lookup"><span data-stu-id="46339-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="46339-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46339-134">OUTPUTS</span></span>

### <span data-ttu-id="46339-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="46339-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="46339-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46339-136">NOTES</span></span>

## <span data-ttu-id="46339-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46339-137">RELATED LINKS</span></span>
