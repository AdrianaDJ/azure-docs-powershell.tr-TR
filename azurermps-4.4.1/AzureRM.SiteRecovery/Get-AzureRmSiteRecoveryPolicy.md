---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 07F9EE13-9874-42FC-A17E-7615419F1381
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 443abbab086fe08ac0a667776a07c792115aa5dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593792"
---
# <span data-ttu-id="1656d-101">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="1656d-101">Get-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="1656d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1656d-102">SYNOPSIS</span></span>
<span data-ttu-id="1656d-103">Site Recovery koruma ilkelerini alır.</span><span class="sxs-lookup"><span data-stu-id="1656d-103">Gets Site Recovery protection policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1656d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1656d-104">SYNTAX</span></span>

### <span data-ttu-id="1656d-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1656d-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1656d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1656d-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1656d-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="1656d-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryPolicy -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1656d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1656d-108">DESCRIPTION</span></span>
<span data-ttu-id="1656d-109">**Get-AzureRmSiteRecoveryPolicy** cmdlet 'ı yapılandırılmış Azure Site Recovery koruma ilkelerinin listesini veya belirli bir koruma ilkesi adını kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="1656d-109">The **Get-AzureRmSiteRecoveryPolicy** cmdlet gets the list of configured Azure Site Recovery protection policies or a specific protection policy by name.</span></span>

## <span data-ttu-id="1656d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1656d-110">EXAMPLES</span></span>

## <span data-ttu-id="1656d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1656d-111">PARAMETERS</span></span>

### <span data-ttu-id="1656d-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1656d-112">-FriendlyName</span></span>
<span data-ttu-id="1656d-113">Site kurtarma çoğaltma ilkesinin kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1656d-113">Specifies the friendly name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="1656d-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="1656d-114">-Name</span></span>
<span data-ttu-id="1656d-115">Site kurtarma çoğaltma ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1656d-115">Specifies the name of the Site Recovery replication policy.</span></span>

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

### <span data-ttu-id="1656d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1656d-116">-DefaultProfile</span></span>
<span data-ttu-id="1656d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1656d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1656d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1656d-118">CommonParameters</span></span>
<span data-ttu-id="1656d-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1656d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1656d-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1656d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1656d-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1656d-121">INPUTS</span></span>

## <span data-ttu-id="1656d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1656d-122">OUTPUTS</span></span>

### <span data-ttu-id="1656d-123">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRPolicy]</span><span class="sxs-lookup"><span data-stu-id="1656d-123">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRPolicy]</span></span>

## <span data-ttu-id="1656d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1656d-124">NOTES</span></span>

## <span data-ttu-id="1656d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1656d-125">RELATED LINKS</span></span>

[<span data-ttu-id="1656d-126">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="1656d-126">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="1656d-127">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="1656d-127">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
