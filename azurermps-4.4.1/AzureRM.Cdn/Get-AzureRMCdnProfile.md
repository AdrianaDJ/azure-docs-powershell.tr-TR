---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: 726e84e1fe43e90ebf16241a017dadb2af5584b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593825"
---
# <span data-ttu-id="fa62a-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fa62a-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="fa62a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa62a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa62a-103">CDN profili alır.</span><span class="sxs-lookup"><span data-stu-id="fa62a-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa62a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa62a-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa62a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa62a-105">DESCRIPTION</span></span>
<span data-ttu-id="fa62a-106">**Get-AzureRMCdnProfile** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) profili ve ilgili bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="fa62a-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="fa62a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa62a-107">EXAMPLES</span></span>

## <span data-ttu-id="fa62a-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa62a-108">PARAMETERS</span></span>

### <span data-ttu-id="fa62a-109">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="fa62a-109">-ProfileName</span></span>
<span data-ttu-id="fa62a-110">Profilin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa62a-110">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="fa62a-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa62a-111">-ResourceGroupName</span></span>
<span data-ttu-id="fa62a-112">Profilin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa62a-112">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="fa62a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa62a-113">-DefaultProfile</span></span>
<span data-ttu-id="fa62a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa62a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa62a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa62a-115">CommonParameters</span></span>
<span data-ttu-id="fa62a-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa62a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa62a-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa62a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa62a-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa62a-118">INPUTS</span></span>

## <span data-ttu-id="fa62a-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa62a-119">OUTPUTS</span></span>

###  
<span data-ttu-id="fa62a-120">Bu cmdlet bir profil nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="fa62a-120">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="fa62a-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa62a-121">NOTES</span></span>

## <span data-ttu-id="fa62a-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa62a-122">RELATED LINKS</span></span>

[<span data-ttu-id="fa62a-123">Yeni-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fa62a-123">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="fa62a-124">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fa62a-124">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="fa62a-125">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="fa62a-125">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


