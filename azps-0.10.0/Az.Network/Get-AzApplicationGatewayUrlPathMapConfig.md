---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 92d970d87b79b1a392b6da73c567d6e8445cfd90
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935568"
---
# <span data-ttu-id="692e9-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="692e9-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="692e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="692e9-102">SYNOPSIS</span></span>
<span data-ttu-id="692e9-103">Arka uç sunucu havuzuna yönelik URL yol eşleştirmelerinin dizisini alır.</span><span class="sxs-lookup"><span data-stu-id="692e9-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="692e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="692e9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="692e9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="692e9-105">DESCRIPTION</span></span>
<span data-ttu-id="692e9-106">**Get-AzApplicationGatewayURLPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna YÖNELIK bir URL yol eşlemeleri dizisini alır.</span><span class="sxs-lookup"><span data-stu-id="692e9-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="692e9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="692e9-107">EXAMPLES</span></span>

### <span data-ttu-id="692e9-108">Örnek 1: URL yol haritası yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="692e9-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="692e9-109">Bu komut, ağ geçidi adlı uygulama ağ geçidinde bulunan arka uç sunucusundan URL yol haritası yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="692e9-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="692e9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="692e9-110">PARAMETERS</span></span>

### <span data-ttu-id="692e9-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="692e9-111">-ApplicationGateway</span></span>
<span data-ttu-id="692e9-112">Bu cmdlet 'in URL yol haritası yapılandırmasını aldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="692e9-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="692e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692e9-113">-DefaultProfile</span></span>
<span data-ttu-id="692e9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="692e9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="692e9-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="692e9-115">-Name</span></span>
<span data-ttu-id="692e9-116">Bu cmdlet 'in yol haritası yapılandırmasını aldığı URL yol haritası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="692e9-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="692e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692e9-117">CommonParameters</span></span>
<span data-ttu-id="692e9-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="692e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692e9-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="692e9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692e9-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="692e9-120">INPUTS</span></span>

### <span data-ttu-id="692e9-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="692e9-121">PSApplicationGateway</span></span>
<span data-ttu-id="692e9-122">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="692e9-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="692e9-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="692e9-123">OUTPUTS</span></span>

### <span data-ttu-id="692e9-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="692e9-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="692e9-125">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="692e9-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="692e9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="692e9-126">NOTES</span></span>

## <span data-ttu-id="692e9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="692e9-127">RELATED LINKS</span></span>

[<span data-ttu-id="692e9-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="692e9-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="692e9-129">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="692e9-129">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="692e9-130">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="692e9-130">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="692e9-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="692e9-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


