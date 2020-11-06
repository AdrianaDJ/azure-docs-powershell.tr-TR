---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 0505f7452c20c0bdb3ccf3a9bc203380479083ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572729"
---
# <span data-ttu-id="9e6a8-101">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="9e6a8-101">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="9e6a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e6a8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6a8-103">Uygulama ağ geçidi 'nin güvenilen kök sertifikasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e6a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e6a8-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e6a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e6a8-105">DESCRIPTION</span></span>
<span data-ttu-id="9e6a8-106">**Set-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet 'ı, uygulamanın varolan güvenilen kök sertifikasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-106">The **Set-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="9e6a8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e6a8-107">EXAMPLES</span></span>

### <span data-ttu-id="9e6a8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9e6a8-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="9e6a8-109">Yukarıdaki örnek senaryolar, kök sertifika alındığında varolan bir güvenilen kök sertifikanın nasıl güncelleştirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="9e6a8-110">İlk komut bir uygulama ağ geçidi alır ve $gw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="9e6a8-111">İkinci komut, varolan güvenilen kök sertifikayı yeni bir kök sertifikayla değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="9e6a8-112">Üçüncü komut, Azure 'daki uygulama ağ geçidini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="9e6a8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e6a8-113">PARAMETERS</span></span>

### <span data-ttu-id="9e6a8-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e6a8-114">-ApplicationGateway</span></span>
<span data-ttu-id="9e6a8-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e6a8-115">The applicationGateway</span></span>

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

### <span data-ttu-id="9e6a8-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9e6a8-116">-CertificateFile</span></span>
<span data-ttu-id="9e6a8-117">Sertifika CER dosyasının yolu</span><span class="sxs-lookup"><span data-stu-id="9e6a8-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="9e6a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6a8-118">-DefaultProfile</span></span>
<span data-ttu-id="9e6a8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e6a8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e6a8-120">-Name</span></span>
<span data-ttu-id="9e6a8-121">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="9e6a8-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="9e6a8-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="9e6a8-122">-Confirm</span></span>
<span data-ttu-id="9e6a8-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e6a8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e6a8-124">-WhatIf</span></span>
<span data-ttu-id="9e6a8-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e6a8-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e6a8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6a8-127">CommonParameters</span></span>
<span data-ttu-id="9e6a8-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e6a8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6a8-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6a8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6a8-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e6a8-130">INPUTS</span></span>

### <span data-ttu-id="9e6a8-131">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e6a8-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e6a8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e6a8-132">OUTPUTS</span></span>

### <span data-ttu-id="9e6a8-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e6a8-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9e6a8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e6a8-134">NOTES</span></span>

## <span data-ttu-id="9e6a8-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e6a8-135">RELATED LINKS</span></span>
