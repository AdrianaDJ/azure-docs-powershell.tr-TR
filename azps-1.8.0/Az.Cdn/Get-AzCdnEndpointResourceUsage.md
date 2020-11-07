---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 1c9e83e8181d716024ae993ba0c3f5a9f75c6ef1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761420"
---
# <span data-ttu-id="7f94e-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7f94e-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="7f94e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f94e-102">SYNOPSIS</span></span>
<span data-ttu-id="7f94e-103">CDN uç noktasının kaynak kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="7f94e-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="7f94e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f94e-104">SYNTAX</span></span>

### <span data-ttu-id="7f94e-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f94e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f94e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f94e-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f94e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f94e-107">DESCRIPTION</span></span>
<span data-ttu-id="7f94e-108">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="7f94e-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7f94e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f94e-109">EXAMPLES</span></span>

### <span data-ttu-id="7f94e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f94e-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7f94e-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="7f94e-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="7f94e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f94e-112">PARAMETERS</span></span>

### <span data-ttu-id="7f94e-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f94e-113">-CdnEndpoint</span></span>
<span data-ttu-id="7f94e-114">CDN uç noktası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7f94e-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f94e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f94e-115">-DefaultProfile</span></span>
<span data-ttu-id="7f94e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7f94e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f94e-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7f94e-117">-EndpointName</span></span>
<span data-ttu-id="7f94e-118">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="7f94e-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7f94e-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7f94e-119">-ProfileName</span></span>
<span data-ttu-id="7f94e-120">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="7f94e-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f94e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f94e-121">-ResourceGroupName</span></span>
<span data-ttu-id="7f94e-122">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="7f94e-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f94e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f94e-123">CommonParameters</span></span>
<span data-ttu-id="7f94e-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f94e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f94e-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f94e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f94e-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f94e-126">INPUTS</span></span>

### <span data-ttu-id="7f94e-127">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7f94e-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7f94e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f94e-128">OUTPUTS</span></span>

### <span data-ttu-id="7f94e-129">Microsoft. Azure. Commands. CDN. model. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7f94e-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="7f94e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f94e-130">NOTES</span></span>

## <span data-ttu-id="7f94e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f94e-131">RELATED LINKS</span></span>