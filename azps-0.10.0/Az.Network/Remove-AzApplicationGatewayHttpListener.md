---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: c3bc83f3f38c8a9b3c34e990e5729648a3677dd8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935324"
---
# <span data-ttu-id="5598f-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5598f-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5598f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5598f-102">SYNOPSIS</span></span>
<span data-ttu-id="5598f-103">Uygulama ağ geçidinden HTTP dinleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5598f-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="5598f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5598f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5598f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5598f-105">DESCRIPTION</span></span>
<span data-ttu-id="5598f-106">**Remove-AzApplicationGatewayHttpListener** cmdlet 'ı bir Azure uygulama ağ geçidinden HTTP dinleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5598f-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="5598f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5598f-107">EXAMPLES</span></span>

### <span data-ttu-id="5598f-108">Örnek 1: uygulama ağ geçidi HTTP dinleyicisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="5598f-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="5598f-109">İlk komut bir uygulama ağ geçidi alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5598f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="5598f-110">İkinci komut, $AppGw depolanan uygulama ağ geçidinden Listener02 adlı HTTP dinleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5598f-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="5598f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5598f-111">PARAMETERS</span></span>

### <span data-ttu-id="5598f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5598f-112">-ApplicationGateway</span></span>
<span data-ttu-id="5598f-113">HTTP dinleyicisinin kaldırılacağı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5598f-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="5598f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5598f-114">-DefaultProfile</span></span>
<span data-ttu-id="5598f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5598f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5598f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="5598f-116">-Name</span></span>
<span data-ttu-id="5598f-117">Bu cmdlet 'in kaldırıldığı HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5598f-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5598f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5598f-118">CommonParameters</span></span>
<span data-ttu-id="5598f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5598f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5598f-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5598f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5598f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5598f-121">INPUTS</span></span>

### <span data-ttu-id="5598f-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5598f-122">System.String</span></span>

## <span data-ttu-id="5598f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5598f-123">OUTPUTS</span></span>

### <span data-ttu-id="5598f-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5598f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5598f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5598f-125">NOTES</span></span>

## <span data-ttu-id="5598f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5598f-126">RELATED LINKS</span></span>

[<span data-ttu-id="5598f-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5598f-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5598f-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5598f-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5598f-129">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5598f-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5598f-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5598f-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


