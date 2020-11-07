---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 65c178cc8cf293cf6c20e6262733031e377f61fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938958"
---
# <span data-ttu-id="cca22-101">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cca22-101">Add-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="cca22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca22-102">SYNOPSIS</span></span>
<span data-ttu-id="cca22-103">Uygulama ağ geçidine SSL sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cca22-103">Adds an SSL certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cca22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cca22-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cca22-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cca22-105">DESCRIPTION</span></span>
<span data-ttu-id="cca22-106">**Add-AzureRmApplicationGatewaySslCertificate** cmdlet 'i bir uygulama ağ geçidine SSL sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cca22-106">The **Add-AzureRmApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="cca22-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cca22-107">EXAMPLES</span></span>

### <span data-ttu-id="cca22-108">Örnek 1: uygulama ağ geçidine SSL sertifikası ekleyin.</span><span class="sxs-lookup"><span data-stu-id="cca22-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="cca22-109">Bu komut ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve ardından Cert01 adlı bir SSL sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cca22-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="cca22-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cca22-110">PARAMETERS</span></span>

### <span data-ttu-id="cca22-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cca22-111">-ApplicationGateway</span></span>
<span data-ttu-id="cca22-112">Bu cmdlet 'in SSL sertifikası eklediği uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cca22-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="cca22-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cca22-113">-CertificateFile</span></span>
<span data-ttu-id="cca22-114">Bu cmdlet 'in eklediği SSL sertifikasının. pfx dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cca22-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cca22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca22-115">-DefaultProfile</span></span>
<span data-ttu-id="cca22-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cca22-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cca22-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="cca22-117">-Name</span></span>
<span data-ttu-id="cca22-118">Bu cmdlet 'in eklediği SSL sertifikasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cca22-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cca22-119">-Parola</span><span class="sxs-lookup"><span data-stu-id="cca22-119">-Password</span></span>
<span data-ttu-id="cca22-120">Bu cmdlet 'in eklediği SSL sertifikasının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cca22-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="cca22-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca22-121">CommonParameters</span></span>
<span data-ttu-id="cca22-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cca22-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca22-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cca22-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca22-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cca22-124">INPUTS</span></span>

### <span data-ttu-id="cca22-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cca22-125">System.String</span></span>

## <span data-ttu-id="cca22-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cca22-126">OUTPUTS</span></span>

### <span data-ttu-id="cca22-127">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cca22-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cca22-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cca22-128">NOTES</span></span>

## <span data-ttu-id="cca22-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cca22-129">RELATED LINKS</span></span>

[<span data-ttu-id="cca22-130">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cca22-130">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cca22-131">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cca22-131">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cca22-132">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cca22-132">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="cca22-133">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cca22-133">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


