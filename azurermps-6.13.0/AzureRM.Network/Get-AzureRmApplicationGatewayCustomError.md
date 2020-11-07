---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b2f748bca68bff772026237f3bb6205ca6bc1923
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764344"
---
# <span data-ttu-id="a35c7-101">Get-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a35c7-101">Get-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a35c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a35c7-102">SYNOPSIS</span></span>
<span data-ttu-id="a35c7-103">Uygulama ağ geçidinden özel hataları alır.</span><span class="sxs-lookup"><span data-stu-id="a35c7-103">Gets custom error(s) from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a35c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a35c7-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a35c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a35c7-105">DESCRIPTION</span></span>
<span data-ttu-id="a35c7-106">**Get-AzureRmApplicationGatewayCustomError** cmdlet 'i uygulama ağ geçidinden özel hataları alır.</span><span class="sxs-lookup"><span data-stu-id="a35c7-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="a35c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a35c7-107">EXAMPLES</span></span>

### <span data-ttu-id="a35c7-108">Örnek 1: uygulama ağ geçidinde özel hata alır</span><span class="sxs-lookup"><span data-stu-id="a35c7-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="a35c7-109">Bu komut, uygulama ağ geçidi $appgw http durum kodu 502 özel hatasını alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="a35c7-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="a35c7-110">Örnek 2: uygulama ağ geçidinde tüm özel hataların listesini alır</span><span class="sxs-lookup"><span data-stu-id="a35c7-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="a35c7-111">Bu komut, uygulama ağ geçidi $appgw tüm özel hataların listesini alır ve döndürür.</span><span class="sxs-lookup"><span data-stu-id="a35c7-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="a35c7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a35c7-112">PARAMETERS</span></span>

### <span data-ttu-id="a35c7-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a35c7-113">-ApplicationGateway</span></span>
<span data-ttu-id="a35c7-114">Uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="a35c7-114">The Application Gateway</span></span>

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

### <span data-ttu-id="a35c7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a35c7-115">-DefaultProfile</span></span>
<span data-ttu-id="a35c7-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a35c7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a35c7-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="a35c7-117">-StatusCode</span></span>
<span data-ttu-id="a35c7-118">Uygulama ağ geçidi müşteri hatasının durum kodu.</span><span class="sxs-lookup"><span data-stu-id="a35c7-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="a35c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a35c7-119">CommonParameters</span></span>
<span data-ttu-id="a35c7-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a35c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a35c7-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a35c7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a35c7-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a35c7-122">INPUTS</span></span>

### <span data-ttu-id="a35c7-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a35c7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a35c7-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a35c7-124">OUTPUTS</span></span>

### <span data-ttu-id="a35c7-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a35c7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="a35c7-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a35c7-126">NOTES</span></span>

## <span data-ttu-id="a35c7-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a35c7-127">RELATED LINKS</span></span>
