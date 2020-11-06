---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 7f8dfed861abd9d426a72c5d66f7c41b4efc947e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587776"
---
# <span data-ttu-id="982af-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="982af-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="982af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="982af-102">SYNOPSIS</span></span>
<span data-ttu-id="982af-103">Site kurtarma sitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="982af-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="982af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="982af-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="982af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="982af-105">DESCRIPTION</span></span>
<span data-ttu-id="982af-106">**New-AzureRmSiteRecoverySite** cmdlet 'i geçerli kasada bir Azure Site kurtarma sitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="982af-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="982af-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="982af-107">EXAMPLES</span></span>

## <span data-ttu-id="982af-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="982af-108">PARAMETERS</span></span>

### <span data-ttu-id="982af-109">-Ad</span><span class="sxs-lookup"><span data-stu-id="982af-109">-Name</span></span>
<span data-ttu-id="982af-110">Sitenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="982af-110">Specifies the name of the site.</span></span>

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

### <span data-ttu-id="982af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="982af-111">-DefaultProfile</span></span>
<span data-ttu-id="982af-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="982af-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="982af-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982af-113">CommonParameters</span></span>
<span data-ttu-id="982af-114">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="982af-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982af-115">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="982af-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982af-116">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="982af-116">INPUTS</span></span>

## <span data-ttu-id="982af-117">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="982af-117">OUTPUTS</span></span>

## <span data-ttu-id="982af-118">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="982af-118">NOTES</span></span>

## <span data-ttu-id="982af-119">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="982af-119">RELATED LINKS</span></span>

[<span data-ttu-id="982af-120">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="982af-120">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="982af-121">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="982af-121">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
