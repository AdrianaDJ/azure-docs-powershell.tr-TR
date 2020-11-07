---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ac85a308b73d822846a2f2a0a7b9ddf9ccc05cbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931791"
---
# <span data-ttu-id="134af-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="134af-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="134af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="134af-102">SYNOPSIS</span></span>
<span data-ttu-id="134af-103">Arka uç sunucu havuzuna yönelik URL yol eşleştirmelerinin dizisini alır.</span><span class="sxs-lookup"><span data-stu-id="134af-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="134af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="134af-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="134af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="134af-105">DESCRIPTION</span></span>
<span data-ttu-id="134af-106">**Get-AzApplicationGatewayURLPathMapConfig** cmdlet 'i, arka uç sunucu havuzuna YÖNELIK bir URL yol eşlemeleri dizisini alır.</span><span class="sxs-lookup"><span data-stu-id="134af-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="134af-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="134af-107">EXAMPLES</span></span>

### <span data-ttu-id="134af-108">Örnek 1: URL yol haritası yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="134af-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="134af-109">Bu komut, ağ geçidi adlı uygulama ağ geçidinde bulunan arka uç sunucusundan URL yol haritası yapılandırmalarını alır.</span><span class="sxs-lookup"><span data-stu-id="134af-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="134af-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="134af-110">PARAMETERS</span></span>

### <span data-ttu-id="134af-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="134af-111">-ApplicationGateway</span></span>
<span data-ttu-id="134af-112">Bu cmdlet 'in URL yol haritası yapılandırmasını aldığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="134af-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="134af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134af-113">-DefaultProfile</span></span>
<span data-ttu-id="134af-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="134af-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="134af-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="134af-115">-Name</span></span>
<span data-ttu-id="134af-116">Bu cmdlet 'in yol haritası yapılandırmasını aldığı URL yol haritası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="134af-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="134af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134af-117">CommonParameters</span></span>
<span data-ttu-id="134af-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="134af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134af-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="134af-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134af-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="134af-120">INPUTS</span></span>

### <span data-ttu-id="134af-121">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="134af-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="134af-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="134af-122">OUTPUTS</span></span>

### <span data-ttu-id="134af-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="134af-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="134af-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="134af-124">NOTES</span></span>

## <span data-ttu-id="134af-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="134af-125">RELATED LINKS</span></span>

[<span data-ttu-id="134af-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="134af-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="134af-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="134af-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="134af-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="134af-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="134af-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="134af-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)

