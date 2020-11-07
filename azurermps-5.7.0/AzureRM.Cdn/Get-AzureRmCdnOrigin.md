---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: b4800b77441a82fc0e9966be16f91c9d81a2214a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762171"
---
# <span data-ttu-id="fe359-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="fe359-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="fe359-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe359-102">SYNOPSIS</span></span>
<span data-ttu-id="fe359-103">CDN kaynak sunucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="fe359-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe359-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe359-104">SYNTAX</span></span>

### <span data-ttu-id="fe359-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe359-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe359-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe359-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe359-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe359-107">DESCRIPTION</span></span>
<span data-ttu-id="fe359-108">**Get-Azurermcvseçnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusu ve yapılandırma verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="fe359-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="fe359-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe359-109">EXAMPLES</span></span>

## <span data-ttu-id="fe359-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe359-110">PARAMETERS</span></span>

### <span data-ttu-id="fe359-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe359-111">-CdnEndpoint</span></span>
<span data-ttu-id="fe359-112">Başlangıcının ait olduğu CDN uç noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe359-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe359-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe359-113">-DefaultProfile</span></span>
<span data-ttu-id="fe359-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fe359-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe359-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fe359-115">-EndpointName</span></span>
<span data-ttu-id="fe359-116">Kaynak sunucunun ait olduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe359-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe359-117">-AdName</span><span class="sxs-lookup"><span data-stu-id="fe359-117">-OriginName</span></span>
<span data-ttu-id="fe359-118">Kaynak sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe359-118">Specifies the name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe359-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fe359-119">-ProfileName</span></span>
<span data-ttu-id="fe359-120">Kaynak sunucunun ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe359-120">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe359-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe359-121">-ResourceGroupName</span></span>
<span data-ttu-id="fe359-122">Kaynak sunucunun ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe359-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe359-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe359-123">CommonParameters</span></span>
<span data-ttu-id="fe359-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe359-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe359-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe359-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe359-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe359-126">INPUTS</span></span>

### <span data-ttu-id="fe359-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fe359-127">PSEndpoint</span></span>
<span data-ttu-id="fe359-128">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="fe359-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="fe359-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe359-129">OUTPUTS</span></span>

###  
<span data-ttu-id="fe359-130">Bu cmdlet bir kaynak sunucu nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="fe359-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="fe359-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe359-131">NOTES</span></span>

## <span data-ttu-id="fe359-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe359-132">RELATED LINKS</span></span>

[<span data-ttu-id="fe359-133">Set-Azurermcvseçnorigın</span><span class="sxs-lookup"><span data-stu-id="fe359-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


