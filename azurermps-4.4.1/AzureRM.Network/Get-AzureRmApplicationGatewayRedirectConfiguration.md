---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 66da90ea590c4d2359dbe7e703667f9fe7189fba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762207"
---
# <span data-ttu-id="22cf5-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="22cf5-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="22cf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="22cf5-103">Uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="22cf5-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22cf5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22cf5-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22cf5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22cf5-105">DESCRIPTION</span></span>
<span data-ttu-id="22cf5-106">**Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet 'ı uygulama ağ geçidinden varolan bir yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="22cf5-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="22cf5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22cf5-107">EXAMPLES</span></span>

### <span data-ttu-id="22cf5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="22cf5-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="22cf5-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="22cf5-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="22cf5-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Redirect01 adındaki yeniden yönlendirme yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="22cf5-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="22cf5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22cf5-111">PARAMETERS</span></span>

### <span data-ttu-id="22cf5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22cf5-112">-ApplicationGateway</span></span>
<span data-ttu-id="22cf5-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22cf5-113">The applicationGateway</span></span>

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

### <span data-ttu-id="22cf5-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="22cf5-114">-Name</span></span>
<span data-ttu-id="22cf5-115">İstek yönlendirme kuralının adı</span><span class="sxs-lookup"><span data-stu-id="22cf5-115">The name of the request routing rule</span></span>

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

### <span data-ttu-id="22cf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cf5-116">-DefaultProfile</span></span>
<span data-ttu-id="22cf5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22cf5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22cf5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cf5-118">CommonParameters</span></span>
<span data-ttu-id="22cf5-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22cf5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cf5-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22cf5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cf5-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22cf5-121">INPUTS</span></span>

### <span data-ttu-id="22cf5-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22cf5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22cf5-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22cf5-123">OUTPUTS</span></span>

### <span data-ttu-id="22cf5-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="22cf5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="22cf5-125">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22cf5-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="22cf5-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22cf5-126">NOTES</span></span>

## <span data-ttu-id="22cf5-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22cf5-127">RELATED LINKS</span></span>

