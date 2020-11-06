---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnCustomDomain.md
ms.openlocfilehash: fa0e3682d62f01d7d305d190c6765aab709bed15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591387"
---
# <span data-ttu-id="d9622-101">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d9622-101">Remove-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="d9622-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9622-102">SYNOPSIS</span></span>
<span data-ttu-id="d9622-103">Özel bir etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9622-103">Removes a custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9622-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9622-104">SYNTAX</span></span>

### <span data-ttu-id="d9622-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d9622-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9622-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9622-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9622-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9622-107">DESCRIPTION</span></span>
<span data-ttu-id="d9622-108">**Remove-AzureRmCdnCustomDomain** cmdlet 'ı Azure Içerik teslim ağı (CDN) uç noktasından özel etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d9622-108">The **Remove-AzureRmCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="d9622-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9622-109">EXAMPLES</span></span>

## <span data-ttu-id="d9622-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9622-110">PARAMETERS</span></span>

### <span data-ttu-id="d9622-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d9622-111">-CdnCustomDomain</span></span>
<span data-ttu-id="d9622-112">Bu cmdlet 'in kaldırdığı özel etki alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9622-112">Specifies the custom domain that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9622-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="d9622-113">-CustomDomainName</span></span>
<span data-ttu-id="d9622-114">Bu cmdlet 'in kaldırdığı özel etki alanının kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9622-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9622-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9622-115">-DefaultProfile</span></span>
<span data-ttu-id="d9622-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d9622-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9622-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d9622-117">-EndpointName</span></span>
<span data-ttu-id="d9622-118">Bu cmdlet 'in özel bir etki alanını kaldırdığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9622-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9622-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d9622-119">-PassThru</span></span>
<span data-ttu-id="d9622-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="d9622-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d9622-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d9622-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9622-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d9622-122">-ProfileName</span></span>
<span data-ttu-id="d9622-123">Bu cmdlet 'in özel etki alanını kaldırdığı profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9622-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9622-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9622-124">-ResourceGroupName</span></span>
<span data-ttu-id="d9622-125">Bu cmdlet 'in özel bir etki alanını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d9622-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9622-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9622-126">-Confirm</span></span>
<span data-ttu-id="d9622-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9622-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9622-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9622-128">-WhatIf</span></span>
<span data-ttu-id="d9622-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9622-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9622-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9622-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9622-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9622-131">CommonParameters</span></span>
<span data-ttu-id="d9622-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9622-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9622-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9622-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9622-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9622-134">INPUTS</span></span>

### <span data-ttu-id="d9622-135">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="d9622-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="d9622-136">Parametreler: CdnCustomDomain (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d9622-136">Parameters: CdnCustomDomain (ByValue)</span></span>

### <span data-ttu-id="d9622-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d9622-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d9622-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9622-138">OUTPUTS</span></span>

### <span data-ttu-id="d9622-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9622-139">System.Boolean</span></span>

## <span data-ttu-id="d9622-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9622-140">NOTES</span></span>

## <span data-ttu-id="d9622-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9622-141">RELATED LINKS</span></span>

[<span data-ttu-id="d9622-142">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d9622-142">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="d9622-143">Yeni-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d9622-143">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="d9622-144">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d9622-144">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


