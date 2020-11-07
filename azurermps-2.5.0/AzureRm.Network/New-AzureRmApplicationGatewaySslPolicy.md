---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 6c28665f35a7422a731aefd4ccf1c4ecabc549d4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938937"
---
# <span data-ttu-id="c20d1-101">New-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c20d1-101">New-AzureRmApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c20d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c20d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c20d1-103">Uygulama ağ geçidi için SSL ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c20d1-103">Creates an SSL policy for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c20d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c20d1-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySslPolicy
 [-DisabledSslProtocols <System.Collections.Generic.List`1[System.String]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <System.Collections.Generic.List`1[System.String]>]
 [-MinProtocolVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c20d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c20d1-105">DESCRIPTION</span></span>
<span data-ttu-id="c20d1-106">**New-AzureRmApplicationGatewaySslPolicy** cmdlet 'i bir uygulama ağ GEÇIDI için SSL ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c20d1-106">The **New-AzureRmApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="c20d1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c20d1-107">EXAMPLES</span></span>

### <span data-ttu-id="c20d1-108">2</span><span class="sxs-lookup"><span data-stu-id="c20d1-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzureRmApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="c20d1-109">Bu komut özel bir ilke oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c20d1-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="c20d1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c20d1-110">PARAMETERS</span></span>

### <span data-ttu-id="c20d1-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="c20d1-111">-CipherSuite</span></span>
<span data-ttu-id="c20d1-112">Uygulama ağ geçidine belirtilen sırada etkinleştirilecek SSL şifre paketleri</span><span class="sxs-lookup"><span data-stu-id="c20d1-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

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

### <span data-ttu-id="c20d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c20d1-113">-DefaultProfile</span></span>
<span data-ttu-id="c20d1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c20d1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c20d1-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="c20d1-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="c20d1-116">Hangi protokollerin devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c20d1-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="c20d1-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c20d1-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c20d1-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="c20d1-118">TLSv1_0</span></span> 
- <span data-ttu-id="c20d1-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="c20d1-119">TLSv1_1</span></span> 
- <span data-ttu-id="c20d1-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="c20d1-120">TLSv1_2</span></span>

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

### <span data-ttu-id="c20d1-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="c20d1-121">-MinProtocolVersion</span></span>
<span data-ttu-id="c20d1-122">Uygulama ağ geçidinde desteklenecek SSL protokolünün en az sürümü</span><span class="sxs-lookup"><span data-stu-id="c20d1-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20d1-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="c20d1-123">-PolicyName</span></span>
<span data-ttu-id="c20d1-124">Önceden tanımlanmış SSL ilkesi adı</span><span class="sxs-lookup"><span data-stu-id="c20d1-124">Name of Ssl predefined policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20d1-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="c20d1-125">-PolicyType</span></span>
<span data-ttu-id="c20d1-126">SSL Ilkesinin türü</span><span class="sxs-lookup"><span data-stu-id="c20d1-126">Type of Ssl Policy</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Predefined, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20d1-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="c20d1-127">-Confirm</span></span>
<span data-ttu-id="c20d1-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c20d1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20d1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c20d1-129">-WhatIf</span></span>
<span data-ttu-id="c20d1-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c20d1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c20d1-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c20d1-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c20d1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c20d1-132">CommonParameters</span></span>
<span data-ttu-id="c20d1-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c20d1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c20d1-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c20d1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c20d1-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c20d1-135">INPUTS</span></span>

### <span data-ttu-id="c20d1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c20d1-136">System.String</span></span>

## <span data-ttu-id="c20d1-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c20d1-137">OUTPUTS</span></span>

### <span data-ttu-id="c20d1-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c20d1-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="c20d1-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c20d1-139">NOTES</span></span>
* <span data-ttu-id="c20d1-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="c20d1-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c20d1-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c20d1-141">RELATED LINKS</span></span>

[<span data-ttu-id="c20d1-142">Get-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c20d1-142">Get-AzureRmApplicationGatewaySslPolicy</span></span>](./Get-AzureRmApplicationGatewaySslPolicy.md)

[<span data-ttu-id="c20d1-143">Set-AzureRmApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="c20d1-143">Set-AzureRmApplicationGatewaySslPolicy</span></span>](./Set-AzureRmApplicationGatewaySslPolicy.md)


