---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: dc568657feb5f86cf7cfaa21042e03f8470a9caa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096842"
---
# <span data-ttu-id="4bf16-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4bf16-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="4bf16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bf16-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf16-103">Azure VirtualRouter alma</span><span class="sxs-lookup"><span data-stu-id="4bf16-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="4bf16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bf16-104">SYNTAX</span></span>

### <span data-ttu-id="4bf16-105">VirtualRouterNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bf16-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bf16-106">Virtualrouterresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4bf16-106">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bf16-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bf16-107">DESCRIPTION</span></span>
<span data-ttu-id="4bf16-108">**Get-AzVirtualRouter** cmdlet 'ı bir Azure virtualrouter alır</span><span class="sxs-lookup"><span data-stu-id="4bf16-108">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="4bf16-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bf16-109">EXAMPLES</span></span>

### <span data-ttu-id="4bf16-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4bf16-110">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="4bf16-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4bf16-111">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="4bf16-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bf16-112">PARAMETERS</span></span>

### <span data-ttu-id="4bf16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf16-113">-DefaultProfile</span></span>
<span data-ttu-id="4bf16-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bf16-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf16-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf16-115">-ResourceGroupName</span></span>
<span data-ttu-id="4bf16-116">Sanal yönlendiricinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4bf16-116">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf16-117">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4bf16-117">-ResourceId</span></span>
<span data-ttu-id="4bf16-118">Sanal yönlendiricinin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="4bf16-118">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf16-119">-RouterName</span><span class="sxs-lookup"><span data-stu-id="4bf16-119">-RouterName</span></span>
<span data-ttu-id="4bf16-120">Sanal yönlendiricinin adı.</span><span class="sxs-lookup"><span data-stu-id="4bf16-120">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf16-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf16-121">CommonParameters</span></span>
<span data-ttu-id="4bf16-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bf16-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf16-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bf16-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf16-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bf16-124">INPUTS</span></span>

### <span data-ttu-id="4bf16-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4bf16-125">System.String</span></span>

## <span data-ttu-id="4bf16-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bf16-126">OUTPUTS</span></span>

### <span data-ttu-id="4bf16-127">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4bf16-127">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="4bf16-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bf16-128">NOTES</span></span>

## <span data-ttu-id="4bf16-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bf16-129">RELATED LINKS</span></span>