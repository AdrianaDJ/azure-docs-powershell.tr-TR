---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279961"
---
# <span data-ttu-id="dcd11-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dcd11-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="dcd11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd11-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd11-103">Bir Azure ExpressRoutePort kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="dcd11-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="dcd11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dcd11-104">SYNTAX</span></span>

### <span data-ttu-id="dcd11-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dcd11-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcd11-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dcd11-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcd11-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dcd11-107">DESCRIPTION</span></span>
<span data-ttu-id="dcd11-108">**Get-AzExpressRoutePort** cmdlet 'i aboneliğinizden bir ExpressRoutePort nesnesini almak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="dcd11-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="dcd11-109">Döndürülen expressrouteport nesnesi ExpressRoutePort üzerinde çalışan diğer cmdlet 'ler için girdi olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="dcd11-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="dcd11-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dcd11-110">EXAMPLES</span></span>

### <span data-ttu-id="dcd11-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dcd11-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="dcd11-112">Aboneliğinizdeki $rg $PortName adlı ExpressRoutePort nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="dcd11-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="dcd11-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="dcd11-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="dcd11-114">Adı "test" ile başlayan ExpressRoutePort nesnelerini alır.</span><span class="sxs-lookup"><span data-stu-id="dcd11-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="dcd11-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="dcd11-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="dcd11-116">RESOURCEID $id ile ExpressRoutePort nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="dcd11-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="dcd11-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dcd11-117">PARAMETERS</span></span>

### <span data-ttu-id="dcd11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd11-118">-DefaultProfile</span></span>
<span data-ttu-id="dcd11-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dcd11-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcd11-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="dcd11-120">-Name</span></span>
<span data-ttu-id="dcd11-121">ExpressRoutePort adı.</span><span class="sxs-lookup"><span data-stu-id="dcd11-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dcd11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd11-122">-ResourceGroupName</span></span>
<span data-ttu-id="dcd11-123">ExpressRoutePort kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="dcd11-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="dcd11-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dcd11-124">-ResourceId</span></span>
<span data-ttu-id="dcd11-125">Hızlı rota bağlantı noktasının RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="dcd11-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="dcd11-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd11-126">CommonParameters</span></span>
<span data-ttu-id="dcd11-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dcd11-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd11-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dcd11-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd11-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dcd11-129">INPUTS</span></span>

### <span data-ttu-id="dcd11-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dcd11-130">System.String</span></span>

## <span data-ttu-id="dcd11-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dcd11-131">OUTPUTS</span></span>

### <span data-ttu-id="dcd11-132">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dcd11-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="dcd11-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dcd11-133">NOTES</span></span>

## <span data-ttu-id="dcd11-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dcd11-134">RELATED LINKS</span></span>

[<span data-ttu-id="dcd11-135">Yeni-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dcd11-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="dcd11-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dcd11-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="dcd11-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dcd11-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
