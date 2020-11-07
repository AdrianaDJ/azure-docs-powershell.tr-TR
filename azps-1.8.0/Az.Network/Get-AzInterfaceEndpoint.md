---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azinterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzInterfaceEndpoint.md
ms.openlocfilehash: 55133225b380e16112301620a52f857fca50dc0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760563"
---
# <span data-ttu-id="d7151-101">Get-AzInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7151-101">Get-AzInterfaceEndpoint</span></span>

## <span data-ttu-id="d7151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7151-102">SYNOPSIS</span></span>
<span data-ttu-id="d7151-103">Get-AzInterfaceEndpoint cmdlet bir arabirim uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="d7151-103">The Get-AzInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="d7151-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d7151-104">SYNTAX</span></span>

### <span data-ttu-id="d7151-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d7151-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzInterfaceEndpoint [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7151-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d7151-106">GetByResourceIdParameterSet</span></span>
```
Get-AzInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7151-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d7151-107">DESCRIPTION</span></span>
<span data-ttu-id="d7151-108">**Get-Azınterfaceendpoint** cmdlet 'ı bir arabirim uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="d7151-108">The **Get-AzInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="d7151-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d7151-109">EXAMPLES</span></span>

### <span data-ttu-id="d7151-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d7151-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d7151-111">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait InterfaceEndpoint1 adındaki arabirim uç noktasını alır ve $interfaceendpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d7151-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="d7151-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d7151-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"
```

<span data-ttu-id="d7151-113">Bu komut RESOURCEID/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 ile arabirim uç noktasını alır ve $interfaceendpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d7151-113">This command gets the interface endpoint with resourceId /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="d7151-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d7151-114">Example 3</span></span>
```
$interfaceendpoint = Get-AzInterfaceEndpoint -Name InterfaceEndpoint*
```

<span data-ttu-id="d7151-115">Bu komut, "ınterfaceendpoint" ile başlayan arabirim uç noktalarını alır</span><span class="sxs-lookup"><span data-stu-id="d7151-115">This command gets the interface endpoints that start with "InterfaceEndpoint"</span></span>

## <span data-ttu-id="d7151-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d7151-116">PARAMETERS</span></span>

### <span data-ttu-id="d7151-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7151-117">-DefaultProfile</span></span>
<span data-ttu-id="d7151-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d7151-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7151-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d7151-119">-Name</span></span>
<span data-ttu-id="d7151-120">Arabirim uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="d7151-120">The name of the interface endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d7151-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7151-121">-ResourceGroupName</span></span>
<span data-ttu-id="d7151-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d7151-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d7151-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d7151-123">-ResourceId</span></span>
<span data-ttu-id="d7151-124">Arabirim uç noktasının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d7151-124">The ID of the interface endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7151-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="d7151-125">-Confirm</span></span>
<span data-ttu-id="d7151-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d7151-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7151-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7151-127">-WhatIf</span></span>
<span data-ttu-id="d7151-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d7151-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7151-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d7151-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7151-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7151-130">CommonParameters</span></span>
<span data-ttu-id="d7151-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d7151-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7151-132">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d7151-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7151-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d7151-133">INPUTS</span></span>

### <span data-ttu-id="d7151-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d7151-134">System.String</span></span>

## <span data-ttu-id="d7151-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d7151-135">OUTPUTS</span></span>

### <span data-ttu-id="d7151-136">Microsoft. Azure. Commands. Network. model. Psınterfaceendpoint</span><span class="sxs-lookup"><span data-stu-id="d7151-136">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>

## <span data-ttu-id="d7151-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d7151-137">NOTES</span></span>

## <span data-ttu-id="d7151-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d7151-138">RELATED LINKS</span></span>
