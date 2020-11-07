---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 8216d6404cb184767b03acd92f6549c2b8eda2e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917552"
---
# <span data-ttu-id="996a1-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="996a1-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="996a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="996a1-102">SYNOPSIS</span></span>
<span data-ttu-id="996a1-103">CDN uç noktası başlatır.</span><span class="sxs-lookup"><span data-stu-id="996a1-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="996a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="996a1-104">SYNTAX</span></span>

### <span data-ttu-id="996a1-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="996a1-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="996a1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="996a1-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="996a1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="996a1-107">DESCRIPTION</span></span>
<span data-ttu-id="996a1-108">**Start-AzCdnEndpoint** cmdlet 'ı bir Azure Content Delivery Network (CDN) uç noktasını başlatır.</span><span class="sxs-lookup"><span data-stu-id="996a1-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="996a1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="996a1-109">EXAMPLES</span></span>

## <span data-ttu-id="996a1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="996a1-110">PARAMETERS</span></span>

### <span data-ttu-id="996a1-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="996a1-111">-CdnEndpoint</span></span>
<span data-ttu-id="996a1-112">Bu cmdlet 'in başladığı uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="996a1-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="996a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996a1-113">-DefaultProfile</span></span>
<span data-ttu-id="996a1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="996a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="996a1-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="996a1-115">-EndpointName</span></span>
<span data-ttu-id="996a1-116">Bu cmdlet 'in başladığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="996a1-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="996a1-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="996a1-117">-PassThru</span></span>
<span data-ttu-id="996a1-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="996a1-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="996a1-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="996a1-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="996a1-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="996a1-120">-ProfileName</span></span>
<span data-ttu-id="996a1-121">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="996a1-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="996a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="996a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="996a1-123">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="996a1-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="996a1-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="996a1-124">-Confirm</span></span>
<span data-ttu-id="996a1-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="996a1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="996a1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="996a1-126">-WhatIf</span></span>
<span data-ttu-id="996a1-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="996a1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="996a1-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="996a1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="996a1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996a1-129">CommonParameters</span></span>
<span data-ttu-id="996a1-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="996a1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996a1-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="996a1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996a1-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="996a1-132">INPUTS</span></span>

### <span data-ttu-id="996a1-133">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="996a1-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="996a1-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="996a1-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="996a1-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="996a1-135">OUTPUTS</span></span>

### <span data-ttu-id="996a1-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="996a1-136">System.Boolean</span></span>

## <span data-ttu-id="996a1-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="996a1-137">NOTES</span></span>

## <span data-ttu-id="996a1-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="996a1-138">RELATED LINKS</span></span>

[<span data-ttu-id="996a1-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="996a1-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="996a1-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="996a1-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="996a1-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="996a1-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="996a1-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="996a1-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="996a1-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="996a1-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


