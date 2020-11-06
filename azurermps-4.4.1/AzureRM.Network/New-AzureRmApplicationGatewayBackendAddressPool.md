---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: f5be63987e055a7a7b6053820c22522bae021ad3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592178"
---
# <span data-ttu-id="6a648-101">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a648-101">New-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="6a648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a648-102">SYNOPSIS</span></span>
<span data-ttu-id="6a648-103">Uygulama ağ geçidi için arka uç adres havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a648-103">Creates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a648-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a648-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendAddressPool -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a648-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a648-105">DESCRIPTION</span></span>
<span data-ttu-id="6a648-106">**New-AzureRmApplicationGatewayBackendAddressPool** cmdlet 'ı bir Azure Application Gateway için bir arka uç adres havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a648-106">The **New-AzureRmApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="6a648-107">Arka uç adresi, IP adresi, tam nitelikli etki alanı adı (FQDN) veya IP yapılandırma KIMLIĞI olarak belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="6a648-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="6a648-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a648-108">EXAMPLES</span></span>

### <span data-ttu-id="6a648-109">Örnek 1: arka uç sunucusunun FQDN 'sini kullanarak arka uç adres havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a648-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="6a648-110">Bu komut, arka uç sunucuların FQDN 'lerini kullanarak Pool01 adlı bir arka uç adres havuzu oluşturur ve $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6a648-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="6a648-111">Örnek 2: arka uç sunucusunun IP adresini kullanarak arka uç adres havuzu oluşturma</span><span class="sxs-lookup"><span data-stu-id="6a648-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="6a648-112">Bu komut, arka uç sunucuların IP adreslerini kullanarak Pool02 adlı bir arka uç adres havuzu oluşturur ve $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6a648-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="6a648-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a648-113">PARAMETERS</span></span>

### <span data-ttu-id="6a648-114">-Backendfqdn 'leri</span><span class="sxs-lookup"><span data-stu-id="6a648-114">-BackendFqdns</span></span>
<span data-ttu-id="6a648-115">Bu cmdlet 'in arka uç sunucu havuzuyla ilişki kurduğu arka uç FQDN 'lerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a648-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="6a648-116">Backentüm adresler</span><span class="sxs-lookup"><span data-stu-id="6a648-116">-BackendIPAddresses</span></span>
<span data-ttu-id="6a648-117">Bu cmdlet 'in arka uç sunucu havuzuyla ilişki kurduğu arka uç IP adresleri listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a648-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="6a648-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a648-118">-Name</span></span>
<span data-ttu-id="6a648-119">Bu cmdlet 'in oluşturduğu arka uç sunucu havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a648-119">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6a648-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="6a648-120">-Confirm</span></span>
<span data-ttu-id="6a648-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6a648-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a648-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a648-122">-WhatIf</span></span>
<span data-ttu-id="6a648-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a648-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a648-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a648-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a648-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a648-125">-DefaultProfile</span></span>
<span data-ttu-id="6a648-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a648-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a648-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a648-127">CommonParameters</span></span>
<span data-ttu-id="6a648-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a648-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a648-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a648-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a648-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a648-130">INPUTS</span></span>

### <span data-ttu-id="6a648-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6a648-131">System.String</span></span>

## <span data-ttu-id="6a648-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a648-132">OUTPUTS</span></span>

### <span data-ttu-id="6a648-133">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a648-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="6a648-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a648-134">NOTES</span></span>

## <span data-ttu-id="6a648-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a648-135">RELATED LINKS</span></span>

[<span data-ttu-id="6a648-136">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a648-136">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6a648-137">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a648-137">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6a648-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a648-138">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="6a648-139">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="6a648-139">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


