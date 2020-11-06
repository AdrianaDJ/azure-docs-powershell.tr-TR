---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: f53b02d54164b6cc4e3aad8cf07357e7f2e156e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593714"
---
# <span data-ttu-id="a9fe2-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe2-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="a9fe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fe2-103">CDN profili alır.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9fe2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9fe2-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9fe2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9fe2-105">DESCRIPTION</span></span>
<span data-ttu-id="a9fe2-106">**Get-AzureRMCdnProfile** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) profili ve ilgili bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="a9fe2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9fe2-107">EXAMPLES</span></span>

## <span data-ttu-id="a9fe2-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9fe2-108">PARAMETERS</span></span>

### <span data-ttu-id="a9fe2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe2-109">-DefaultProfile</span></span>
<span data-ttu-id="a9fe2-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a9fe2-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9fe2-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a9fe2-111">-ProfileName</span></span>
<span data-ttu-id="a9fe2-112">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="a9fe2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fe2-113">-ResourceGroupName</span></span>
<span data-ttu-id="a9fe2-114">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="a9fe2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fe2-115">CommonParameters</span></span>
<span data-ttu-id="a9fe2-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9fe2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fe2-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9fe2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fe2-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9fe2-118">INPUTS</span></span>

### <span data-ttu-id="a9fe2-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a9fe2-119">System.String</span></span>

## <span data-ttu-id="a9fe2-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9fe2-120">OUTPUTS</span></span>

### <span data-ttu-id="a9fe2-121">Microsoft. Azure. Commands. CDN. model. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe2-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="a9fe2-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9fe2-122">NOTES</span></span>

## <span data-ttu-id="a9fe2-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9fe2-123">RELATED LINKS</span></span>

[<span data-ttu-id="a9fe2-124">Yeni-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe2-124">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="a9fe2-125">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe2-125">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="a9fe2-126">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="a9fe2-126">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


