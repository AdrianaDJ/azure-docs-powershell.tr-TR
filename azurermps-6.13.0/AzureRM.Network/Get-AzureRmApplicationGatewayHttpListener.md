---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 0cb29f9ad00c2412d9ab492bba780e977ef6b571
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764637"
---
# <span data-ttu-id="7660f-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7660f-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7660f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7660f-102">SYNOPSIS</span></span>
<span data-ttu-id="7660f-103">Uygulama ağ geçidinin HTTP dinleyicisini alır.</span><span class="sxs-lookup"><span data-stu-id="7660f-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7660f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7660f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7660f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7660f-105">DESCRIPTION</span></span>
<span data-ttu-id="7660f-106">**Get-AzureRmApplicationGatewayHttpListener** cmdlet 'i bir uygulama ağ geçidinin HTTP dinleyicisini alır.</span><span class="sxs-lookup"><span data-stu-id="7660f-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="7660f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7660f-107">EXAMPLES</span></span>

### <span data-ttu-id="7660f-108">Örnek 1: belirli bir HTTP dinleyicisi alma</span><span class="sxs-lookup"><span data-stu-id="7660f-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="7660f-109">Bu komut, Listener01 adlı bir HTTP dinleyicisi alır.</span><span class="sxs-lookup"><span data-stu-id="7660f-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="7660f-110">Örnek 2: HTTP dinleyicilerinin listesini alma</span><span class="sxs-lookup"><span data-stu-id="7660f-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="7660f-111">Bu komut, HTTP dinleyicilerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="7660f-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="7660f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7660f-112">PARAMETERS</span></span>

### <span data-ttu-id="7660f-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7660f-113">-ApplicationGateway</span></span>
<span data-ttu-id="7660f-114">HTTP dinleyicisini içeren uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7660f-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="7660f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7660f-115">-DefaultProfile</span></span>
<span data-ttu-id="7660f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7660f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7660f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="7660f-117">-Name</span></span>
<span data-ttu-id="7660f-118">Bu cmdlet 'in aldığı HTTP dinleyicisi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7660f-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="7660f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7660f-119">CommonParameters</span></span>
<span data-ttu-id="7660f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7660f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7660f-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7660f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7660f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7660f-122">INPUTS</span></span>

### <span data-ttu-id="7660f-123">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7660f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="7660f-124">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7660f-124">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="7660f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7660f-125">OUTPUTS</span></span>

### <span data-ttu-id="7660f-126">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7660f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7660f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7660f-127">NOTES</span></span>

## <span data-ttu-id="7660f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7660f-128">RELATED LINKS</span></span>

[<span data-ttu-id="7660f-129">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7660f-129">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7660f-130">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7660f-130">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7660f-131">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7660f-131">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7660f-132">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7660f-132">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


