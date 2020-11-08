---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279537"
---
# <span data-ttu-id="6c6b7-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="6c6b7-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="6c6b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="6c6b7-103">CDN kaynak sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="6c6b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c6b7-104">SYNTAX</span></span>

### <span data-ttu-id="6c6b7-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6c6b7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c6b7-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="6c6b7-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c6b7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c6b7-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c6b7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c6b7-108">DESCRIPTION</span></span>
<span data-ttu-id="6c6b7-109">**Get-Azcdnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusu ve yapılandırma verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="6c6b7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c6b7-110">EXAMPLES</span></span>

## <span data-ttu-id="6c6b7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c6b7-111">PARAMETERS</span></span>

### <span data-ttu-id="6c6b7-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c6b7-112">-CdnEndpoint</span></span>
<span data-ttu-id="6c6b7-113">Başlangıcının ait olduğu CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="6c6b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c6b7-114">-DefaultProfile</span></span>
<span data-ttu-id="6c6b7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6c6b7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c6b7-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6c6b7-116">-EndpointName</span></span>
<span data-ttu-id="6c6b7-117">Kaynak sunucunun ait olduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="6c6b7-118">-AdName</span><span class="sxs-lookup"><span data-stu-id="6c6b7-118">-OriginName</span></span>
<span data-ttu-id="6c6b7-119">Kaynak sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="6c6b7-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6c6b7-120">-ProfileName</span></span>
<span data-ttu-id="6c6b7-121">Kaynak sunucunun ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="6c6b7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c6b7-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c6b7-123">Kaynak sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="6c6b7-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6c6b7-124">-ResourceId</span></span>
<span data-ttu-id="6c6b7-125">Azure CDN kaynağının kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c6b7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c6b7-126">CommonParameters</span></span>
<span data-ttu-id="6c6b7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c6b7-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6c6b7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c6b7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c6b7-129">INPUTS</span></span>

### <span data-ttu-id="6c6b7-130">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="6c6b7-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="6c6b7-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c6b7-131">OUTPUTS</span></span>

### <span data-ttu-id="6c6b7-132">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="6c6b7-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="6c6b7-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c6b7-133">NOTES</span></span>

## <span data-ttu-id="6c6b7-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c6b7-134">RELATED LINKS</span></span>

[<span data-ttu-id="6c6b7-135">Set-Azcdnorigın</span><span class="sxs-lookup"><span data-stu-id="6c6b7-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


