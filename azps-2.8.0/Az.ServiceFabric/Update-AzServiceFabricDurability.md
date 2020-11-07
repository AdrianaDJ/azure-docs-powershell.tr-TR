---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 283ca228ba44d2ec87cd926d23e0217eb67434eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932412"
---
# <span data-ttu-id="01208-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="01208-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="01208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01208-102">SYNOPSIS</span></span>
<span data-ttu-id="01208-103">Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="01208-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="01208-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01208-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01208-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01208-105">DESCRIPTION</span></span>
<span data-ttu-id="01208-106">, Kümenin dayanıklılık veya SKU 'YU güncelleştirmek için **Update-Azservicefabricdayanıklılık** 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="01208-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="01208-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01208-107">EXAMPLES</span></span>

### <span data-ttu-id="01208-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="01208-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="01208-109">Bu komut, NodeType 'in dayanıklılık katmanını ' NT1 ' ile gümüş 'ya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="01208-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="01208-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01208-110">PARAMETERS</span></span>

### <span data-ttu-id="01208-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01208-111">-DefaultProfile</span></span>
<span data-ttu-id="01208-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01208-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01208-113">-Dur, Itylevel</span><span class="sxs-lookup"><span data-stu-id="01208-113">-DurabilityLevel</span></span>
<span data-ttu-id="01208-114">Dayanıklılık düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="01208-114">Specify durability level.</span></span>

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

### <span data-ttu-id="01208-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="01208-115">-Name</span></span>
<span data-ttu-id="01208-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="01208-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="01208-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="01208-117">-NodeType</span></span>
<span data-ttu-id="01208-118">Hizmet yapısı düğüm türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="01208-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="01208-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01208-119">-ResourceGroupName</span></span>
<span data-ttu-id="01208-120">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01208-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="01208-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="01208-121">-Sku</span></span>
<span data-ttu-id="01208-122">Düğüm türünün SKU adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="01208-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="01208-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="01208-123">-Confirm</span></span>
<span data-ttu-id="01208-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01208-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01208-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01208-125">-WhatIf</span></span>
<span data-ttu-id="01208-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01208-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01208-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01208-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01208-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01208-128">CommonParameters</span></span>
<span data-ttu-id="01208-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01208-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01208-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01208-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01208-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01208-131">INPUTS</span></span>

### <span data-ttu-id="01208-132">System. String</span><span class="sxs-lookup"><span data-stu-id="01208-132">System.String</span></span>

### <span data-ttu-id="01208-133">Microsoft. Azure. Commands. ServiceFabric. modeller. Durkomutlarıdüzey</span><span class="sxs-lookup"><span data-stu-id="01208-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="01208-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01208-134">OUTPUTS</span></span>

### <span data-ttu-id="01208-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="01208-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="01208-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01208-136">NOTES</span></span>

## <span data-ttu-id="01208-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01208-137">RELATED LINKS</span></span>
