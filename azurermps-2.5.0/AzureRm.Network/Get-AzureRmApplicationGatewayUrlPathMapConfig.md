---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: dd7ad8110afad4302c393295599ed1ef9d6fd4bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938955"
---
# <span data-ttu-id="b9a30-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b9a30-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="b9a30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9a30-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a30-103">Arka uç sunucu havuzuna yönelik URL yol eşleştirmelerinin dizisini alır.</span><span class="sxs-lookup"><span data-stu-id="b9a30-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9a30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9a30-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9a30-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9a30-105">DESCRIPTION</span></span>
<span data-ttu-id="b9a30-106">**Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna YÖNELIK bir URL yol eşlemeleri dizisini alır.</span><span class="sxs-lookup"><span data-stu-id="b9a30-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b9a30-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9a30-107">EXAMPLES</span></span>

### <span data-ttu-id="b9a30-108">Örnek 1: URL yol haritası yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="b9a30-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="b9a30-109">Bu komut, ağ geçidi adlı uygulama ağ geçidinde bulunan arka uç sunucusundan URL yol haritası yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="b9a30-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="b9a30-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9a30-110">PARAMETERS</span></span>

### <span data-ttu-id="b9a30-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9a30-111">-ApplicationGateway</span></span>
<span data-ttu-id="b9a30-112">Bu cmdlet 'in URL yol haritası yapılandırmasını aldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9a30-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9a30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a30-113">-DefaultProfile</span></span>
<span data-ttu-id="b9a30-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9a30-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9a30-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9a30-115">-Name</span></span>
<span data-ttu-id="b9a30-116">Bu cmdlet 'in yol haritası yapılandırmasını aldığı URL yol haritası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b9a30-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="b9a30-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a30-117">CommonParameters</span></span>
<span data-ttu-id="b9a30-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9a30-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a30-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9a30-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a30-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9a30-120">INPUTS</span></span>

### <span data-ttu-id="b9a30-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9a30-121">PSApplicationGateway</span></span>
<span data-ttu-id="b9a30-122">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b9a30-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b9a30-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9a30-123">OUTPUTS</span></span>

### <span data-ttu-id="b9a30-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="b9a30-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="b9a30-125">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="b9a30-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="b9a30-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9a30-126">NOTES</span></span>

## <span data-ttu-id="b9a30-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9a30-127">RELATED LINKS</span></span>

[<span data-ttu-id="b9a30-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b9a30-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b9a30-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b9a30-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b9a30-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b9a30-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b9a30-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b9a30-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


