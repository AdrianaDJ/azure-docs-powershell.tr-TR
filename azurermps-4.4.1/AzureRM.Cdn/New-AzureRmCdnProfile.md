---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 2785A8E5-6905-4EDE-BFE1-FF7B1E386A39
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnProfile.md
ms.openlocfilehash: 0e69e48d29c96163acbb82ffe691de6affe8d131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592656"
---
# <span data-ttu-id="9854e-101">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9854e-101">New-AzureRmCdnProfile</span></span>

## <span data-ttu-id="9854e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9854e-102">SYNOPSIS</span></span>
<span data-ttu-id="9854e-103">CDN profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9854e-103">Creates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9854e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9854e-104">SYNTAX</span></span>

```
New-AzureRmCdnProfile -ProfileName <String> -Location <String> -Sku <PSSkuName> -ResourceGroupName <String>
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9854e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9854e-105">DESCRIPTION</span></span>
<span data-ttu-id="9854e-106">**Yeni-AzureRmCdnProfile** cmdlet 'ı bir Azure Içerik teslim ağı (CDN) profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9854e-106">The **New-AzureRmCdnProfile** cmdlet creates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="9854e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9854e-107">EXAMPLES</span></span>

## <span data-ttu-id="9854e-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9854e-108">PARAMETERS</span></span>

### <span data-ttu-id="9854e-109">-Konum</span><span class="sxs-lookup"><span data-stu-id="9854e-109">-Location</span></span>
<span data-ttu-id="9854e-110">Profilin kaynak konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9854e-110">Specifies the resource location of the profile.</span></span>

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

### <span data-ttu-id="9854e-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9854e-111">-ProfileName</span></span>
<span data-ttu-id="9854e-112">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9854e-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="9854e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9854e-113">-ResourceGroupName</span></span>
<span data-ttu-id="9854e-114">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9854e-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="9854e-115">-SKU</span><span class="sxs-lookup"><span data-stu-id="9854e-115">-Sku</span></span>
<span data-ttu-id="9854e-116">Profilin SKU adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9854e-116">Specifies the SKU of the profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSSkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Verizon, Premium_Verizon, Custom_Verizon, Standard_Akamai, Standard_ChinaCdn

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9854e-117">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="9854e-117">-Tags</span></span>
<span data-ttu-id="9854e-118">Bu profille ilişkilendirilmiş etiketlerin karma tablosunu büyütür.</span><span class="sxs-lookup"><span data-stu-id="9854e-118">Sepcifies a hash table of tags that are associated with this profile.</span></span>

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

### <span data-ttu-id="9854e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="9854e-119">-Confirm</span></span>
<span data-ttu-id="9854e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9854e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9854e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9854e-121">-WhatIf</span></span>
<span data-ttu-id="9854e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9854e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9854e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9854e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9854e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9854e-124">-DefaultProfile</span></span>
<span data-ttu-id="9854e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9854e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9854e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9854e-126">CommonParameters</span></span>
<span data-ttu-id="9854e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9854e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9854e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9854e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9854e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9854e-129">INPUTS</span></span>

## <span data-ttu-id="9854e-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9854e-130">OUTPUTS</span></span>

### <span data-ttu-id="9854e-131">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="9854e-131">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="9854e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9854e-132">NOTES</span></span>

## <span data-ttu-id="9854e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9854e-133">RELATED LINKS</span></span>

[<span data-ttu-id="9854e-134">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9854e-134">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="9854e-135">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9854e-135">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="9854e-136">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="9854e-136">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


