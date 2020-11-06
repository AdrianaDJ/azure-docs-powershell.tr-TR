---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 49afefc7b80b5475735f61cb0511366b7f27a466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595204"
---
# <span data-ttu-id="e4acb-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4acb-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="e4acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4acb-102">SYNOPSIS</span></span>
<span data-ttu-id="e4acb-103">CDN uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4acb-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4acb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4acb-104">SYNTAX</span></span>

### <span data-ttu-id="e4acb-105">Alan parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="e4acb-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4acb-106">Nesne parametreleri için parametre kümesi</span><span class="sxs-lookup"><span data-stu-id="e4acb-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4acb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4acb-107">DESCRIPTION</span></span>
<span data-ttu-id="e4acb-108">**Remove-AzureRmCdnEndpoint** cmdlet 'ı bir Azure Content Delivery Network (CDN) uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4acb-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e4acb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4acb-109">EXAMPLES</span></span>

## <span data-ttu-id="e4acb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4acb-110">PARAMETERS</span></span>

### <span data-ttu-id="e4acb-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4acb-111">-CdnEndpoint</span></span>
<span data-ttu-id="e4acb-112">Bu cmdlet 'in kaldırıldığı uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4acb-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4acb-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e4acb-113">-EndpointName</span></span>
<span data-ttu-id="e4acb-114">Bu cmdlet 'in kaldırdığı uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4acb-114">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4acb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e4acb-115">-Force</span></span>
<span data-ttu-id="e4acb-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e4acb-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4acb-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e4acb-117">-PassThru</span></span>
<span data-ttu-id="e4acb-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e4acb-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e4acb-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e4acb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4acb-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e4acb-120">-ProfileName</span></span>
<span data-ttu-id="e4acb-121">Uç noktanın ait olduğu profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4acb-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e4acb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4acb-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4acb-123">Uç noktanın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4acb-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e4acb-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4acb-124">-Confirm</span></span>
<span data-ttu-id="e4acb-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4acb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4acb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4acb-126">-WhatIf</span></span>
<span data-ttu-id="e4acb-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4acb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4acb-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4acb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4acb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4acb-129">-DefaultProfile</span></span>
<span data-ttu-id="e4acb-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4acb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4acb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4acb-131">CommonParameters</span></span>
<span data-ttu-id="e4acb-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4acb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4acb-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4acb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4acb-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4acb-134">INPUTS</span></span>

### <span data-ttu-id="e4acb-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4acb-135">PSEndpoint</span></span>
<span data-ttu-id="e4acb-136">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="e4acb-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e4acb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4acb-137">OUTPUTS</span></span>

### <span data-ttu-id="e4acb-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4acb-138">System.Boolean</span></span>

## <span data-ttu-id="e4acb-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4acb-139">NOTES</span></span>

## <span data-ttu-id="e4acb-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4acb-140">RELATED LINKS</span></span>

[<span data-ttu-id="e4acb-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4acb-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e4acb-142">Yeni-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4acb-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e4acb-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4acb-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e4acb-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4acb-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="e4acb-145">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e4acb-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


