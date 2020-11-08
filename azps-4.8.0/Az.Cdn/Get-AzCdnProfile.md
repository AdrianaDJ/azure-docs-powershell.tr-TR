---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108162"
---
# <span data-ttu-id="eeb8c-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eeb8c-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="eeb8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeb8c-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb8c-103">CDN profili alır.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="eeb8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eeb8c-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eeb8c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eeb8c-105">DESCRIPTION</span></span>
<span data-ttu-id="eeb8c-106">**Get-AzCdnProfile** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) profili ve ilgili bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="eeb8c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eeb8c-107">EXAMPLES</span></span>

## <span data-ttu-id="eeb8c-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eeb8c-108">PARAMETERS</span></span>

### <span data-ttu-id="eeb8c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb8c-109">-DefaultProfile</span></span>
<span data-ttu-id="eeb8c-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eeb8c-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eeb8c-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="eeb8c-111">-ProfileName</span></span>
<span data-ttu-id="eeb8c-112">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb8c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb8c-113">-ResourceGroupName</span></span>
<span data-ttu-id="eeb8c-114">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeb8c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb8c-115">CommonParameters</span></span>
<span data-ttu-id="eeb8c-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb8c-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eeb8c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb8c-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eeb8c-118">INPUTS</span></span>

### <span data-ttu-id="eeb8c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="eeb8c-119">System.String</span></span>

## <span data-ttu-id="eeb8c-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eeb8c-120">OUTPUTS</span></span>

### <span data-ttu-id="eeb8c-121">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="eeb8c-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="eeb8c-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eeb8c-122">NOTES</span></span>

## <span data-ttu-id="eeb8c-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eeb8c-123">RELATED LINKS</span></span>

[<span data-ttu-id="eeb8c-124">New-Azcıdnprofile</span><span class="sxs-lookup"><span data-stu-id="eeb8c-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="eeb8c-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eeb8c-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="eeb8c-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="eeb8c-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


