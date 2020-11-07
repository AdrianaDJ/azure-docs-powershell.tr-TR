---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: fa2116d9247237e6f031bad31d9cea1716ab12f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761402"
---
# <span data-ttu-id="59d63-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="59d63-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="59d63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59d63-102">SYNOPSIS</span></span>
<span data-ttu-id="59d63-103">Özel bir etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59d63-103">Removes a custom domain.</span></span>

## <span data-ttu-id="59d63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59d63-104">SYNTAX</span></span>

### <span data-ttu-id="59d63-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59d63-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59d63-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59d63-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59d63-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="59d63-107">DESCRIPTION</span></span>
<span data-ttu-id="59d63-108">**Remove-AzCdnCustomDomain** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktasından özel etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59d63-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="59d63-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59d63-109">EXAMPLES</span></span>

## <span data-ttu-id="59d63-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59d63-110">PARAMETERS</span></span>

### <span data-ttu-id="59d63-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="59d63-111">-CdnCustomDomain</span></span>
<span data-ttu-id="59d63-112">Bu cmdlet 'in kaldırdığı özel etki alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59d63-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="59d63-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="59d63-113">-CustomDomainName</span></span>
<span data-ttu-id="59d63-114">Bu cmdlet 'in kaldırdığı özel etki alanının kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59d63-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="59d63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d63-115">-DefaultProfile</span></span>
<span data-ttu-id="59d63-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="59d63-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59d63-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="59d63-117">-EndpointName</span></span>
<span data-ttu-id="59d63-118">Bu cmdlet 'in özel bir etki alanını kaldırdığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59d63-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="59d63-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="59d63-119">-PassThru</span></span>
<span data-ttu-id="59d63-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="59d63-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59d63-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="59d63-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59d63-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="59d63-122">-ProfileName</span></span>
<span data-ttu-id="59d63-123">Bu cmdlet 'in özel etki alanını kaldırdığı profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59d63-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="59d63-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d63-124">-ResourceGroupName</span></span>
<span data-ttu-id="59d63-125">Bu cmdlet 'in özel bir etki alanını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59d63-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="59d63-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="59d63-126">-Confirm</span></span>
<span data-ttu-id="59d63-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59d63-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d63-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d63-128">-WhatIf</span></span>
<span data-ttu-id="59d63-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59d63-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59d63-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59d63-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d63-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d63-131">CommonParameters</span></span>
<span data-ttu-id="59d63-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59d63-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d63-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d63-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d63-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59d63-134">INPUTS</span></span>

### <span data-ttu-id="59d63-135">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="59d63-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="59d63-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59d63-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="59d63-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59d63-137">OUTPUTS</span></span>

### <span data-ttu-id="59d63-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59d63-138">System.Boolean</span></span>

## <span data-ttu-id="59d63-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59d63-139">NOTES</span></span>

## <span data-ttu-id="59d63-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59d63-140">RELATED LINKS</span></span>

[<span data-ttu-id="59d63-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="59d63-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="59d63-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="59d63-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="59d63-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="59d63-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


