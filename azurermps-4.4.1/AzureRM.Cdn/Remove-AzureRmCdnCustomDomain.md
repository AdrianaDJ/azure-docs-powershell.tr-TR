---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 2aa6b3932424f7a8375cca2584a7fc7916124c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592651"
---
# <span data-ttu-id="4c1e9-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c1e9-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="4c1e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4c1e9-103">Özel bir etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c1e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c1e9-104">SYNTAX</span></span>

### <span data-ttu-id="4c1e9-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c1e9-105">Parameter Set for fields parameters (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c1e9-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="4c1e9-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c1e9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c1e9-107">DESCRIPTION</span></span>
<span data-ttu-id="4c1e9-108">**Remove-AzureRmCdnCustomDomain** cmdlet 'ı Azure Içerik teslim ağı (CDN) uç noktasından özel etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="4c1e9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c1e9-109">EXAMPLES</span></span>

## <span data-ttu-id="4c1e9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c1e9-110">PARAMETERS</span></span>

### <span data-ttu-id="4c1e9-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c1e9-111">-CdnCustomDomain</span></span>
<span data-ttu-id="4c1e9-112">Bu cmdlet 'in kaldırdığı özel etki alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c1e9-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="4c1e9-113">-CustomDomainName</span></span>
<span data-ttu-id="4c1e9-114">Bu cmdlet 'in kaldırdığı özel etki alanının kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1e9-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4c1e9-115">-EndpointName</span></span>
<span data-ttu-id="4c1e9-116">Bu cmdlet 'in özel bir etki alanını kaldırdığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-116">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1e9-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4c1e9-117">-PassThru</span></span>
<span data-ttu-id="4c1e9-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4c1e9-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c1e9-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4c1e9-120">-ProfileName</span></span>
<span data-ttu-id="4c1e9-121">Bu cmdlet 'in özel etki alanını kaldırdığı profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-121">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c1e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="4c1e9-123">Bu cmdlet 'in özel bir etki alanını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-123">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1e9-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c1e9-124">-Confirm</span></span>
<span data-ttu-id="4c1e9-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c1e9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c1e9-126">-WhatIf</span></span>
<span data-ttu-id="4c1e9-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c1e9-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c1e9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c1e9-129">-DefaultProfile</span></span>
<span data-ttu-id="4c1e9-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c1e9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c1e9-131">CommonParameters</span></span>
<span data-ttu-id="4c1e9-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c1e9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c1e9-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c1e9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c1e9-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c1e9-134">INPUTS</span></span>

### <span data-ttu-id="4c1e9-135">Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="4c1e9-135">PSCustomDomain</span></span>
<span data-ttu-id="4c1e9-136">' CdnCustomDomain ' parametresi ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="4c1e9-136">Parameter 'CdnCustomDomain' accepts value of type 'PSCustomDomain' from the pipeline</span></span>

## <span data-ttu-id="4c1e9-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c1e9-137">OUTPUTS</span></span>

### <span data-ttu-id="4c1e9-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c1e9-138">System.Boolean</span></span>

## <span data-ttu-id="4c1e9-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c1e9-139">NOTES</span></span>

## <span data-ttu-id="4c1e9-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c1e9-140">RELATED LINKS</span></span>

[<span data-ttu-id="4c1e9-141">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c1e9-141">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="4c1e9-142">Yeni-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c1e9-142">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="4c1e9-143">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="4c1e9-143">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)

