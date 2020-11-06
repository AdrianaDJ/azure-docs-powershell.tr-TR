---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 1c62c637324f19088dfffcfb4c8defae0a056b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589086"
---
# <span data-ttu-id="cab7d-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="cab7d-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="cab7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cab7d-102">SYNOPSIS</span></span>
<span data-ttu-id="cab7d-103">Kümedeki bir düğümün dayanıklılık katmanını veya VmSku 'Yu güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="cab7d-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cab7d-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cab7d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cab7d-105">DESCRIPTION</span></span>
<span data-ttu-id="cab7d-106">, Kümenin dayanıklılık veya SKU 'YU güncelleştirmek için **Update-Azurermservicefabricdayanıklılık** 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="cab7d-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="cab7d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cab7d-107">EXAMPLES</span></span>

### <span data-ttu-id="cab7d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cab7d-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="cab7d-109">Bu komut, NodeType 'in dayanıklılık katmanını ' NT1 ' ile gümüş 'ya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cab7d-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="cab7d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cab7d-110">PARAMETERS</span></span>

### <span data-ttu-id="cab7d-111">-Dur, Itylevel</span><span class="sxs-lookup"><span data-stu-id="cab7d-111">-DurabilityLevel</span></span>
<span data-ttu-id="cab7d-112">Dayanıklılık düzeyini belirtin.</span><span class="sxs-lookup"><span data-stu-id="cab7d-112">Specify durability level.</span></span>

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

### <span data-ttu-id="cab7d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="cab7d-113">-Name</span></span>
<span data-ttu-id="cab7d-114">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="cab7d-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cab7d-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="cab7d-115">-NodeType</span></span>
<span data-ttu-id="cab7d-116">Hizmet yapısı düğüm türü adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="cab7d-116">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="cab7d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab7d-117">-ResourceGroupName</span></span>
<span data-ttu-id="cab7d-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cab7d-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cab7d-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="cab7d-119">-Sku</span></span>
<span data-ttu-id="cab7d-120">Düğüm türünün SKU adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="cab7d-120">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="cab7d-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="cab7d-121">-Confirm</span></span>
<span data-ttu-id="cab7d-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cab7d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cab7d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cab7d-123">-WhatIf</span></span>
<span data-ttu-id="cab7d-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cab7d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cab7d-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cab7d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cab7d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab7d-126">-DefaultProfile</span></span>
<span data-ttu-id="cab7d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cab7d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cab7d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab7d-128">CommonParameters</span></span>
<span data-ttu-id="cab7d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cab7d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab7d-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab7d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab7d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cab7d-131">INPUTS</span></span>

### <span data-ttu-id="cab7d-132">Microsoft. Azure. Commands. ServiceFabric. modeller. Durkomutlarıdüzey</span><span class="sxs-lookup"><span data-stu-id="cab7d-132">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="cab7d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cab7d-133">System.String</span></span>

## <span data-ttu-id="cab7d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cab7d-134">OUTPUTS</span></span>

### <span data-ttu-id="cab7d-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PsCluster</span><span class="sxs-lookup"><span data-stu-id="cab7d-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="cab7d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cab7d-136">NOTES</span></span>

## <span data-ttu-id="cab7d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cab7d-137">RELATED LINKS</span></span>

