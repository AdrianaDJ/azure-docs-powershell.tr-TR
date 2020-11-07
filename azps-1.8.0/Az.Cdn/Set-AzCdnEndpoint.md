---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnEndpoint.md
ms.openlocfilehash: cce3e2f9deb1f5df5c85d4f0b289b97e9cd36820
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761399"
---
# <span data-ttu-id="c7a04-101">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7a04-101">Set-AzCdnEndpoint</span></span>

## <span data-ttu-id="c7a04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a04-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a04-103">CDN uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c7a04-103">Updates a CDN endpoint.</span></span>

## <span data-ttu-id="c7a04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7a04-104">SYNTAX</span></span>

```
Set-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7a04-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7a04-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a04-106">**Set-AzCdnEndpoint** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c7a04-106">The **Set-AzCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="c7a04-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7a04-107">EXAMPLES</span></span>

## <span data-ttu-id="c7a04-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7a04-108">PARAMETERS</span></span>

### <span data-ttu-id="c7a04-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7a04-109">-CdnEndpoint</span></span>
<span data-ttu-id="c7a04-110">Bu cmdlet 'in güncelleştirdiği uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7a04-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="c7a04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a04-111">-DefaultProfile</span></span>
<span data-ttu-id="c7a04-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c7a04-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7a04-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7a04-113">-Confirm</span></span>
<span data-ttu-id="c7a04-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7a04-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a04-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a04-115">-WhatIf</span></span>
<span data-ttu-id="c7a04-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7a04-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a04-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7a04-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a04-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a04-118">CommonParameters</span></span>
<span data-ttu-id="c7a04-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7a04-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a04-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a04-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a04-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7a04-121">INPUTS</span></span>

### <span data-ttu-id="c7a04-122">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7a04-122">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c7a04-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7a04-123">OUTPUTS</span></span>

### <span data-ttu-id="c7a04-124">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7a04-124">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c7a04-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7a04-125">NOTES</span></span>

## <span data-ttu-id="c7a04-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7a04-126">RELATED LINKS</span></span>

[<span data-ttu-id="c7a04-127">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7a04-127">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="c7a04-128">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7a04-128">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="c7a04-129">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7a04-129">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="c7a04-130">Başlangıç-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7a04-130">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="c7a04-131">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c7a04-131">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


