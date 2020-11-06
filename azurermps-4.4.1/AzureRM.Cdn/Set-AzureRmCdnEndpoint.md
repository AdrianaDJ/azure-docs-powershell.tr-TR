---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1A84AF77-1AEF-4FD0-9FAA-D195B361FCEB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnEndpoint.md
ms.openlocfilehash: 70a6e57b45e1703b06343cb66d5b83b526b55063
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591134"
---
# <span data-ttu-id="f728f-101">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f728f-101">Set-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="f728f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f728f-102">SYNOPSIS</span></span>
<span data-ttu-id="f728f-103">CDN uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f728f-103">Updates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f728f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f728f-104">SYNTAX</span></span>

```
Set-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f728f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f728f-105">DESCRIPTION</span></span>
<span data-ttu-id="f728f-106">**Set-AzureRmCdnEndpoint** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) uç noktasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f728f-106">The **Set-AzureRmCdnEndpoint** cmdlet updates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f728f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f728f-107">EXAMPLES</span></span>

## <span data-ttu-id="f728f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f728f-108">PARAMETERS</span></span>

### <span data-ttu-id="f728f-109">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f728f-109">-CdnEndpoint</span></span>
<span data-ttu-id="f728f-110">Bu cmdlet 'in güncelleştirdiği uç noktayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f728f-110">Specifies the endpoint that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f728f-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="f728f-111">-Confirm</span></span>
<span data-ttu-id="f728f-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f728f-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f728f-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f728f-113">-WhatIf</span></span>
<span data-ttu-id="f728f-114">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f728f-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f728f-115">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f728f-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f728f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f728f-116">-DefaultProfile</span></span>
<span data-ttu-id="f728f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f728f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f728f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f728f-118">CommonParameters</span></span>
<span data-ttu-id="f728f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f728f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f728f-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f728f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f728f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f728f-121">INPUTS</span></span>

### <span data-ttu-id="f728f-122">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f728f-122">PSEndpoint</span></span>
<span data-ttu-id="f728f-123">Parametre ' CdnEndpoint ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="f728f-123">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="f728f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f728f-124">OUTPUTS</span></span>

### <span data-ttu-id="f728f-125">Microsoft. Azure. Commands. CDN. modeller. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f728f-125">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f728f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f728f-126">NOTES</span></span>

## <span data-ttu-id="f728f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f728f-127">RELATED LINKS</span></span>

[<span data-ttu-id="f728f-128">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f728f-128">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f728f-129">Yeni-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f728f-129">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f728f-130">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f728f-130">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f728f-131">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f728f-131">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f728f-132">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f728f-132">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


