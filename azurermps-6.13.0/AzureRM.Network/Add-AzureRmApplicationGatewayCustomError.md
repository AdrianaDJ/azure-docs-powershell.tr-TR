---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b56c358a208683e513844e36e561efa9e76cbede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588085"
---
# <span data-ttu-id="ac0ec-101">Add-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ac0ec-101">Add-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="ac0ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0ec-103">Uygulama ağ geçidine özel bir hata ekler.</span><span class="sxs-lookup"><span data-stu-id="ac0ec-103">Adds a custom error to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac0ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac0ec-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac0ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac0ec-105">DESCRIPTION</span></span>
<span data-ttu-id="ac0ec-106">**Add-AzureRmApplicationGatewayCustomError** cmdlet 'i uygulama ağ geçidine özel bir hata ekler.</span><span class="sxs-lookup"><span data-stu-id="ac0ec-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="ac0ec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac0ec-107">EXAMPLES</span></span>

### <span data-ttu-id="ac0ec-108">Örnek 1: uygulama ağ geçidi düzeyine özel hata ekler</span><span class="sxs-lookup"><span data-stu-id="ac0ec-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="ac0ec-109">Bu komut, uygulama ağ geçidi $appgw http durum kodu 502 özel hatasını ekler ve güncelleştirilmiş ağ geçidini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ac0ec-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="ac0ec-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac0ec-110">PARAMETERS</span></span>

### <span data-ttu-id="ac0ec-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac0ec-111">-ApplicationGateway</span></span>
<span data-ttu-id="ac0ec-112">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="ac0ec-112">The Application Gateway</span></span>

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

### <span data-ttu-id="ac0ec-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="ac0ec-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="ac0ec-114">Uygulama ağ geçidi müşteri hatasının hata sayfası URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="ac0ec-114">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac0ec-115">-DefaultProfile</span></span>
<span data-ttu-id="ac0ec-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ac0ec-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac0ec-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="ac0ec-117">-StatusCode</span></span>
<span data-ttu-id="ac0ec-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="ac0ec-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0ec-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0ec-119">CommonParameters</span></span>
<span data-ttu-id="ac0ec-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac0ec-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0ec-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac0ec-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0ec-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac0ec-122">INPUTS</span></span>

### <span data-ttu-id="ac0ec-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac0ec-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac0ec-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac0ec-124">OUTPUTS</span></span>

### <span data-ttu-id="ac0ec-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac0ec-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac0ec-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac0ec-126">NOTES</span></span>

## <span data-ttu-id="ac0ec-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac0ec-127">RELATED LINKS</span></span>
