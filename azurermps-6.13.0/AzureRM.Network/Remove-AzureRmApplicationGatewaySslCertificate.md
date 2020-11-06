---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 865b9a576219cbaf7d938094baf923c497436e07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589451"
---
# <span data-ttu-id="12215-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12215-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="12215-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12215-102">SYNOPSIS</span></span>
<span data-ttu-id="12215-103">Bir Azure uygulaması ağ geçidinden SSL sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="12215-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12215-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12215-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12215-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12215-105">DESCRIPTION</span></span>
<span data-ttu-id="12215-106">**Remove-AzureRmApplicationGatewaySslCertificate** cmdlet 'i, bir Azure uygulama ağ geçidinden güvenli yuva KATMANı (SSL) sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="12215-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="12215-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12215-107">EXAMPLES</span></span>

### <span data-ttu-id="12215-108">Örnek 1: uygulama ağ geçidinden SSL sertifikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="12215-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="12215-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="12215-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="12215-110">İkinci komut, Cert02 adlı SSL sertifikasını $AppGW değişkeninde depolanan uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="12215-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="12215-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12215-111">PARAMETERS</span></span>

### <span data-ttu-id="12215-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12215-112">-ApplicationGateway</span></span>
<span data-ttu-id="12215-113">Bu cmdlet 'in SSL sertifikasını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="12215-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="12215-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12215-114">-DefaultProfile</span></span>
<span data-ttu-id="12215-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12215-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12215-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="12215-116">-Name</span></span>
<span data-ttu-id="12215-117">Bu cmdlet 'in kaldırdığı SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12215-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12215-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12215-118">CommonParameters</span></span>
<span data-ttu-id="12215-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12215-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12215-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12215-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12215-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12215-121">INPUTS</span></span>

### <span data-ttu-id="12215-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12215-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="12215-123">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="12215-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="12215-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12215-124">OUTPUTS</span></span>

### <span data-ttu-id="12215-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="12215-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="12215-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12215-126">NOTES</span></span>

## <span data-ttu-id="12215-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12215-127">RELATED LINKS</span></span>

[<span data-ttu-id="12215-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12215-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="12215-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12215-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="12215-130">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12215-130">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="12215-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="12215-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


