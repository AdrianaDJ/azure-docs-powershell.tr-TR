---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 7b5f37cb42d128cbf44294520419c8f4d09124fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932295"
---
# <span data-ttu-id="0a497-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a497-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0a497-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a497-102">SYNOPSIS</span></span>
<span data-ttu-id="0a497-103">Bir Azure uygulaması ağ geçidinden SSL sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a497-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="0a497-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a497-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a497-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a497-105">DESCRIPTION</span></span>
<span data-ttu-id="0a497-106">**Remove-AzApplicationGatewaySslCertificate** cmdlet 'i, bir Azure uygulama ağ geçidinden güvenli yuva KATMANı (SSL) sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a497-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="0a497-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a497-107">EXAMPLES</span></span>

### <span data-ttu-id="0a497-108">Örnek 1: uygulama ağ geçidinden SSL sertifikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="0a497-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="0a497-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="0a497-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="0a497-110">İkinci komut, Cert02 adlı SSL sertifikasını $AppGW değişkeninde depolanan uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a497-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="0a497-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a497-111">PARAMETERS</span></span>

### <span data-ttu-id="0a497-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a497-112">-ApplicationGateway</span></span>
<span data-ttu-id="0a497-113">Bu cmdlet 'in SSL sertifikasını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a497-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="0a497-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a497-114">-DefaultProfile</span></span>
<span data-ttu-id="0a497-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a497-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a497-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a497-116">-Name</span></span>
<span data-ttu-id="0a497-117">Bu cmdlet 'in kaldırdığı SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a497-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0a497-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a497-118">CommonParameters</span></span>
<span data-ttu-id="0a497-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a497-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a497-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a497-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a497-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a497-121">INPUTS</span></span>

### <span data-ttu-id="0a497-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a497-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a497-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a497-123">OUTPUTS</span></span>

### <span data-ttu-id="0a497-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a497-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0a497-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a497-125">NOTES</span></span>

## <span data-ttu-id="0a497-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a497-126">RELATED LINKS</span></span>

[<span data-ttu-id="0a497-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a497-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0a497-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a497-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0a497-129">Yeni-Azapplicationgatewaysslsertifikası</span><span class="sxs-lookup"><span data-stu-id="0a497-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0a497-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a497-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


