---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 20206ebf99d597a2961804bf3062cd4c049f8017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763471"
---
# <span data-ttu-id="01c66-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="01c66-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="01c66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01c66-102">SYNOPSIS</span></span>
<span data-ttu-id="01c66-103">CDN uç noktasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="01c66-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01c66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01c66-104">SYNTAX</span></span>

### <span data-ttu-id="01c66-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="01c66-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01c66-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01c66-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01c66-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="01c66-107">DESCRIPTION</span></span>
<span data-ttu-id="01c66-108">**Stop-AzureRmCdnEndpoint** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="01c66-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="01c66-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01c66-109">EXAMPLES</span></span>

## <span data-ttu-id="01c66-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01c66-110">PARAMETERS</span></span>

### <span data-ttu-id="01c66-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="01c66-111">-CdnEndpoint</span></span>
<span data-ttu-id="01c66-112">Bu cmdlet 'in durduğu uç nokta nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01c66-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="01c66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01c66-113">-DefaultProfile</span></span>
<span data-ttu-id="01c66-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="01c66-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01c66-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="01c66-115">-EndpointName</span></span>
<span data-ttu-id="01c66-116">Bu cmdlet 'in durdurduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01c66-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="01c66-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="01c66-117">-PassThru</span></span>
<span data-ttu-id="01c66-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="01c66-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="01c66-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="01c66-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="01c66-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="01c66-120">-ProfileName</span></span>
<span data-ttu-id="01c66-121">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01c66-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="01c66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01c66-122">-ResourceGroupName</span></span>
<span data-ttu-id="01c66-123">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01c66-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="01c66-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="01c66-124">-Confirm</span></span>
<span data-ttu-id="01c66-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01c66-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01c66-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01c66-126">-WhatIf</span></span>
<span data-ttu-id="01c66-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01c66-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01c66-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01c66-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01c66-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01c66-129">CommonParameters</span></span>
<span data-ttu-id="01c66-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01c66-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01c66-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01c66-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01c66-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01c66-132">INPUTS</span></span>

### <span data-ttu-id="01c66-133">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="01c66-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="01c66-134">Parametreler: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01c66-134">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="01c66-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="01c66-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="01c66-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01c66-136">OUTPUTS</span></span>

### <span data-ttu-id="01c66-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01c66-137">System.Boolean</span></span>

## <span data-ttu-id="01c66-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01c66-138">NOTES</span></span>

## <span data-ttu-id="01c66-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01c66-139">RELATED LINKS</span></span>

[<span data-ttu-id="01c66-140">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="01c66-140">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="01c66-141">Yeni-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="01c66-141">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="01c66-142">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="01c66-142">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="01c66-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="01c66-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="01c66-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="01c66-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


