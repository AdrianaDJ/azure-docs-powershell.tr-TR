---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: eebc75ba8f8f1a55fb4c1db2e7929ce233d93a23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279211"
---
# <span data-ttu-id="a0d51-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a0d51-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="a0d51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0d51-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d51-103">HTTPS (kullanım dışı) özel etki alanını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="a0d51-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="a0d51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0d51-104">SYNTAX</span></span>

### <span data-ttu-id="a0d51-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a0d51-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0d51-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0d51-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0d51-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0d51-107">DESCRIPTION</span></span>
<span data-ttu-id="a0d51-108">**Enable-AzCdnCustomDomain** CMDLET 'i CDN özel etki ALANıNıN güvenli https teslimini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="a0d51-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="a0d51-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0d51-109">EXAMPLES</span></span>

### <span data-ttu-id="a0d51-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a0d51-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="a0d51-111">Özel etki alanının https teslimini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="a0d51-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="a0d51-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0d51-112">PARAMETERS</span></span>

### <span data-ttu-id="a0d51-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="a0d51-113">-CustomDomainName</span></span>
<span data-ttu-id="a0d51-114">Azure CDN özel etki alanı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="a0d51-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="a0d51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d51-115">-DefaultProfile</span></span>
<span data-ttu-id="a0d51-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a0d51-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0d51-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a0d51-117">-EndpointName</span></span>
<span data-ttu-id="a0d51-118">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="a0d51-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a0d51-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0d51-119">-InputObject</span></span>
<span data-ttu-id="a0d51-120">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a0d51-120">The custom domain object.</span></span>

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

### <span data-ttu-id="a0d51-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a0d51-121">-PassThru</span></span>
<span data-ttu-id="a0d51-122">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="a0d51-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="a0d51-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a0d51-123">-ProfileName</span></span>
<span data-ttu-id="a0d51-124">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="a0d51-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a0d51-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d51-125">-ResourceGroupName</span></span>
<span data-ttu-id="a0d51-126">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a0d51-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="a0d51-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="a0d51-127">-Confirm</span></span>
<span data-ttu-id="a0d51-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a0d51-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d51-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d51-129">-WhatIf</span></span>
<span data-ttu-id="a0d51-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a0d51-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0d51-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a0d51-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d51-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d51-132">CommonParameters</span></span>
<span data-ttu-id="a0d51-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0d51-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d51-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a0d51-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d51-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0d51-135">INPUTS</span></span>

### <span data-ttu-id="a0d51-136">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="a0d51-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="a0d51-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0d51-137">OUTPUTS</span></span>

### <span data-ttu-id="a0d51-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0d51-138">System.Boolean</span></span>

## <span data-ttu-id="a0d51-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0d51-139">NOTES</span></span>

## <span data-ttu-id="a0d51-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0d51-140">RELATED LINKS</span></span>
