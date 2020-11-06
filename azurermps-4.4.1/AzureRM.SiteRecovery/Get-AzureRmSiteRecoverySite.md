---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: e41b491611ebc5dda1da56ac26827c5fa547dd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589072"
---
# <span data-ttu-id="e5d63-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e5d63-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="e5d63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5d63-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d63-103">Site kurtarma kasasından Hyper-V sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e5d63-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5d63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5d63-104">SYNTAX</span></span>

### <span data-ttu-id="e5d63-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5d63-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5d63-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e5d63-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5d63-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e5d63-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5d63-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5d63-108">DESCRIPTION</span></span>
<span data-ttu-id="e5d63-109">**Get-AzureRmSiteRecoverySite** cmdlet 'ı, Azure Site Recovery kasasındaki Hyper-V sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e5d63-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="e5d63-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5d63-110">EXAMPLES</span></span>

## <span data-ttu-id="e5d63-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5d63-111">PARAMETERS</span></span>

### <span data-ttu-id="e5d63-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e5d63-112">-FriendlyName</span></span>
<span data-ttu-id="e5d63-113">Sitenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5d63-113">Specifies the friendly name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d63-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5d63-114">-Name</span></span>
<span data-ttu-id="e5d63-115">Sitenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5d63-115">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d63-116">-DefaultProfile</span></span>
<span data-ttu-id="e5d63-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5d63-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5d63-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d63-118">CommonParameters</span></span>
<span data-ttu-id="e5d63-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5d63-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d63-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5d63-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d63-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5d63-121">INPUTS</span></span>

## <span data-ttu-id="e5d63-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5d63-122">OUTPUTS</span></span>

### <span data-ttu-id="e5d63-123">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="e5d63-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="e5d63-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5d63-124">NOTES</span></span>

## <span data-ttu-id="e5d63-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5d63-125">RELATED LINKS</span></span>

[<span data-ttu-id="e5d63-126">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e5d63-126">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="e5d63-127">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e5d63-127">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
