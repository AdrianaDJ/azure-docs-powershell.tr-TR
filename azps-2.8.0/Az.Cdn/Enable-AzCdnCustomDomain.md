---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 5f7ad20d2a6243d52346600d4ae37e5a0505c8e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753094"
---
# <span data-ttu-id="35112-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="35112-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="35112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35112-102">SYNOPSIS</span></span>
<span data-ttu-id="35112-103">HTTPS (kullanım dışı) özel etki alanını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="35112-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="35112-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35112-104">SYNTAX</span></span>

### <span data-ttu-id="35112-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35112-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35112-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35112-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35112-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="35112-107">DESCRIPTION</span></span>
<span data-ttu-id="35112-108">**Enable-AzCdnCustomDomain** CMDLET 'i CDN özel etki ALANıNıN güvenli https teslimini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="35112-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="35112-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35112-109">EXAMPLES</span></span>

### <span data-ttu-id="35112-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="35112-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="35112-111">Özel etki alanının https teslimini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="35112-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="35112-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35112-112">PARAMETERS</span></span>

### <span data-ttu-id="35112-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="35112-113">-CustomDomainName</span></span>
<span data-ttu-id="35112-114">Azure CDN özel etki alanı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="35112-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="35112-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35112-115">-DefaultProfile</span></span>
<span data-ttu-id="35112-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="35112-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35112-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="35112-117">-EndpointName</span></span>
<span data-ttu-id="35112-118">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="35112-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="35112-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35112-119">-InputObject</span></span>
<span data-ttu-id="35112-120">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="35112-120">The custom domain object.</span></span>

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

### <span data-ttu-id="35112-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="35112-121">-PassThru</span></span>
<span data-ttu-id="35112-122">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="35112-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35112-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="35112-123">-ProfileName</span></span>
<span data-ttu-id="35112-124">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="35112-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="35112-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35112-125">-ResourceGroupName</span></span>
<span data-ttu-id="35112-126">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="35112-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="35112-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="35112-127">-Confirm</span></span>
<span data-ttu-id="35112-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="35112-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35112-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35112-129">-WhatIf</span></span>
<span data-ttu-id="35112-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="35112-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35112-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="35112-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35112-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35112-132">CommonParameters</span></span>
<span data-ttu-id="35112-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35112-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35112-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35112-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35112-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35112-135">INPUTS</span></span>

### <span data-ttu-id="35112-136">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="35112-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="35112-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35112-137">OUTPUTS</span></span>

### <span data-ttu-id="35112-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35112-138">System.Boolean</span></span>

## <span data-ttu-id="35112-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35112-139">NOTES</span></span>

## <span data-ttu-id="35112-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35112-140">RELATED LINKS</span></span>