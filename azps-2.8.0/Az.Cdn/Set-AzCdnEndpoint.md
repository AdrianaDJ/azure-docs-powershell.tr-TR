---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: c84b91e70d428a7ba05aa3766bf1a63840b6ffa4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753047"
---
# <span data-ttu-id="dff67-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dff67-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="dff67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dff67-102">SYNOPSIS</span></span>
<span data-ttu-id="dff67-103">CDN uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dff67-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="dff67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dff67-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dff67-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dff67-105">DESCRIPTION</span></span>
<span data-ttu-id="dff67-106">**Set-AzCdnEndpoint** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="dff67-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="dff67-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dff67-107">EXAMPLES</span></span>

## <span data-ttu-id="dff67-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dff67-108">PARAMETERS</span></span>

### <span data-ttu-id="dff67-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dff67-109">-CdnEndpoint</span></span>
<span data-ttu-id="dff67-110">Bu cmdlet 'in güncelleştirdiği uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="dff67-110">Specifies the endpoint that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dff67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff67-111">-DefaultProfile</span></span>
<span data-ttu-id="dff67-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dff67-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dff67-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="dff67-113">-Confirm</span></span>
<span data-ttu-id="dff67-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dff67-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dff67-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dff67-115">-WhatIf</span></span>
<span data-ttu-id="dff67-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dff67-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dff67-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dff67-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dff67-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff67-118">CommonParameters</span></span>
<span data-ttu-id="dff67-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dff67-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff67-120">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dff67-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff67-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dff67-121">INPUTS</span></span>

### <span data-ttu-id="dff67-122">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dff67-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="dff67-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dff67-123">OUTPUTS</span></span>

### <span data-ttu-id="dff67-124">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dff67-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="dff67-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dff67-125">NOTES</span></span>

## <span data-ttu-id="dff67-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dff67-126">RELATED LINKS</span></span>

[<span data-ttu-id="dff67-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dff67-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="dff67-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dff67-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="dff67-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dff67-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="dff67-130">Başlangıç-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dff67-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="dff67-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dff67-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


