---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e44136d5fa9b0a6b0b979005c13faf6041d98f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593219"
---
# <span data-ttu-id="cd8a5-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="cd8a5-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="cd8a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd8a5-102">SYNOPSIS</span></span>
<span data-ttu-id="cd8a5-103">Uygulama ağ geçidine güvenilir kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-103">Adds a trusted root certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd8a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd8a5-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd8a5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd8a5-105">DESCRIPTION</span></span>
<span data-ttu-id="cd8a5-106">**Add-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet 'ı bir Azure Application Gateway 'e güvenilir bir kök sertifikası ekler.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-106">The **Add-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="cd8a5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd8a5-107">EXAMPLES</span></span>

### <span data-ttu-id="cd8a5-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cd8a5-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzureRmApplicationGatewayBackendHttpSetting -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="cd8a5-109">İlk komut uygulama ağ geçidini alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="cd8a5-110">İkinci komut, kök sertifikanın giriş olarak bulunduğu uygulama ağ geçidi</span><span class="sxs-lookup"><span data-stu-id="cd8a5-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="cd8a5-111">Üçüncü komut, arka uç sunucu sertifikasını doğrulamak için güvenilen kök sertifikası kullanarak yeni bir arka uç http ayarı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="cd8a5-112">Fouth komutu, uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="cd8a5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd8a5-113">PARAMETERS</span></span>

### <span data-ttu-id="cd8a5-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd8a5-114">-ApplicationGateway</span></span>
<span data-ttu-id="cd8a5-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd8a5-115">The applicationGateway</span></span>

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

### <span data-ttu-id="cd8a5-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="cd8a5-116">-CertificateFile</span></span>
<span data-ttu-id="cd8a5-117">Sertifika CER dosyasının yolu</span><span class="sxs-lookup"><span data-stu-id="cd8a5-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="cd8a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd8a5-118">-DefaultProfile</span></span>
<span data-ttu-id="cd8a5-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd8a5-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="cd8a5-120">-Name</span></span>
<span data-ttu-id="cd8a5-121">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="cd8a5-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="cd8a5-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="cd8a5-122">-Confirm</span></span>
<span data-ttu-id="cd8a5-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8a5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd8a5-124">-WhatIf</span></span>
<span data-ttu-id="cd8a5-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd8a5-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd8a5-127">CommonParameters</span></span>
<span data-ttu-id="cd8a5-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd8a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd8a5-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd8a5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd8a5-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd8a5-130">INPUTS</span></span>

### <span data-ttu-id="cd8a5-131">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd8a5-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cd8a5-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd8a5-132">OUTPUTS</span></span>

### <span data-ttu-id="cd8a5-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cd8a5-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cd8a5-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd8a5-134">NOTES</span></span>

## <span data-ttu-id="cd8a5-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd8a5-135">RELATED LINKS</span></span>
