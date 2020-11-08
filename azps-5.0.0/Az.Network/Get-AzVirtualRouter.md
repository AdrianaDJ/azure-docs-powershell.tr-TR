---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 26e919935a65a486252cac234450adf214992b36
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276904"
---
# <span data-ttu-id="661ca-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="661ca-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="661ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="661ca-102">SYNOPSIS</span></span>
<span data-ttu-id="661ca-103">Azure VirtualRouter alma</span><span class="sxs-lookup"><span data-stu-id="661ca-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="661ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="661ca-104">SYNTAX</span></span>

### <span data-ttu-id="661ca-105">Virtualroutersubscriptionıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="661ca-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="661ca-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="661ca-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="661ca-107">Virtualrouterresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="661ca-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="661ca-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="661ca-108">DESCRIPTION</span></span>
<span data-ttu-id="661ca-109">**Get-AzVirtualRouter** cmdlet 'ı bir Azure virtualrouter alır</span><span class="sxs-lookup"><span data-stu-id="661ca-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="661ca-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="661ca-110">EXAMPLES</span></span>

### <span data-ttu-id="661ca-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="661ca-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="661ca-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="661ca-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="661ca-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="661ca-113">PARAMETERS</span></span>

### <span data-ttu-id="661ca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="661ca-114">-DefaultProfile</span></span>
<span data-ttu-id="661ca-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="661ca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="661ca-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="661ca-116">-ResourceGroupName</span></span>
<span data-ttu-id="661ca-117">Sanal yönlendiricinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="661ca-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661ca-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="661ca-118">-ResourceId</span></span>
<span data-ttu-id="661ca-119">Sanal yönlendiricinin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="661ca-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661ca-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="661ca-120">-RouterName</span></span>
<span data-ttu-id="661ca-121">Sanal yönlendiricinin adı.</span><span class="sxs-lookup"><span data-stu-id="661ca-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="661ca-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="661ca-122">CommonParameters</span></span>
<span data-ttu-id="661ca-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="661ca-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="661ca-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="661ca-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="661ca-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="661ca-125">INPUTS</span></span>

### <span data-ttu-id="661ca-126">System. String</span><span class="sxs-lookup"><span data-stu-id="661ca-126">System.String</span></span>

## <span data-ttu-id="661ca-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="661ca-127">OUTPUTS</span></span>

### <span data-ttu-id="661ca-128">Microsoft. Azure. Commands. Network. modeller. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="661ca-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="661ca-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="661ca-129">NOTES</span></span>

## <span data-ttu-id="661ca-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="661ca-130">RELATED LINKS</span></span>
