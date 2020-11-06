---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: a28aa5b0f611c8014ae2849e0dee6fe48aedfbe1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592085"
---
# <span data-ttu-id="48478-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="48478-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="48478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48478-102">SYNOPSIS</span></span>
<span data-ttu-id="48478-103">Uygulama ağ geçidinin HTTP dinleyicisini alır.</span><span class="sxs-lookup"><span data-stu-id="48478-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48478-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48478-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48478-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48478-105">DESCRIPTION</span></span>
<span data-ttu-id="48478-106">**Get-AzureRmApplicationGatewayHttpListener** cmdlet 'i bir uygulama ağ geçidinin HTTP dinleyicisini alır.</span><span class="sxs-lookup"><span data-stu-id="48478-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="48478-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48478-107">EXAMPLES</span></span>

### <span data-ttu-id="48478-108">Örnek 1: belirli bir HTTP dinleyicisi alma</span><span class="sxs-lookup"><span data-stu-id="48478-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="48478-109">Bu komut, Listener01 adlı bir HTTP dinleyicisi alır.</span><span class="sxs-lookup"><span data-stu-id="48478-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="48478-110">Örnek 2: HTTP dinleyicilerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="48478-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="48478-111">Bu komut, HTTP dinleyicilerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="48478-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="48478-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48478-112">PARAMETERS</span></span>

### <span data-ttu-id="48478-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48478-113">-ApplicationGateway</span></span>
<span data-ttu-id="48478-114">HTTP dinleyicisini içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48478-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="48478-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48478-115">-DefaultProfile</span></span>
<span data-ttu-id="48478-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48478-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48478-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="48478-117">-Name</span></span>
<span data-ttu-id="48478-118">Bu cmdlet 'in aldığı HTTP dinleyicisi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48478-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="48478-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48478-119">CommonParameters</span></span>
<span data-ttu-id="48478-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48478-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48478-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48478-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48478-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48478-122">INPUTS</span></span>

### <span data-ttu-id="48478-123">System. String</span><span class="sxs-lookup"><span data-stu-id="48478-123">System.String</span></span>

## <span data-ttu-id="48478-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48478-124">OUTPUTS</span></span>

### <span data-ttu-id="48478-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="48478-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="48478-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48478-126">NOTES</span></span>

## <span data-ttu-id="48478-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48478-127">RELATED LINKS</span></span>

[<span data-ttu-id="48478-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="48478-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="48478-129">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="48478-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="48478-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="48478-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="48478-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="48478-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


