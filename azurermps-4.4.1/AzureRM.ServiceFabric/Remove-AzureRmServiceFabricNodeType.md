---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 3da05194d74de1fe547beb66dea420a7f0e90155
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589091"
---
# <span data-ttu-id="cc905-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="cc905-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="cc905-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc905-102">SYNOPSIS</span></span>
<span data-ttu-id="cc905-103">Bir kümeden tam bir düğüm türü kaldırma.</span><span class="sxs-lookup"><span data-stu-id="cc905-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc905-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc905-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc905-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc905-105">DESCRIPTION</span></span>
<span data-ttu-id="cc905-106">**Remove-AzureRmServiceFabricNodeType** öğesini kullanarak belirli bir düğüm türünden tüm düğümleri ve bir kümeden düğüm türünü kaldırın.</span><span class="sxs-lookup"><span data-stu-id="cc905-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="cc905-107">Bu komut, birincil düğüm türünü silmek için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="cc905-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="cc905-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc905-108">EXAMPLES</span></span>

### <span data-ttu-id="cc905-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cc905-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="cc905-110">Bu komut, kümenizdeki ' NT1 ' NodeType öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cc905-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="cc905-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc905-111">PARAMETERS</span></span>

### <span data-ttu-id="cc905-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="cc905-112">-Name</span></span>
<span data-ttu-id="cc905-113">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="cc905-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cc905-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="cc905-114">-NodeType</span></span>
<span data-ttu-id="cc905-115">Düğüm türü adı.</span><span class="sxs-lookup"><span data-stu-id="cc905-115">The node type name.</span></span>

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

### <span data-ttu-id="cc905-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc905-116">-ResourceGroupName</span></span>
<span data-ttu-id="cc905-117">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc905-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cc905-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc905-118">-Confirm</span></span>
<span data-ttu-id="cc905-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc905-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc905-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc905-120">-WhatIf</span></span>
<span data-ttu-id="cc905-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc905-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc905-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc905-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc905-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc905-123">-DefaultProfile</span></span>
<span data-ttu-id="cc905-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc905-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc905-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc905-125">CommonParameters</span></span>
<span data-ttu-id="cc905-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc905-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc905-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc905-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc905-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc905-128">INPUTS</span></span>

### <span data-ttu-id="cc905-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cc905-129">System.String</span></span>

## <span data-ttu-id="cc905-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc905-130">OUTPUTS</span></span>

### <span data-ttu-id="cc905-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="cc905-131">System.Object</span></span>

## <span data-ttu-id="cc905-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc905-132">NOTES</span></span>

## <span data-ttu-id="cc905-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc905-133">RELATED LINKS</span></span>

