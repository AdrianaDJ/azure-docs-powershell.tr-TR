---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f770d50675cf853d84a5b1ea741d4972aaaeeca4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761414"
---
# <span data-ttu-id="2d852-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="2d852-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="2d852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d852-102">SYNOPSIS</span></span>
<span data-ttu-id="2d852-103">CDN kaynak sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="2d852-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="2d852-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d852-104">SYNTAX</span></span>

### <span data-ttu-id="2d852-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2d852-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d852-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d852-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d852-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d852-107">DESCRIPTION</span></span>
<span data-ttu-id="2d852-108">**Get-Azcdnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusu ve yapılandırma verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="2d852-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="2d852-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d852-109">EXAMPLES</span></span>

## <span data-ttu-id="2d852-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d852-110">PARAMETERS</span></span>

### <span data-ttu-id="2d852-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d852-111">-CdnEndpoint</span></span>
<span data-ttu-id="2d852-112">Başlangıcının ait olduğu CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d852-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="2d852-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d852-113">-DefaultProfile</span></span>
<span data-ttu-id="2d852-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2d852-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d852-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2d852-115">-EndpointName</span></span>
<span data-ttu-id="2d852-116">Kaynak sunucunun ait olduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d852-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2d852-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="2d852-117">-OriginName</span></span>
<span data-ttu-id="2d852-118">Kaynak sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d852-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="2d852-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2d852-119">-ProfileName</span></span>
<span data-ttu-id="2d852-120">Kaynak sunucunun ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d852-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2d852-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d852-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d852-122">Kaynak sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d852-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="2d852-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d852-123">CommonParameters</span></span>
<span data-ttu-id="2d852-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d852-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d852-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d852-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d852-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d852-126">INPUTS</span></span>

### <span data-ttu-id="2d852-127">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="2d852-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="2d852-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d852-128">OUTPUTS</span></span>

### <span data-ttu-id="2d852-129">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="2d852-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="2d852-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d852-130">NOTES</span></span>

## <span data-ttu-id="2d852-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d852-131">RELATED LINKS</span></span>

[<span data-ttu-id="2d852-132">Set-Azcdnorigın</span><span class="sxs-lookup"><span data-stu-id="2d852-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


