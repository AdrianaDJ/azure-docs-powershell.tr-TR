---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 1af7ef3b60fa296a5fb8190675393a0726d0502b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588152"
---
# <span data-ttu-id="ddb8a-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb8a-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ddb8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddb8a-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb8a-103">SSL sertifikasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ddb8a-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddb8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddb8a-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ddb8a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddb8a-105">DESCRIPTION</span></span>
<span data-ttu-id="ddb8a-106">**Set-AzureRmApplicationGatewaySslCertificate** cmdlet 'ı, SSL sertifikasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ddb8a-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="ddb8a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddb8a-107">EXAMPLES</span></span>

### <span data-ttu-id="ddb8a-108">Örnek 1: SSL sertifikasının hedef durumunu ayarlama</span><span class="sxs-lookup"><span data-stu-id="ddb8a-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\> $appGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="ddb8a-109">Bu komut, ApplicationGateway01 adındaki uygulama ağ geçidinden SSL sertifikasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ddb8a-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="ddb8a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddb8a-110">PARAMETERS</span></span>

### <span data-ttu-id="ddb8a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddb8a-111">-ApplicationGateway</span></span>
<span data-ttu-id="ddb8a-112">Güvenli Yuva Katmanı (SSL) sertifikasının ilişkili olduğu uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddb8a-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="ddb8a-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="ddb8a-113">-CertificateFile</span></span>
<span data-ttu-id="ddb8a-114">SSL sertifikasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddb8a-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="ddb8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb8a-115">-DefaultProfile</span></span>
<span data-ttu-id="ddb8a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddb8a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddb8a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="ddb8a-117">-Name</span></span>
<span data-ttu-id="ddb8a-118">SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddb8a-118">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="ddb8a-119">-Parola</span><span class="sxs-lookup"><span data-stu-id="ddb8a-119">-Password</span></span>
<span data-ttu-id="ddb8a-120">SSL sertifikasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddb8a-120">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="ddb8a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb8a-121">CommonParameters</span></span>
<span data-ttu-id="ddb8a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddb8a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb8a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb8a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb8a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddb8a-124">INPUTS</span></span>

### <span data-ttu-id="ddb8a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb8a-125">System.String</span></span>

## <span data-ttu-id="ddb8a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddb8a-126">OUTPUTS</span></span>

### <span data-ttu-id="ddb8a-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ddb8a-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ddb8a-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddb8a-128">NOTES</span></span>

## <span data-ttu-id="ddb8a-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddb8a-129">RELATED LINKS</span></span>

[<span data-ttu-id="ddb8a-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb8a-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ddb8a-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb8a-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ddb8a-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb8a-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ddb8a-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb8a-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


