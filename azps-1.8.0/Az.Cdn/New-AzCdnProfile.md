---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnProfile.md
ms.openlocfilehash: 703b686f11d7d55cc77bcfde929f9a9f261070f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761406"
---
# <span data-ttu-id="4834e-101">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4834e-101">New-AzCdnProfile</span></span>

## <span data-ttu-id="4834e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4834e-102">SYNOPSIS</span></span>
<span data-ttu-id="4834e-103">CDN profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4834e-103">Creates a CDN profile.</span></span>

## <span data-ttu-id="4834e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4834e-104">SYNTAX</span></span>

```
New-AzCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4834e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4834e-105">DESCRIPTION</span></span>
<span data-ttu-id="4834e-106">**New-Azcıdnprofile** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4834e-106">The **New-AzCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="4834e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4834e-107">EXAMPLES</span></span>

## <span data-ttu-id="4834e-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4834e-108">PARAMETERS</span></span>

### <span data-ttu-id="4834e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4834e-109">-DefaultProfile</span></span>
<span data-ttu-id="4834e-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4834e-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4834e-111">-Konum</span><span class="sxs-lookup"><span data-stu-id="4834e-111">-Location</span></span>
<span data-ttu-id="4834e-112">Profilin kaynak konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4834e-112">Specifies the resource location of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4834e-113">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4834e-113">-ProfileName</span></span>
<span data-ttu-id="4834e-114">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4834e-114">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4834e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4834e-115">-ResourceGroupName</span></span>
<span data-ttu-id="4834e-116">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4834e-116">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4834e-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="4834e-117">-Sku</span></span>
<span data-ttu-id="4834e-118">Profilin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4834e-118">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn, Standard_Microsoft

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4834e-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4834e-119">-Tag</span></span>
<span data-ttu-id="4834e-120">Azure CDN profiliyle ilişkilendirilecek Etiketler.</span><span class="sxs-lookup"><span data-stu-id="4834e-120">The tags to associate with the Azure CDN profile.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4834e-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="4834e-121">-Confirm</span></span>
<span data-ttu-id="4834e-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4834e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4834e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4834e-123">-WhatIf</span></span>
<span data-ttu-id="4834e-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4834e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4834e-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4834e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4834e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4834e-126">CommonParameters</span></span>
<span data-ttu-id="4834e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4834e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4834e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4834e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4834e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4834e-129">INPUTS</span></span>

### <span data-ttu-id="4834e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4834e-130">System.String</span></span>

## <span data-ttu-id="4834e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4834e-131">OUTPUTS</span></span>

### <span data-ttu-id="4834e-132">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4834e-132">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4834e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4834e-133">NOTES</span></span>

## <span data-ttu-id="4834e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4834e-134">RELATED LINKS</span></span>

[<span data-ttu-id="4834e-135">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4834e-135">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="4834e-136">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4834e-136">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="4834e-137">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="4834e-137">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


