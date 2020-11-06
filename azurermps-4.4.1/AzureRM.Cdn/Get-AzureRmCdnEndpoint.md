---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: 088f9ff5ee1c41b4529353b2740bf9ef1fa8e33c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592663"
---
# <span data-ttu-id="5a92d-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a92d-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="5a92d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a92d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a92d-103">CDN uç noktasını alır.</span><span class="sxs-lookup"><span data-stu-id="5a92d-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a92d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a92d-104">SYNTAX</span></span>

### <span data-ttu-id="5a92d-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a92d-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a92d-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="5a92d-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a92d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a92d-107">DESCRIPTION</span></span>
<span data-ttu-id="5a92d-108">**Get-AzureRMCdnEndpoint** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) uç noktasını ve ilişkili yapılandırma verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a92d-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="5a92d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a92d-109">EXAMPLES</span></span>

## <span data-ttu-id="5a92d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a92d-110">PARAMETERS</span></span>

### <span data-ttu-id="5a92d-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5a92d-111">-CdnProfile</span></span>
<span data-ttu-id="5a92d-112">Uç noktanın ait olduğu CDN profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a92d-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a92d-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5a92d-113">-EndpointName</span></span>
<span data-ttu-id="5a92d-114">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a92d-114">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="5a92d-115">Uç noktasının adı uç noktasının ana bilgisayar adı değildir.</span><span class="sxs-lookup"><span data-stu-id="5a92d-115">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="5a92d-116">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5a92d-116">-ProfileName</span></span>
<span data-ttu-id="5a92d-117">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a92d-117">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5a92d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a92d-118">-ResourceGroupName</span></span>
<span data-ttu-id="5a92d-119">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a92d-119">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5a92d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a92d-120">-DefaultProfile</span></span>
<span data-ttu-id="5a92d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a92d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a92d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a92d-122">CommonParameters</span></span>
<span data-ttu-id="5a92d-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a92d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a92d-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a92d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a92d-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a92d-125">INPUTS</span></span>

### <span data-ttu-id="5a92d-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="5a92d-126">PSProfile</span></span>
<span data-ttu-id="5a92d-127">' CdnProfile ' parametresi ardışık düzenin ' PSProfile ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5a92d-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="5a92d-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a92d-128">OUTPUTS</span></span>

###  
<span data-ttu-id="5a92d-129">Bu cmdlet bir uç nokta nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="5a92d-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="5a92d-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a92d-130">NOTES</span></span>

## <span data-ttu-id="5a92d-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a92d-131">RELATED LINKS</span></span>

[<span data-ttu-id="5a92d-132">Yeni-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a92d-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5a92d-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a92d-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5a92d-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a92d-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5a92d-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a92d-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5a92d-136">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5a92d-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


