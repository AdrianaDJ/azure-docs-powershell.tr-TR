---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 6feb7eb3f20e06c8dfffaa3dd9a1fb2bf3cc4c68
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591386"
---
# <span data-ttu-id="0e3c5-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e3c5-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="0e3c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e3c5-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3c5-103">CDN uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e3c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e3c5-104">SYNTAX</span></span>

### <span data-ttu-id="0e3c5-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e3c5-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e3c5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e3c5-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e3c5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e3c5-107">DESCRIPTION</span></span>
<span data-ttu-id="0e3c5-108">**Remove-AzureRmCdnEndpoint** cmdlet 'ı bir Azure Content Delivery Network (CDN) uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="0e3c5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e3c5-109">EXAMPLES</span></span>

## <span data-ttu-id="0e3c5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e3c5-110">PARAMETERS</span></span>

### <span data-ttu-id="0e3c5-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e3c5-111">-CdnEndpoint</span></span>
<span data-ttu-id="0e3c5-112">Bu cmdlet 'in kaldırıldığı uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0e3c5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3c5-113">-DefaultProfile</span></span>
<span data-ttu-id="0e3c5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0e3c5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e3c5-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0e3c5-115">-EndpointName</span></span>
<span data-ttu-id="0e3c5-116">Bu cmdlet 'in kaldırdığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0e3c5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0e3c5-117">-Force</span></span>
<span data-ttu-id="0e3c5-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0e3c5-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0e3c5-119">-PassThru</span></span>
<span data-ttu-id="0e3c5-120">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0e3c5-121">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0e3c5-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="0e3c5-122">-ProfileName</span></span>
<span data-ttu-id="0e3c5-123">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0e3c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e3c5-125">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="0e3c5-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e3c5-126">-Confirm</span></span>
<span data-ttu-id="0e3c5-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e3c5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e3c5-128">-WhatIf</span></span>
<span data-ttu-id="0e3c5-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e3c5-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e3c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3c5-131">CommonParameters</span></span>
<span data-ttu-id="0e3c5-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e3c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3c5-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e3c5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3c5-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e3c5-134">INPUTS</span></span>

### <span data-ttu-id="0e3c5-135">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e3c5-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="0e3c5-136">Parametreler: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0e3c5-136">Parameters: CdnEndpoint (ByValue)</span></span>

### <span data-ttu-id="0e3c5-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0e3c5-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0e3c5-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e3c5-138">OUTPUTS</span></span>

### <span data-ttu-id="0e3c5-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e3c5-139">System.Boolean</span></span>

## <span data-ttu-id="0e3c5-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e3c5-140">NOTES</span></span>

## <span data-ttu-id="0e3c5-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e3c5-141">RELATED LINKS</span></span>

[<span data-ttu-id="0e3c5-142">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e3c5-142">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0e3c5-143">Yeni-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e3c5-143">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0e3c5-144">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e3c5-144">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0e3c5-145">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e3c5-145">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="0e3c5-146">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e3c5-146">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)

