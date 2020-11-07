---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: eeab1f5699af5de737bc1e0390c35d387acfdd98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939093"
---
# <span data-ttu-id="3dc7d-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3dc7d-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="3dc7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dc7d-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc7d-103">Bir Azure uygulaması ağ geçidinden SSL sertifikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3dc7d-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dc7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3dc7d-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dc7d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3dc7d-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc7d-106">**Remove-AzureRmApplicationGatewaySslCertificate** cmdlet 'i, bir Azure uygulama ağ geçidinden güvenli yuva KATMANı (SSL) sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3dc7d-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="3dc7d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3dc7d-107">EXAMPLES</span></span>

### <span data-ttu-id="3dc7d-108">Örnek 1: uygulama ağ geçidinden SSL sertifikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="3dc7d-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="3dc7d-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve sonucu $AppGW adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="3dc7d-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="3dc7d-110">İkinci komut, Cert02 adlı SSL sertifikasını $AppGW değişkeninde depolanan uygulama ağ geçidinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3dc7d-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="3dc7d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3dc7d-111">PARAMETERS</span></span>

### <span data-ttu-id="3dc7d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3dc7d-112">-ApplicationGateway</span></span>
<span data-ttu-id="3dc7d-113">Bu cmdlet 'in SSL sertifikasını kaldırdığı uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dc7d-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="3dc7d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc7d-114">-DefaultProfile</span></span>
<span data-ttu-id="3dc7d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3dc7d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dc7d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="3dc7d-116">-Name</span></span>
<span data-ttu-id="3dc7d-117">Bu cmdlet 'in kaldırdığı SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dc7d-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3dc7d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc7d-118">CommonParameters</span></span>
<span data-ttu-id="3dc7d-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3dc7d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc7d-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc7d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc7d-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3dc7d-121">INPUTS</span></span>

### <span data-ttu-id="3dc7d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="3dc7d-122">System.String</span></span>

## <span data-ttu-id="3dc7d-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3dc7d-123">OUTPUTS</span></span>

### <span data-ttu-id="3dc7d-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3dc7d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3dc7d-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3dc7d-125">NOTES</span></span>

## <span data-ttu-id="3dc7d-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3dc7d-126">RELATED LINKS</span></span>

[<span data-ttu-id="3dc7d-127">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3dc7d-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3dc7d-128">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3dc7d-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3dc7d-129">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3dc7d-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="3dc7d-130">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="3dc7d-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


