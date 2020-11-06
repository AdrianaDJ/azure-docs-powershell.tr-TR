---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 83229b9251e7cbbbe4bd17d73004b9bc64800511
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591128"
---
# <span data-ttu-id="56a70-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a70-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="56a70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56a70-102">SYNOPSIS</span></span>
<span data-ttu-id="56a70-103">CDN uç noktasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="56a70-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56a70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56a70-104">SYNTAX</span></span>

### <span data-ttu-id="56a70-105">Alanlar parametrelerinin parametre kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56a70-105">Parameter Set for fields parameters (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56a70-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="56a70-106">Parameter Set for object parameters</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56a70-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="56a70-107">DESCRIPTION</span></span>
<span data-ttu-id="56a70-108">**Stop-AzureRmCdnEndpoint** cmdlet 'ı, Azure Içerik teslim ağı (CDN) uç noktasını durdurur.</span><span class="sxs-lookup"><span data-stu-id="56a70-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="56a70-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56a70-109">EXAMPLES</span></span>

## <span data-ttu-id="56a70-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56a70-110">PARAMETERS</span></span>

### <span data-ttu-id="56a70-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a70-111">-CdnEndpoint</span></span>
<span data-ttu-id="56a70-112">Bu cmdlet 'in durduğu uç nokta nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="56a70-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56a70-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="56a70-113">-EndpointName</span></span>
<span data-ttu-id="56a70-114">Bu cmdlet 'in durdurduğu uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56a70-114">Specifies the name of the endpoint that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56a70-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="56a70-115">-PassThru</span></span>
<span data-ttu-id="56a70-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="56a70-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="56a70-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="56a70-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="56a70-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="56a70-118">-ProfileName</span></span>
<span data-ttu-id="56a70-119">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56a70-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56a70-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56a70-120">-ResourceGroupName</span></span>
<span data-ttu-id="56a70-121">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56a70-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56a70-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="56a70-122">-Confirm</span></span>
<span data-ttu-id="56a70-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="56a70-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56a70-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56a70-124">-WhatIf</span></span>
<span data-ttu-id="56a70-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="56a70-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56a70-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="56a70-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56a70-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56a70-127">-DefaultProfile</span></span>
<span data-ttu-id="56a70-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56a70-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56a70-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56a70-129">CommonParameters</span></span>
<span data-ttu-id="56a70-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56a70-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56a70-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56a70-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56a70-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56a70-132">INPUTS</span></span>

### <span data-ttu-id="56a70-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a70-133">PSEndpoint</span></span>
<span data-ttu-id="56a70-134">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="56a70-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="56a70-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56a70-135">OUTPUTS</span></span>

### <span data-ttu-id="56a70-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56a70-136">System.Boolean</span></span>

## <span data-ttu-id="56a70-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56a70-137">NOTES</span></span>

## <span data-ttu-id="56a70-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56a70-138">RELATED LINKS</span></span>

[<span data-ttu-id="56a70-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a70-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="56a70-140">Yeni-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a70-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="56a70-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a70-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="56a70-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a70-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="56a70-143">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="56a70-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


