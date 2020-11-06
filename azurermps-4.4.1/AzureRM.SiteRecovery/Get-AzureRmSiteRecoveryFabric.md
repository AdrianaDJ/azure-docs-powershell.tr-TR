---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589082"
---
# <span data-ttu-id="af842-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="af842-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="af842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af842-102">SYNOPSIS</span></span>
<span data-ttu-id="af842-103">Bir Azure Site kurtarma yapısı özelliklerini edinin.</span><span class="sxs-lookup"><span data-stu-id="af842-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af842-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af842-104">SYNTAX</span></span>

### <span data-ttu-id="af842-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af842-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af842-106">ByName</span><span class="sxs-lookup"><span data-stu-id="af842-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af842-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="af842-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af842-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="af842-108">DESCRIPTION</span></span>
<span data-ttu-id="af842-109">**Get-AzureRmSiteRecoveryFabric** cmdlet 'ı, kurtarma hizmeti kasasındaki belirli bir Azure Site Recovery yapısı veya tüm Azure Site kurtarma yapılarını alır.</span><span class="sxs-lookup"><span data-stu-id="af842-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="af842-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af842-110">EXAMPLES</span></span>

## <span data-ttu-id="af842-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af842-111">PARAMETERS</span></span>

### <span data-ttu-id="af842-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="af842-112">-FriendlyName</span></span>
<span data-ttu-id="af842-113">Azure Site Recovery yapısı kolay adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af842-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="af842-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="af842-114">-Name</span></span>
<span data-ttu-id="af842-115">Azure Site Recovery yapısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af842-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="af842-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af842-116">-DefaultProfile</span></span>
<span data-ttu-id="af842-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af842-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af842-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af842-118">CommonParameters</span></span>
<span data-ttu-id="af842-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af842-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af842-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af842-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af842-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af842-121">INPUTS</span></span>

## <span data-ttu-id="af842-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af842-122">OUTPUTS</span></span>

### <span data-ttu-id="af842-123">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRFabric, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="af842-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="af842-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af842-124">NOTES</span></span>

## <span data-ttu-id="af842-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af842-125">RELATED LINKS</span></span>

[<span data-ttu-id="af842-126">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="af842-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="af842-127">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="af842-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
