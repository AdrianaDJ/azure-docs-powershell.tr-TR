---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: aba554d2c81e4fce438e9bd6e10a8dfec63da465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595021"
---
# <span data-ttu-id="791e1-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="791e1-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="791e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="791e1-102">SYNOPSIS</span></span>
<span data-ttu-id="791e1-103">CDN kaynak sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="791e1-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="791e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="791e1-104">SYNTAX</span></span>

### <span data-ttu-id="791e1-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="791e1-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="791e1-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="791e1-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="791e1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="791e1-107">DESCRIPTION</span></span>
<span data-ttu-id="791e1-108">**Get-Azurermcvseçnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusu ve yapılandırma verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="791e1-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="791e1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="791e1-109">EXAMPLES</span></span>

## <span data-ttu-id="791e1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="791e1-110">PARAMETERS</span></span>

### <span data-ttu-id="791e1-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="791e1-111">-CdnEndpoint</span></span>
<span data-ttu-id="791e1-112">Başlangıcının ait olduğu CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="791e1-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="791e1-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="791e1-113">-EndpointName</span></span>
<span data-ttu-id="791e1-114">Kaynak sunucunun ait olduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="791e1-114">Specifies the name of the endpoint to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791e1-115">-AdName</span><span class="sxs-lookup"><span data-stu-id="791e1-115">-OriginName</span></span>
<span data-ttu-id="791e1-116">Kaynak sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="791e1-116">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="791e1-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="791e1-117">-ProfileName</span></span>
<span data-ttu-id="791e1-118">Kaynak sunucunun ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="791e1-118">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="791e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="791e1-120">Kaynak sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="791e1-120">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="791e1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791e1-121">-DefaultProfile</span></span>
<span data-ttu-id="791e1-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="791e1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="791e1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791e1-123">CommonParameters</span></span>
<span data-ttu-id="791e1-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="791e1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791e1-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="791e1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791e1-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="791e1-126">INPUTS</span></span>

### <span data-ttu-id="791e1-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="791e1-127">PSEndpoint</span></span>
<span data-ttu-id="791e1-128">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="791e1-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="791e1-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="791e1-129">OUTPUTS</span></span>

###  
<span data-ttu-id="791e1-130">Bu cmdlet bir kaynak sunucu nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="791e1-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="791e1-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="791e1-131">NOTES</span></span>

## <span data-ttu-id="791e1-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="791e1-132">RELATED LINKS</span></span>

[<span data-ttu-id="791e1-133">Set-Azurermcvseçnorigın</span><span class="sxs-lookup"><span data-stu-id="791e1-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


