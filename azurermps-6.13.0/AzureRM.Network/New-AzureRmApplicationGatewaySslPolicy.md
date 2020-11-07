---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySslPolicy.md
ms.openlocfilehash: 140bfd84d2758badc45a902e4ed14e027c5bca3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594876"
---
# <span data-ttu-id="47093-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="47093-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="47093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47093-102">SYNOPSIS</span></span>
<span data-ttu-id="47093-103">Uygulama ağ geçidi için SSL ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47093-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47093-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47093-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47093-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="47093-105">DESCRIPTION</span></span>
<span data-ttu-id="47093-106">**New-AzureRmApplicationGatewaySslPolicy** cmdlet 'i bir uygulama ağ GEÇIDI için SSL ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47093-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="47093-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47093-107">EXAMPLES</span></span>

### <span data-ttu-id="47093-108">2</span><span class="sxs-lookup"><span data-stu-id="47093-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="47093-109">Bu komut özel bir ilke oluşturur.</span><span class="sxs-lookup"><span data-stu-id="47093-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="47093-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47093-110">PARAMETERS</span></span>

### <span data-ttu-id="47093-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="47093-111">-CipherSuite</span></span>
<span data-ttu-id="47093-112">Uygulama ağ geçidine belirtilen sırada etkinleştirilecek SSL şifre paketleri</span><span class="sxs-lookup"><span data-stu-id="47093-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47093-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47093-113">-DefaultProfile</span></span>
<span data-ttu-id="47093-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47093-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47093-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="47093-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="47093-116">Hangi protokollerin devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="47093-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="47093-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="47093-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="47093-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="47093-118">TLSv1_0</span></span> 
- <span data-ttu-id="47093-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="47093-119">TLSv1_1</span></span> 
- <span data-ttu-id="47093-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="47093-120">TLSv1_2</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47093-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="47093-121">-MinProtocolVersion</span></span>
<span data-ttu-id="47093-122">Uygulama ağ geçidinde desteklenecek SSL protokolünün en az sürümü</span><span class="sxs-lookup"><span data-stu-id="47093-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47093-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="47093-123">-PolicyName</span></span>
<span data-ttu-id="47093-124">Önceden tanımlanmış SSL ilkesi adı</span><span class="sxs-lookup"><span data-stu-id="47093-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="47093-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="47093-125">-PolicyType</span></span>
<span data-ttu-id="47093-126">SSL Ilkesinin türü</span><span class="sxs-lookup"><span data-stu-id="47093-126">Type of Ssl Policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47093-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="47093-127">-Confirm</span></span>
<span data-ttu-id="47093-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47093-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47093-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47093-129">-WhatIf</span></span>
<span data-ttu-id="47093-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47093-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47093-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47093-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47093-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47093-132">CommonParameters</span></span>
<span data-ttu-id="47093-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47093-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47093-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47093-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47093-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47093-135">INPUTS</span></span>

### <span data-ttu-id="47093-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="47093-136">None</span></span>

## <span data-ttu-id="47093-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47093-137">OUTPUTS</span></span>

### <span data-ttu-id="47093-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="47093-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="47093-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47093-139">NOTES</span></span>
* <span data-ttu-id="47093-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="47093-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="47093-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47093-141">RELATED LINKS</span></span>

[<span data-ttu-id="47093-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="47093-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="47093-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="47093-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)

