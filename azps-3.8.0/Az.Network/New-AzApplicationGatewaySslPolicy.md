---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98FA4E95-CAC5-4FBD-AA84-113BE9ED7FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslPolicy.md
ms.openlocfilehash: 758dddc18e029aadd1e3d548d613a07abd7fd565
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104776"
---
# <span data-ttu-id="d5d96-101">New-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d96-101">New-AzApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="d5d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d96-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d96-103">Uygulama ağ geçidi için SSL ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5d96-103">Creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="d5d96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5d96-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslPolicy [-DisabledSslProtocols <String[]>] [-PolicyType <String>]
 [-PolicyName <String>] [-CipherSuite <String[]>] [-MinProtocolVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5d96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5d96-105">DESCRIPTION</span></span>
<span data-ttu-id="d5d96-106">**Yeni-AzApplicationGatewaySslPolicy** cmdlet 'i bir uygulama ağ GEÇIDI için SSL ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5d96-106">The **New-AzApplicationGatewaySslPolicy** cmdlet creates an SSL policy for an application gateway.</span></span>

## <span data-ttu-id="d5d96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5d96-107">EXAMPLES</span></span>

### <span data-ttu-id="d5d96-108">2</span><span class="sxs-lookup"><span data-stu-id="d5d96-108">1:</span></span>
```
PS C:\>$sslPolicy = New-AzApplicationGatewaySslPolicy -PolicyType Custom -MinProtocolVersion TLSv1_1 -CipherSuite "TLS_ECDHE_ECDSA_WITH_AES_128_GCM_SHA256", "TLS_ECDHE_ECDSA_WITH_AES_256_GCM_SHA384", "TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA", "TLS_RSA_WITH_AES_128_GCM_SHA256"
```

<span data-ttu-id="d5d96-109">Bu komut özel bir ilke oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d5d96-109">This command creates a custom policy.</span></span>

## <span data-ttu-id="d5d96-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5d96-110">PARAMETERS</span></span>

### <span data-ttu-id="d5d96-111">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="d5d96-111">-CipherSuite</span></span>
<span data-ttu-id="d5d96-112">Uygulama ağ geçidine belirtilen sırada etkinleştirilecek SSL şifre paketleri</span><span class="sxs-lookup"><span data-stu-id="d5d96-112">Ssl cipher suites to be enabled in the specified order to application gateway</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d96-113">-DefaultProfile</span></span>
<span data-ttu-id="d5d96-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5d96-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d96-115">-DisabledSslProtocols</span><span class="sxs-lookup"><span data-stu-id="d5d96-115">-DisabledSslProtocols</span></span>
<span data-ttu-id="d5d96-116">Hangi protokollerin devre dışı olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5d96-116">Specifies which protocols are disabled.</span></span>
<span data-ttu-id="d5d96-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d5d96-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d5d96-118">TLSv1_0</span><span class="sxs-lookup"><span data-stu-id="d5d96-118">TLSv1_0</span></span> 
- <span data-ttu-id="d5d96-119">TLSv1_1</span><span class="sxs-lookup"><span data-stu-id="d5d96-119">TLSv1_1</span></span> 
- <span data-ttu-id="d5d96-120">TLSv1_2</span><span class="sxs-lookup"><span data-stu-id="d5d96-120">TLSv1_2</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: TLSv1_0, TLSv1_1, TLSv1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5d96-121">-MinProtocolVersion</span><span class="sxs-lookup"><span data-stu-id="d5d96-121">-MinProtocolVersion</span></span>
<span data-ttu-id="d5d96-122">Uygulama ağ geçidinde desteklenecek SSL protokolünün en az sürümü</span><span class="sxs-lookup"><span data-stu-id="d5d96-122">Minimum version of Ssl protocol to be supported on application gateway</span></span>

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

### <span data-ttu-id="d5d96-123">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="d5d96-123">-PolicyName</span></span>
<span data-ttu-id="d5d96-124">Önceden tanımlanmış SSL ilkesi adı</span><span class="sxs-lookup"><span data-stu-id="d5d96-124">Name of Ssl predefined policy</span></span>

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

### <span data-ttu-id="d5d96-125">-PolicyType</span><span class="sxs-lookup"><span data-stu-id="d5d96-125">-PolicyType</span></span>
<span data-ttu-id="d5d96-126">SSL Ilkesinin türü</span><span class="sxs-lookup"><span data-stu-id="d5d96-126">Type of Ssl Policy</span></span>

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

### <span data-ttu-id="d5d96-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5d96-127">-Confirm</span></span>
<span data-ttu-id="d5d96-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5d96-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d96-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5d96-129">-WhatIf</span></span>
<span data-ttu-id="d5d96-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5d96-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5d96-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5d96-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d96-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d96-132">CommonParameters</span></span>
<span data-ttu-id="d5d96-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5d96-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d96-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5d96-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d96-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5d96-135">INPUTS</span></span>

### <span data-ttu-id="d5d96-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d5d96-136">None</span></span>

## <span data-ttu-id="d5d96-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5d96-137">OUTPUTS</span></span>

### <span data-ttu-id="d5d96-138">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d96-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="d5d96-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5d96-139">NOTES</span></span>
* <span data-ttu-id="d5d96-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="d5d96-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d5d96-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5d96-141">RELATED LINKS</span></span>

[<span data-ttu-id="d5d96-142">Get-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d96-142">Get-AzApplicationGatewaySslPolicy</span></span>](./Get-AzApplicationGatewaySslPolicy.md)

[<span data-ttu-id="d5d96-143">Set-AzApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="d5d96-143">Set-AzApplicationGatewaySslPolicy</span></span>](./Set-AzApplicationGatewaySslPolicy.md)


