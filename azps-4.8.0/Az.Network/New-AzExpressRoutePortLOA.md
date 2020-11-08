---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274860"
---
# <span data-ttu-id="63d2d-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="63d2d-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="63d2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="63d2d-103">Hızlı yol bağlantı noktası için yetkilendirme belgesi harfini indirin.</span><span class="sxs-lookup"><span data-stu-id="63d2d-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="63d2d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63d2d-104">SYNTAX</span></span>

### <span data-ttu-id="63d2d-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63d2d-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63d2d-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="63d2d-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63d2d-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="63d2d-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63d2d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="63d2d-108">DESCRIPTION</span></span>
<span data-ttu-id="63d2d-109">New-AzExpressRoutePortLOA cmdlet, bir hızlı yol bağlantı noktası için bir yetkilendirme belgesini PDF biçiminde indirir.</span><span class="sxs-lookup"><span data-stu-id="63d2d-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="63d2d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63d2d-110">EXAMPLES</span></span>

### <span data-ttu-id="63d2d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63d2d-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="63d2d-112">' MyPort ' hızlı rota bağlantı noktası için yetkilendirme belgesi harfini indirin ve ' loa.pdf ' dosyasında saklayın.</span><span class="sxs-lookup"><span data-stu-id="63d2d-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="63d2d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63d2d-113">PARAMETERS</span></span>

### <span data-ttu-id="63d2d-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="63d2d-114">-AsJob</span></span>
<span data-ttu-id="63d2d-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="63d2d-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="63d2d-116">-CustomerName</span></span>
<span data-ttu-id="63d2d-117">Bu hızlı yol bağlantı noktasının atandığı müşterinin adı.</span><span class="sxs-lookup"><span data-stu-id="63d2d-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d2d-118">-DefaultProfile</span></span>
<span data-ttu-id="63d2d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63d2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63d2d-120">-Hedef</span><span class="sxs-lookup"><span data-stu-id="63d2d-120">-Destination</span></span>
<span data-ttu-id="63d2d-121">Yetkilendirme harfinin depolanacağı çıkış FilePath.</span><span class="sxs-lookup"><span data-stu-id="63d2d-121">The output filepath to store the Letter of Authorization to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="63d2d-122">-ExpressRoutePort</span></span>
<span data-ttu-id="63d2d-123">Hızlı rota bağlantı noktası kaynağı.</span><span class="sxs-lookup"><span data-stu-id="63d2d-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-124">-ID</span><span class="sxs-lookup"><span data-stu-id="63d2d-124">-Id</span></span>
<span data-ttu-id="63d2d-125">Hızlı rota bağlantı noktasının RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="63d2d-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="63d2d-126">-PassThru</span></span>
<span data-ttu-id="63d2d-127">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="63d2d-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="63d2d-128">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="63d2d-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="63d2d-129">-PortName</span></span>
<span data-ttu-id="63d2d-130">Hızlı rota bağlantı noktası adı.</span><span class="sxs-lookup"><span data-stu-id="63d2d-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d2d-131">-ResourceGroupName</span></span>
<span data-ttu-id="63d2d-132">Hızlı yol bağlantı noktasının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="63d2d-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d2d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d2d-133">CommonParameters</span></span>
<span data-ttu-id="63d2d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63d2d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d2d-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="63d2d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d2d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63d2d-136">INPUTS</span></span>

### <span data-ttu-id="63d2d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="63d2d-137">System.String</span></span>

## <span data-ttu-id="63d2d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63d2d-138">OUTPUTS</span></span>

### <span data-ttu-id="63d2d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="63d2d-139">System.Boolean</span></span>

## <span data-ttu-id="63d2d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63d2d-140">NOTES</span></span>

## <span data-ttu-id="63d2d-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63d2d-141">RELATED LINKS</span></span>
