---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 5727E2CA-0A0B-4050-9F4A-7E06758D9B53
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnCustomDomain.md
ms.openlocfilehash: 0645b3f5286526ba72db35fd8b9e048c895f4108
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095810"
---
# <span data-ttu-id="aa636-101">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="aa636-101">Remove-AzCdnCustomDomain</span></span>

## <span data-ttu-id="aa636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa636-102">SYNOPSIS</span></span>
<span data-ttu-id="aa636-103">Özel bir etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="aa636-103">Removes a custom domain.</span></span>

## <span data-ttu-id="aa636-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa636-104">SYNTAX</span></span>

### <span data-ttu-id="aa636-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aa636-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa636-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa636-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnCustomDomain -CdnCustomDomain <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa636-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa636-107">DESCRIPTION</span></span>
<span data-ttu-id="aa636-108">**Remove-AzCdnCustomDomain** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktasından özel etki alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="aa636-108">The **Remove-AzCdnCustomDomain** cmdlet removes the custom domain from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="aa636-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa636-109">EXAMPLES</span></span>

## <span data-ttu-id="aa636-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa636-110">PARAMETERS</span></span>

### <span data-ttu-id="aa636-111">-CdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="aa636-111">-CdnCustomDomain</span></span>
<span data-ttu-id="aa636-112">Bu cmdlet 'in kaldırdığı özel etki alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa636-112">Specifies the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aa636-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="aa636-113">-CustomDomainName</span></span>
<span data-ttu-id="aa636-114">Bu cmdlet 'in kaldırdığı özel etki alanının kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa636-114">Specifies the resource name of the custom domain that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aa636-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa636-115">-DefaultProfile</span></span>
<span data-ttu-id="aa636-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="aa636-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa636-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="aa636-117">-EndpointName</span></span>
<span data-ttu-id="aa636-118">Bu cmdlet 'in özel bir etki alanını kaldırdığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa636-118">Specifies the name of the endpoint from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="aa636-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="aa636-119">-PassThru</span></span>
<span data-ttu-id="aa636-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="aa636-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aa636-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="aa636-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa636-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="aa636-122">-ProfileName</span></span>
<span data-ttu-id="aa636-123">Bu cmdlet 'in özel etki alanını kaldırdığı profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa636-123">Specifies the name of the profile from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="aa636-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa636-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa636-125">Bu cmdlet 'in özel bir etki alanını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa636-125">Specifies the name of the resource group from which this cmdlet removes a custom domain.</span></span>

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

### <span data-ttu-id="aa636-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="aa636-126">-Confirm</span></span>
<span data-ttu-id="aa636-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aa636-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa636-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa636-128">-WhatIf</span></span>
<span data-ttu-id="aa636-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa636-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa636-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aa636-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa636-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa636-131">CommonParameters</span></span>
<span data-ttu-id="aa636-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa636-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa636-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aa636-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa636-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa636-134">INPUTS</span></span>

### <span data-ttu-id="aa636-135">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="aa636-135">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="aa636-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aa636-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa636-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa636-137">OUTPUTS</span></span>

### <span data-ttu-id="aa636-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa636-138">System.Boolean</span></span>

## <span data-ttu-id="aa636-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa636-139">NOTES</span></span>

## <span data-ttu-id="aa636-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa636-140">RELATED LINKS</span></span>

[<span data-ttu-id="aa636-141">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="aa636-141">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="aa636-142">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="aa636-142">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="aa636-143">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="aa636-143">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


