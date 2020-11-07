---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomain.md
ms.openlocfilehash: 42de9254bc5bdaf31aa965aa7bdd1512cad361f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761425"
---
# <span data-ttu-id="19e70-101">Enable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="19e70-101">Enable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="19e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19e70-102">SYNOPSIS</span></span>
<span data-ttu-id="19e70-103">HTTPS (kullanım dışı) özel etki alanını etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="19e70-103">Enables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="19e70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19e70-104">SYNTAX</span></span>

### <span data-ttu-id="19e70-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="19e70-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19e70-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19e70-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19e70-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="19e70-107">DESCRIPTION</span></span>
<span data-ttu-id="19e70-108">**Enable-AzCdnCustomDomain** CMDLET 'i CDN özel etki ALANıNıN güvenli https teslimini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="19e70-108">The **Enable-AzCdnCustomDomain** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="19e70-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19e70-109">EXAMPLES</span></span>

### <span data-ttu-id="19e70-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="19e70-110">Example 1</span></span>
```powershell
Enable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="19e70-111">Özel etki alanının https teslimini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="19e70-111">Enable https delivery of the custom domain.</span></span>

## <span data-ttu-id="19e70-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19e70-112">PARAMETERS</span></span>

### <span data-ttu-id="19e70-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="19e70-113">-CustomDomainName</span></span>
<span data-ttu-id="19e70-114">Azure CDN özel etki alanı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="19e70-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="19e70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e70-115">-DefaultProfile</span></span>
<span data-ttu-id="19e70-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19e70-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19e70-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="19e70-117">-EndpointName</span></span>
<span data-ttu-id="19e70-118">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="19e70-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="19e70-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19e70-119">-InputObject</span></span>
<span data-ttu-id="19e70-120">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="19e70-120">The custom domain object.</span></span>

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

### <span data-ttu-id="19e70-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="19e70-121">-PassThru</span></span>
<span data-ttu-id="19e70-122">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="19e70-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="19e70-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="19e70-123">-ProfileName</span></span>
<span data-ttu-id="19e70-124">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="19e70-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="19e70-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19e70-125">-ResourceGroupName</span></span>
<span data-ttu-id="19e70-126">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="19e70-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="19e70-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="19e70-127">-Confirm</span></span>
<span data-ttu-id="19e70-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19e70-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19e70-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19e70-129">-WhatIf</span></span>
<span data-ttu-id="19e70-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19e70-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19e70-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19e70-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19e70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e70-132">CommonParameters</span></span>
<span data-ttu-id="19e70-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19e70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e70-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19e70-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e70-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19e70-135">INPUTS</span></span>

### <span data-ttu-id="19e70-136">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="19e70-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="19e70-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19e70-137">OUTPUTS</span></span>

### <span data-ttu-id="19e70-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19e70-138">System.Boolean</span></span>

## <span data-ttu-id="19e70-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19e70-139">NOTES</span></span>

## <span data-ttu-id="19e70-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19e70-140">RELATED LINKS</span></span>
