---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098311"
---
# <span data-ttu-id="3c46f-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c46f-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="3c46f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c46f-102">SYNOPSIS</span></span>
<span data-ttu-id="3c46f-103">CDN uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c46f-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="3c46f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c46f-104">SYNTAX</span></span>

### <span data-ttu-id="3c46f-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c46f-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c46f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c46f-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c46f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c46f-107">DESCRIPTION</span></span>
<span data-ttu-id="3c46f-108">**Remove-AzCdnEndpoint** cmdlet 'ı bir Azure Content Delivery Network (CDN) uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3c46f-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="3c46f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c46f-109">EXAMPLES</span></span>

## <span data-ttu-id="3c46f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c46f-110">PARAMETERS</span></span>

### <span data-ttu-id="3c46f-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c46f-111">-CdnEndpoint</span></span>
<span data-ttu-id="3c46f-112">Bu cmdlet 'in kaldırıldığı uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c46f-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3c46f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c46f-113">-DefaultProfile</span></span>
<span data-ttu-id="3c46f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3c46f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c46f-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="3c46f-115">-EndpointName</span></span>
<span data-ttu-id="3c46f-116">Bu cmdlet 'in kaldırdığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c46f-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3c46f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3c46f-117">-Force</span></span>
<span data-ttu-id="3c46f-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3c46f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3c46f-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3c46f-119">-PassThru</span></span>
<span data-ttu-id="3c46f-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="3c46f-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3c46f-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="3c46f-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3c46f-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3c46f-122">-ProfileName</span></span>
<span data-ttu-id="3c46f-123">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c46f-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3c46f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c46f-124">-ResourceGroupName</span></span>
<span data-ttu-id="3c46f-125">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c46f-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="3c46f-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c46f-126">-Confirm</span></span>
<span data-ttu-id="3c46f-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c46f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c46f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c46f-128">-WhatIf</span></span>
<span data-ttu-id="3c46f-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c46f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c46f-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c46f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c46f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c46f-131">CommonParameters</span></span>
<span data-ttu-id="3c46f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c46f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c46f-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3c46f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c46f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c46f-134">INPUTS</span></span>

### <span data-ttu-id="3c46f-135">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c46f-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="3c46f-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3c46f-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3c46f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c46f-137">OUTPUTS</span></span>

### <span data-ttu-id="3c46f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c46f-138">System.Boolean</span></span>

## <span data-ttu-id="3c46f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c46f-139">NOTES</span></span>

## <span data-ttu-id="3c46f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c46f-140">RELATED LINKS</span></span>

[<span data-ttu-id="3c46f-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c46f-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="3c46f-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c46f-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="3c46f-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c46f-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="3c46f-144">Başlangıç-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c46f-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="3c46f-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c46f-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)

