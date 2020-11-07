---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 961580d6354c6916ad811d6f8bccd4119d8b07a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935444"
---
# <span data-ttu-id="a5310-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a5310-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a5310-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5310-102">SYNOPSIS</span></span>
<span data-ttu-id="a5310-103">Uygulama ağ geçidi için arka uç adres havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5310-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="a5310-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5310-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5310-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5310-105">DESCRIPTION</span></span>
<span data-ttu-id="a5310-106">**Yeni-AzApplicationGatewayBackendAddressPool** cmdlet 'ı bir Azure uygulama ağ geçidi için arka uç adres havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5310-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="a5310-107">Arka uç adresi, IP adresi, tam nitelikli etki alanı adı (FQDN) veya IP yapılandırma KIMLIĞI olarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="a5310-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="a5310-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5310-108">EXAMPLES</span></span>

### <span data-ttu-id="a5310-109">Örnek 1: arka uç sunucusunun FQDN 'sini kullanarak arka uç adres havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a5310-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="a5310-110">Bu komut, arka uç sunucuların FQDN 'lerini kullanarak Pool01 adlı bir arka uç adres havuzu oluşturur ve $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a5310-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="a5310-111">Örnek 2: arka uç sunucusunun IP adresini kullanarak arka uç adres havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="a5310-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="a5310-112">Bu komut, arka uç sunucuların IP adreslerini kullanarak Pool02 adlı bir arka uç adres havuzu oluşturur ve $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a5310-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="a5310-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5310-113">PARAMETERS</span></span>

### <span data-ttu-id="a5310-114">-Backendfqdn 'leri</span><span class="sxs-lookup"><span data-stu-id="a5310-114">-BackendFqdns</span></span>
<span data-ttu-id="a5310-115">Bu cmdlet 'in arka uç sunucu havuzuyla ilişki kurduğu arka uç FQDN 'lerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5310-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="a5310-116">Backentüm adresler</span><span class="sxs-lookup"><span data-stu-id="a5310-116">-BackendIPAddresses</span></span>
<span data-ttu-id="a5310-117">Bu cmdlet 'in arka uç sunucu havuzuyla ilişki kurduğu arka uç IP adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5310-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="a5310-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5310-118">-DefaultProfile</span></span>
<span data-ttu-id="a5310-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5310-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5310-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5310-120">-Name</span></span>
<span data-ttu-id="a5310-121">Bu cmdlet 'in oluşturduğu arka uç sunucu havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5310-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a5310-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5310-122">-Confirm</span></span>
<span data-ttu-id="a5310-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5310-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5310-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5310-124">-WhatIf</span></span>
<span data-ttu-id="a5310-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5310-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5310-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5310-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5310-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5310-127">CommonParameters</span></span>
<span data-ttu-id="a5310-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5310-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5310-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5310-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5310-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5310-130">INPUTS</span></span>

### <span data-ttu-id="a5310-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a5310-131">System.String</span></span>

## <span data-ttu-id="a5310-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5310-132">OUTPUTS</span></span>

### <span data-ttu-id="a5310-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a5310-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a5310-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5310-134">NOTES</span></span>

## <span data-ttu-id="a5310-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5310-135">RELATED LINKS</span></span>

[<span data-ttu-id="a5310-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a5310-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a5310-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a5310-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a5310-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a5310-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a5310-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a5310-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


