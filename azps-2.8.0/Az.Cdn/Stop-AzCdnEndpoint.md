---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: e732f9d9ca326e5c5f759b97925c3d16542f7d07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753039"
---
# <span data-ttu-id="5c089-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c089-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="5c089-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c089-102">SYNOPSIS</span></span>
<span data-ttu-id="5c089-103">CDN uç noktasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="5c089-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="5c089-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c089-104">SYNTAX</span></span>

### <span data-ttu-id="5c089-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5c089-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c089-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c089-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c089-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c089-107">DESCRIPTION</span></span>
<span data-ttu-id="5c089-108">**Stop-AzCdnEndpoint** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="5c089-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5c089-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c089-109">EXAMPLES</span></span>

## <span data-ttu-id="5c089-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c089-110">PARAMETERS</span></span>

### <span data-ttu-id="5c089-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c089-111">-CdnEndpoint</span></span>
<span data-ttu-id="5c089-112">Bu cmdlet 'in durduğu uç nokta nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c089-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c089-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c089-113">-DefaultProfile</span></span>
<span data-ttu-id="5c089-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5c089-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c089-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5c089-115">-EndpointName</span></span>
<span data-ttu-id="5c089-116">Bu cmdlet 'in durdurduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c089-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="5c089-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5c089-117">-PassThru</span></span>
<span data-ttu-id="5c089-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5c089-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5c089-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5c089-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c089-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5c089-120">-ProfileName</span></span>
<span data-ttu-id="5c089-121">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c089-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5c089-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c089-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c089-123">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c089-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5c089-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c089-124">-Confirm</span></span>
<span data-ttu-id="5c089-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c089-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c089-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c089-126">-WhatIf</span></span>
<span data-ttu-id="5c089-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c089-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c089-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c089-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c089-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c089-129">CommonParameters</span></span>
<span data-ttu-id="5c089-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c089-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c089-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5c089-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c089-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c089-132">INPUTS</span></span>

### <span data-ttu-id="5c089-133">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c089-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="5c089-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5c089-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5c089-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c089-135">OUTPUTS</span></span>

### <span data-ttu-id="5c089-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c089-136">System.Boolean</span></span>

## <span data-ttu-id="5c089-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c089-137">NOTES</span></span>

## <span data-ttu-id="5c089-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c089-138">RELATED LINKS</span></span>

[<span data-ttu-id="5c089-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c089-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="5c089-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c089-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="5c089-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c089-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="5c089-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c089-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="5c089-143">Başlangıç-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5c089-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


