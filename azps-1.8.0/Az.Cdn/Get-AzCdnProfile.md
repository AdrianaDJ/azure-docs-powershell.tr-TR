---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 110528c1e7a9891381ebc8182a1e0b45267d87b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761413"
---
# <span data-ttu-id="a4e40-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a4e40-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="a4e40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4e40-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e40-103">CDN profili alır.</span><span class="sxs-lookup"><span data-stu-id="a4e40-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="a4e40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4e40-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4e40-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4e40-105">DESCRIPTION</span></span>
<span data-ttu-id="a4e40-106">**Get-AzCdnProfile** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) profili ve ilgili bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="a4e40-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="a4e40-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4e40-107">EXAMPLES</span></span>

## <span data-ttu-id="a4e40-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4e40-108">PARAMETERS</span></span>

### <span data-ttu-id="a4e40-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e40-109">-DefaultProfile</span></span>
<span data-ttu-id="a4e40-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a4e40-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4e40-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a4e40-111">-ProfileName</span></span>
<span data-ttu-id="a4e40-112">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4e40-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="a4e40-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4e40-113">-ResourceGroupName</span></span>
<span data-ttu-id="a4e40-114">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4e40-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="a4e40-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e40-115">CommonParameters</span></span>
<span data-ttu-id="a4e40-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4e40-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e40-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4e40-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e40-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4e40-118">INPUTS</span></span>

### <span data-ttu-id="a4e40-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a4e40-119">System.String</span></span>

## <span data-ttu-id="a4e40-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4e40-120">OUTPUTS</span></span>

### <span data-ttu-id="a4e40-121">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="a4e40-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="a4e40-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4e40-122">NOTES</span></span>

## <span data-ttu-id="a4e40-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4e40-123">RELATED LINKS</span></span>

[<span data-ttu-id="a4e40-124">New-Azcıdnprofile</span><span class="sxs-lookup"><span data-stu-id="a4e40-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="a4e40-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a4e40-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="a4e40-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a4e40-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


