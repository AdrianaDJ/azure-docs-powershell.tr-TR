---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 402084acc332102c8a2f003e31e140b175b6f22f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935583"
---
# <span data-ttu-id="c3ff7-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c3ff7-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c3ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="c3ff7-103">Uygulama ağ geçidinin istek yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="c3ff7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3ff7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3ff7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="c3ff7-106">**Get-AzApplicationGatewayRequestRoutingRule** cmdlet 'i, bir uygulama ağ geçidinin istek yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="c3ff7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3ff7-107">EXAMPLES</span></span>

### <span data-ttu-id="c3ff7-108">Örnek 1: belirli bir istek yönlendirme kuralı alma</span><span class="sxs-lookup"><span data-stu-id="c3ff7-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="c3ff7-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c3ff7-110">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden Rule01 adındaki istek yönlendirme kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="c3ff7-111">Örnek 2: istek yönlendirme kuralları listesini alma</span><span class="sxs-lookup"><span data-stu-id="c3ff7-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="c3ff7-112">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="c3ff7-113">İkinci komut, $AppGW adlı değişkende depolanan uygulama ağ geçidinden gelen istek yönlendirme kuralları listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="c3ff7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3ff7-114">PARAMETERS</span></span>

### <span data-ttu-id="c3ff7-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c3ff7-115">-ApplicationGateway</span></span>
<span data-ttu-id="c3ff7-116">İsteğin yönlendirme kuralını içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="c3ff7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3ff7-117">-DefaultProfile</span></span>
<span data-ttu-id="c3ff7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3ff7-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3ff7-119">-Name</span></span>
<span data-ttu-id="c3ff7-120">Bu cmdlet 'in aldığı istek yönlendirme kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="c3ff7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3ff7-121">CommonParameters</span></span>
<span data-ttu-id="c3ff7-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3ff7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3ff7-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3ff7-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3ff7-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3ff7-124">INPUTS</span></span>

### <span data-ttu-id="c3ff7-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c3ff7-125">System.String</span></span>

## <span data-ttu-id="c3ff7-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3ff7-126">OUTPUTS</span></span>

### <span data-ttu-id="c3ff7-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c3ff7-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c3ff7-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3ff7-128">NOTES</span></span>

## <span data-ttu-id="c3ff7-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3ff7-129">RELATED LINKS</span></span>

[<span data-ttu-id="c3ff7-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c3ff7-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c3ff7-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c3ff7-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c3ff7-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c3ff7-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c3ff7-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c3ff7-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


