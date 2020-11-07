---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763451"
---
# <span data-ttu-id="0c8c6-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0c8c6-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="0c8c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8c6-103">Uygulama ağ geçidinden belirli bir adla güvenilen kök sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="0c8c6-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c8c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c8c6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c8c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c8c6-105">DESCRIPTION</span></span>
<span data-ttu-id="0c8c6-106">**Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet 'ı uygulama ağ geçidinden belirli bir adla güvenilen kök sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="0c8c6-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="0c8c6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c8c6-107">EXAMPLES</span></span>

### <span data-ttu-id="0c8c6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c8c6-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="0c8c6-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0c8c6-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="0c8c6-110">İkinci komut, uygulama ağ geçidinden belirtilen adla güvenilen kök sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="0c8c6-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="0c8c6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c8c6-111">PARAMETERS</span></span>

### <span data-ttu-id="0c8c6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c8c6-112">-ApplicationGateway</span></span>
<span data-ttu-id="0c8c6-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c8c6-113">The applicationGateway</span></span>

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

### <span data-ttu-id="0c8c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8c6-114">-DefaultProfile</span></span>
<span data-ttu-id="0c8c6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c8c6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c8c6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c8c6-116">-Name</span></span>
<span data-ttu-id="0c8c6-117">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="0c8c6-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="0c8c6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8c6-118">CommonParameters</span></span>
<span data-ttu-id="0c8c6-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c8c6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8c6-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c8c6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8c6-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c8c6-121">INPUTS</span></span>

### <span data-ttu-id="0c8c6-122">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0c8c6-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0c8c6-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c8c6-123">OUTPUTS</span></span>

### <span data-ttu-id="0c8c6-124">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0c8c6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="0c8c6-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c8c6-125">NOTES</span></span>

## <span data-ttu-id="0c8c6-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c8c6-126">RELATED LINKS</span></span>
