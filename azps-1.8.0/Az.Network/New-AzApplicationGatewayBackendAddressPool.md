---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1165d7abccdbf21dc94e4f39b8b2dad953fdba07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760429"
---
# <span data-ttu-id="12b45-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12b45-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="12b45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12b45-102">SYNOPSIS</span></span>
<span data-ttu-id="12b45-103">Uygulama ağ geçidi için arka uç adres havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12b45-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="12b45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="12b45-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12b45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="12b45-105">DESCRIPTION</span></span>
<span data-ttu-id="12b45-106">**Yeni-AzApplicationGatewayBackendAddressPool** cmdlet 'ı bir Azure uygulama ağ geçidi için arka uç adres havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12b45-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="12b45-107">Arka uç adresi, IP adresi, tam nitelikli etki alanı adı (FQDN) veya IP yapılandırma KIMLIĞI olarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="12b45-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="12b45-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="12b45-108">EXAMPLES</span></span>

### <span data-ttu-id="12b45-109">Örnek 1: arka uç sunucusunun FQDN 'sini kullanarak arka uç adres havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="12b45-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="12b45-110">Bu komut, arka uç sunucuların FQDN 'lerini kullanarak Pool01 adlı bir arka uç adres havuzu oluşturur ve $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="12b45-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="12b45-111">Örnek 2: arka uç sunucusunun IP adresini kullanarak arka uç adres havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="12b45-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="12b45-112">Bu komut, arka uç sunucuların IP adreslerini kullanarak Pool02 adlı bir arka uç adres havuzu oluşturur ve $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="12b45-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="12b45-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="12b45-113">PARAMETERS</span></span>

### <span data-ttu-id="12b45-114">-Backendfqdn 'leri</span><span class="sxs-lookup"><span data-stu-id="12b45-114">-BackendFqdns</span></span>
<span data-ttu-id="12b45-115">Bu cmdlet 'in arka uç sunucu havuzuyla ilişki kurduğu arka uç FQDN 'lerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="12b45-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="12b45-116">Backentüm adresler</span><span class="sxs-lookup"><span data-stu-id="12b45-116">-BackendIPAddresses</span></span>
<span data-ttu-id="12b45-117">Bu cmdlet 'in arka uç sunucu havuzuyla ilişki kurduğu arka uç IP adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="12b45-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="12b45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b45-118">-DefaultProfile</span></span>
<span data-ttu-id="12b45-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="12b45-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12b45-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="12b45-120">-Name</span></span>
<span data-ttu-id="12b45-121">Bu cmdlet 'in oluşturduğu arka uç sunucu havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="12b45-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="12b45-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="12b45-122">-Confirm</span></span>
<span data-ttu-id="12b45-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="12b45-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b45-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b45-124">-WhatIf</span></span>
<span data-ttu-id="12b45-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12b45-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12b45-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="12b45-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b45-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b45-127">CommonParameters</span></span>
<span data-ttu-id="12b45-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="12b45-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b45-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b45-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b45-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="12b45-130">INPUTS</span></span>

### <span data-ttu-id="12b45-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="12b45-131">None</span></span>

## <span data-ttu-id="12b45-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="12b45-132">OUTPUTS</span></span>

### <span data-ttu-id="12b45-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12b45-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="12b45-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="12b45-134">NOTES</span></span>

## <span data-ttu-id="12b45-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="12b45-135">RELATED LINKS</span></span>

[<span data-ttu-id="12b45-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12b45-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="12b45-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12b45-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="12b45-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12b45-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="12b45-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="12b45-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

