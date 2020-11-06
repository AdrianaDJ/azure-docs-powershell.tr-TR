---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/enable-azurermcdncustomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Enable-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 50c1bf02a8952bbbddd2bbb82e55441adacd6a2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572921"
---
# <span data-ttu-id="8713f-101">Enable-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="8713f-101">Enable-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="8713f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8713f-102">SYNOPSIS</span></span>
<span data-ttu-id="8713f-103">Özel HTTPS 'yi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="8713f-103">Enables custom HTTPS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8713f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8713f-104">SYNTAX</span></span>

### <span data-ttu-id="8713f-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8713f-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzureRmCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8713f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8713f-106">ByObjectParameterSet</span></span>
```
Enable-AzureRmCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8713f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8713f-107">DESCRIPTION</span></span>
<span data-ttu-id="8713f-108">**Enable-AzureRmCdnCustomDomain** CMDLET 'i CDN özel etki ALANıNıN güvenli https teslimini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="8713f-108">The **Enable-AzureRmCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="8713f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8713f-109">EXAMPLES</span></span>

### <span data-ttu-id="8713f-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8713f-110">Example 1</span></span>
```powershell
Enable-AzureRmCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="8713f-111">Özel etki alanının https teslimini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="8713f-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="8713f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8713f-112">PARAMETERS</span></span>

### <span data-ttu-id="8713f-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="8713f-113">-CustomDomainName</span></span>
<span data-ttu-id="8713f-114">Azure CDN özel etki alanı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="8713f-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="8713f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8713f-115">-DefaultProfile</span></span>
<span data-ttu-id="8713f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8713f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8713f-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8713f-117">-EndpointName</span></span>
<span data-ttu-id="8713f-118">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="8713f-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="8713f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8713f-119">-InputObject</span></span>
<span data-ttu-id="8713f-120">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8713f-120">The custom domain object.</span></span>

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

### <span data-ttu-id="8713f-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8713f-121">-PassThru</span></span>
<span data-ttu-id="8713f-122">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="8713f-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="8713f-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8713f-123">-ProfileName</span></span>
<span data-ttu-id="8713f-124">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="8713f-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="8713f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8713f-125">-ResourceGroupName</span></span>
<span data-ttu-id="8713f-126">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8713f-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="8713f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="8713f-127">-Confirm</span></span>
<span data-ttu-id="8713f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8713f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8713f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8713f-129">-WhatIf</span></span>
<span data-ttu-id="8713f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8713f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8713f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8713f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8713f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8713f-132">CommonParameters</span></span>
<span data-ttu-id="8713f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8713f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8713f-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8713f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8713f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8713f-135">INPUTS</span></span>

### <span data-ttu-id="8713f-136">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="8713f-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>
<span data-ttu-id="8713f-137">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8713f-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8713f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8713f-138">OUTPUTS</span></span>

### <span data-ttu-id="8713f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8713f-139">System.Boolean</span></span>

## <span data-ttu-id="8713f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8713f-140">NOTES</span></span>

## <span data-ttu-id="8713f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8713f-141">RELATED LINKS</span></span>
