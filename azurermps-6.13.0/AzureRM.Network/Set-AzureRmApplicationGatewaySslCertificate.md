---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: c45a829414fd1009f97c99844705e9affab0ef30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587223"
---
# <span data-ttu-id="48852-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="48852-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="48852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48852-102">SYNOPSIS</span></span>
<span data-ttu-id="48852-103">SSL sertifikasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="48852-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48852-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48852-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48852-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48852-105">DESCRIPTION</span></span>
<span data-ttu-id="48852-106">**Set-AzureRmApplicationGatewaySslCertificate** cmdlet 'ı, SSL sertifikasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="48852-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="48852-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48852-107">EXAMPLES</span></span>

### <span data-ttu-id="48852-108">Örnek 1: SSL sertifikasının hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="48852-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="48852-109">Bu komut, ApplicationGateway01 adındaki uygulama ağ geçidinden SSL sertifikasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="48852-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="48852-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48852-110">PARAMETERS</span></span>

### <span data-ttu-id="48852-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48852-111">-ApplicationGateway</span></span>
<span data-ttu-id="48852-112">Güvenli Yuva Katmanı (SSL) sertifikasının ilişkili olduğu uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="48852-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="48852-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="48852-113">-CertificateFile</span></span>
<span data-ttu-id="48852-114">SSL sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="48852-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="48852-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48852-115">-DefaultProfile</span></span>
<span data-ttu-id="48852-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48852-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48852-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="48852-117">-Name</span></span>
<span data-ttu-id="48852-118">SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48852-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="48852-119">-Parola</span><span class="sxs-lookup"><span data-stu-id="48852-119">-Password</span></span>
<span data-ttu-id="48852-120">SSL sertifikasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48852-120">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48852-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48852-121">CommonParameters</span></span>
<span data-ttu-id="48852-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48852-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48852-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48852-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48852-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48852-124">INPUTS</span></span>

### <span data-ttu-id="48852-125">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48852-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="48852-126">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48852-126">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="48852-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48852-127">OUTPUTS</span></span>

### <span data-ttu-id="48852-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48852-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="48852-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48852-129">NOTES</span></span>

## <span data-ttu-id="48852-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48852-130">RELATED LINKS</span></span>

[<span data-ttu-id="48852-131">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="48852-131">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="48852-132">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="48852-132">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="48852-133">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="48852-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="48852-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="48852-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


