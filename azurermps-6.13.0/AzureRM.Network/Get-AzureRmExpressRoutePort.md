---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
ms.openlocfilehash: 36c15c9a0bfae9bbf3a14f59877d23c1c8778163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764624"
---
# <span data-ttu-id="dd1e2-101">Get-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dd1e2-101">Get-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="dd1e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1e2-103">Bir Azure ExpressRoutePort kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-103">Gets an Azure ExpressRoutePort resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd1e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd1e2-104">SYNTAX</span></span>

### <span data-ttu-id="dd1e2-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd1e2-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd1e2-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dd1e2-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd1e2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd1e2-107">DESCRIPTION</span></span>
<span data-ttu-id="dd1e2-108">**Get-AzureRmExpressRoutePort** cmdlet 'i aboneliğinizden bir expressrouteport nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-108">The **Get-AzureRmExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="dd1e2-109">Döndürülen expressrouteport nesnesi ExpressRoutePort üzerinde çalışan diğer cmdlet 'ler için girdi olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="dd1e2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd1e2-110">EXAMPLES</span></span>

### <span data-ttu-id="dd1e2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd1e2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="dd1e2-112">Aboneliğinizdeki $rg $PortName adlı ExpressRoutePort nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="dd1e2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dd1e2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -ResourceId $id
```

<span data-ttu-id="dd1e2-114">RESOURCEID $id ile ExpressRoutePort nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-114">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="dd1e2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd1e2-115">PARAMETERS</span></span>

### <span data-ttu-id="dd1e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1e2-116">-DefaultProfile</span></span>
<span data-ttu-id="dd1e2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd1e2-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd1e2-118">-Name</span></span>
<span data-ttu-id="dd1e2-119">ExpressRoutePort adı.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-119">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1e2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd1e2-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd1e2-121">ExpressRoutePort kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-121">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1e2-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dd1e2-122">-ResourceId</span></span>
<span data-ttu-id="dd1e2-123">Hızlı rota bağlantı noktasının RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-123">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1e2-124">CommonParameters</span></span>
<span data-ttu-id="dd1e2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd1e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1e2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd1e2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1e2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd1e2-127">INPUTS</span></span>

### <span data-ttu-id="dd1e2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dd1e2-128">System.String</span></span>

## <span data-ttu-id="dd1e2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd1e2-129">OUTPUTS</span></span>

### <span data-ttu-id="dd1e2-130">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dd1e2-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="dd1e2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd1e2-131">NOTES</span></span>

## <span data-ttu-id="dd1e2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd1e2-132">RELATED LINKS</span></span>
