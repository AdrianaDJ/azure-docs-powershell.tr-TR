---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 4a710507321d2f4eb2a605846928f66c5bdb6a4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763976"
---
# <span data-ttu-id="48333-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="48333-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="48333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48333-102">SYNOPSIS</span></span>
<span data-ttu-id="48333-103">Site kurtarma kasasından Hyper-V sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="48333-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48333-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48333-104">SYNTAX</span></span>

### <span data-ttu-id="48333-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="48333-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48333-106">ByName</span><span class="sxs-lookup"><span data-stu-id="48333-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48333-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="48333-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48333-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="48333-108">DESCRIPTION</span></span>
<span data-ttu-id="48333-109">**Get-AzureRmSiteRecoverySite** cmdlet 'ı, Azure Site Recovery kasasındaki Hyper-V sitelerini alır.</span><span class="sxs-lookup"><span data-stu-id="48333-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="48333-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48333-110">EXAMPLES</span></span>

## <span data-ttu-id="48333-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48333-111">PARAMETERS</span></span>

### <span data-ttu-id="48333-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48333-112">-DefaultProfile</span></span>
<span data-ttu-id="48333-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48333-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48333-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="48333-114">-FriendlyName</span></span>
<span data-ttu-id="48333-115">Sitenin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48333-115">Specifies the friendly name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48333-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="48333-116">-Name</span></span>
<span data-ttu-id="48333-117">Sitenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="48333-117">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48333-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48333-118">CommonParameters</span></span>
<span data-ttu-id="48333-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48333-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48333-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48333-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48333-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48333-121">INPUTS</span></span>

### <span data-ttu-id="48333-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="48333-122">None</span></span>
<span data-ttu-id="48333-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="48333-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48333-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48333-124">OUTPUTS</span></span>

### <span data-ttu-id="48333-125">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="48333-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="48333-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48333-126">NOTES</span></span>

## <span data-ttu-id="48333-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48333-127">RELATED LINKS</span></span>

[<span data-ttu-id="48333-128">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="48333-128">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="48333-129">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="48333-129">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
