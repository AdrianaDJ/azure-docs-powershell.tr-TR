---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: d254008ef4d6d4fc6e16f9a543a38518a6537a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764990"
---
# <span data-ttu-id="3579a-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3579a-101">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="3579a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3579a-102">SYNOPSIS</span></span>
<span data-ttu-id="3579a-103">Uygulama ağ geçidinin istek yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="3579a-103">Gets the request routing rule of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3579a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3579a-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3579a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3579a-105">DESCRIPTION</span></span>
<span data-ttu-id="3579a-106">**Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet 'i, bir uygulama ağ geçidinin istek yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="3579a-106">The **Get-AzureRmApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="3579a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3579a-107">EXAMPLES</span></span>

### <span data-ttu-id="3579a-108">Örnek 1: belirli bir istek yönlendirme kuralı alma</span><span class="sxs-lookup"><span data-stu-id="3579a-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzureRmApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="3579a-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3579a-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="3579a-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Rule01 adındaki istek yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="3579a-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="3579a-111">Örnek 2: istek yönlendirme kuralları listesini alma</span><span class="sxs-lookup"><span data-stu-id="3579a-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="3579a-112">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3579a-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="3579a-113">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden gelen istek yönlendirme kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="3579a-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="3579a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3579a-114">PARAMETERS</span></span>

### <span data-ttu-id="3579a-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3579a-115">-ApplicationGateway</span></span>
<span data-ttu-id="3579a-116">İsteğin yönlendirme kuralını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3579a-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="3579a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3579a-117">-DefaultProfile</span></span>
<span data-ttu-id="3579a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3579a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3579a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3579a-119">-Name</span></span>
<span data-ttu-id="3579a-120">Bu cmdlet 'in aldığı istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3579a-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="3579a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3579a-121">CommonParameters</span></span>
<span data-ttu-id="3579a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3579a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3579a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3579a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3579a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3579a-124">INPUTS</span></span>

### <span data-ttu-id="3579a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3579a-125">System.String</span></span>

## <span data-ttu-id="3579a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3579a-126">OUTPUTS</span></span>

### <span data-ttu-id="3579a-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3579a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="3579a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3579a-128">NOTES</span></span>

## <span data-ttu-id="3579a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3579a-129">RELATED LINKS</span></span>

[<span data-ttu-id="3579a-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3579a-130">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3579a-131">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3579a-131">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3579a-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3579a-132">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="3579a-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="3579a-133">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


