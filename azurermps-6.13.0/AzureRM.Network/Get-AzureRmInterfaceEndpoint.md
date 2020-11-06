---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurerminterfaceendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmInterfaceEndpoint.md
ms.openlocfilehash: 8759546c9d7161f2bea139845c7d291c6d7832b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590177"
---
# <span data-ttu-id="f9860-101">Get-AzureRmInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="f9860-101">Get-AzureRmInterfaceEndpoint</span></span>

## <span data-ttu-id="f9860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9860-102">SYNOPSIS</span></span>
<span data-ttu-id="f9860-103">Get-AzureRmInterfaceEndpoint cmdlet bir arabirim uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="f9860-103">The Get-AzureRmInterfaceEndpoint cmdlet gets a Interface Endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9860-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9860-104">SYNTAX</span></span>

### <span data-ttu-id="f9860-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9860-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmInterfaceEndpoint [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9860-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f9860-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmInterfaceEndpoint -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9860-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9860-107">DESCRIPTION</span></span>
<span data-ttu-id="f9860-108">**Get-Azurerminter, Endpoint** cmdlet 'ı bir arabirim uç noktası alır.</span><span class="sxs-lookup"><span data-stu-id="f9860-108">The **Get-AzureRmInterfaceEndpoint** cmdlet gets a Interface Endpoint.</span></span>

## <span data-ttu-id="f9860-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9860-109">EXAMPLES</span></span>

### <span data-ttu-id="f9860-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f9860-110">Example 1</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -Name "InterfaceEndpoint1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f9860-111">Bu komut, ResourceGroup01 adındaki kaynak grubuna ait InterfaceEndpoint1 adındaki arabirim uç noktasını alır ve $interfaceendpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f9860-111">This command gets the interface endpoint named InterfaceEndpoint1 that belongs to the resource group named ResourceGroup01 and stores it in the $interfaceendpoint variable.</span></span>

### <span data-ttu-id="f9860-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f9860-112">Example 2</span></span>
```
$interfaceendpoint = Get-AzureRmInterfaceEndpoint -ResourceId "/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10"

```

<span data-ttu-id="f9860-113">Bu komut RESOURCEID/subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 ile arabirim uç noktasını alır ve $interfaceendpoint değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f9860-113">This command gets the interface endpoint with resourceId  /subscriptions/sub1/resourceGroups/chsriniIEtest1/providers/Microsoft.Network/interfaceEndpoints/ie1.10 and stores it in the $interfaceendpoint variable.</span></span>


## <span data-ttu-id="f9860-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9860-114">PARAMETERS</span></span>

### <span data-ttu-id="f9860-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9860-115">-DefaultProfile</span></span>
<span data-ttu-id="f9860-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9860-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9860-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9860-117">-Name</span></span>
<span data-ttu-id="f9860-118">Arabirim uç noktasının adı</span><span class="sxs-lookup"><span data-stu-id="f9860-118">The name of the interface endpoint</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9860-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9860-119">-ResourceGroupName</span></span>
<span data-ttu-id="f9860-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f9860-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9860-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f9860-121">-ResourceId</span></span>
<span data-ttu-id="f9860-122">{{Fill RESOURCEID açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f9860-122">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9860-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9860-123">-Confirm</span></span>
<span data-ttu-id="f9860-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9860-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9860-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9860-125">-WhatIf</span></span>
<span data-ttu-id="f9860-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9860-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9860-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9860-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9860-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9860-128">CommonParameters</span></span>
<span data-ttu-id="f9860-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9860-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f9860-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9860-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9860-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9860-131">INPUTS</span></span>

### <span data-ttu-id="f9860-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f9860-132">System.String</span></span>


## <span data-ttu-id="f9860-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9860-133">OUTPUTS</span></span>

### <span data-ttu-id="f9860-134">Microsoft. Azure. Commands. Network. model. Psınterfaceendpoint</span><span class="sxs-lookup"><span data-stu-id="f9860-134">Microsoft.Azure.Commands.Network.Models.PSInterfaceEndpoint</span></span>


## <span data-ttu-id="f9860-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9860-135">NOTES</span></span>

## <span data-ttu-id="f9860-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9860-136">RELATED LINKS</span></span>
