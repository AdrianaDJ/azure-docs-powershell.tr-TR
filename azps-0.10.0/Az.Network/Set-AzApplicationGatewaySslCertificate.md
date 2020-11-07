---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b68f0bf3b0112587256fddc3dbb6c31605f811b7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936555"
---
# <span data-ttu-id="75af2-101">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="75af2-101">Set-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="75af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75af2-102">SYNOPSIS</span></span>
<span data-ttu-id="75af2-103">SSL sertifikasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="75af2-103">Sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="75af2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75af2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="75af2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75af2-105">DESCRIPTION</span></span>
<span data-ttu-id="75af2-106">**Set-AzApplicationGatewaySslCertificate** cmdlet 'ı, SSL sertifikasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="75af2-106">The **Set-AzApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="75af2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75af2-107">EXAMPLES</span></span>

### <span data-ttu-id="75af2-108">Örnek 1: SSL sertifikasının hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="75af2-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="75af2-109">Bu komut, ApplicationGateway01 adındaki uygulama ağ geçidinden SSL sertifikasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="75af2-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="75af2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75af2-110">PARAMETERS</span></span>

### <span data-ttu-id="75af2-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75af2-111">-ApplicationGateway</span></span>
<span data-ttu-id="75af2-112">Güvenli Yuva Katmanı (SSL) sertifikasının ilişkili olduğu uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75af2-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="75af2-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="75af2-113">-CertificateFile</span></span>
<span data-ttu-id="75af2-114">SSL sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="75af2-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="75af2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75af2-115">-DefaultProfile</span></span>
<span data-ttu-id="75af2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75af2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75af2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="75af2-117">-Name</span></span>
<span data-ttu-id="75af2-118">SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75af2-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="75af2-119">-Parola</span><span class="sxs-lookup"><span data-stu-id="75af2-119">-Password</span></span>
<span data-ttu-id="75af2-120">SSL sertifikasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75af2-120">Specifies the password of the SSL certificate.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75af2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75af2-121">CommonParameters</span></span>
<span data-ttu-id="75af2-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75af2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75af2-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75af2-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75af2-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75af2-124">INPUTS</span></span>

### <span data-ttu-id="75af2-125">System. String</span><span class="sxs-lookup"><span data-stu-id="75af2-125">System.String</span></span>

## <span data-ttu-id="75af2-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75af2-126">OUTPUTS</span></span>

### <span data-ttu-id="75af2-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="75af2-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="75af2-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75af2-128">NOTES</span></span>

## <span data-ttu-id="75af2-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75af2-129">RELATED LINKS</span></span>

[<span data-ttu-id="75af2-130">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="75af2-130">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="75af2-131">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="75af2-131">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="75af2-132">Yeni-Azapplicationgatewaysslsertifikası</span><span class="sxs-lookup"><span data-stu-id="75af2-132">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="75af2-133">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="75af2-133">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)


