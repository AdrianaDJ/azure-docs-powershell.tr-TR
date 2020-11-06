---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 34977acc0889a3fa557af7dfc9f02d6937e22fde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588839"
---
# <span data-ttu-id="b896c-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="b896c-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="b896c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b896c-102">SYNOPSIS</span></span>
<span data-ttu-id="b896c-103">Geçerli kasa için site kurtarma tarafından yönetilen ağlar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b896c-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b896c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b896c-104">SYNTAX</span></span>

### <span data-ttu-id="b896c-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b896c-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b896c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b896c-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b896c-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b896c-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b896c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b896c-108">DESCRIPTION</span></span>
<span data-ttu-id="b896c-109">**Get-AzureRmRecoveryServicesAsrNetwork** cmdlet 'i, geçerli Azure Site Recovery Kasası Için Azure Site Recovery ağları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="b896c-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b896c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b896c-110">EXAMPLES</span></span>

### <span data-ttu-id="b896c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b896c-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="b896c-112">Belirtilen yapıda tüm bilinen ağları alır.</span><span class="sxs-lookup"><span data-stu-id="b896c-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="b896c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b896c-113">PARAMETERS</span></span>

### <span data-ttu-id="b896c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b896c-114">-DefaultProfile</span></span>
<span data-ttu-id="b896c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b896c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="b896c-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="b896c-116">-Fabric</span></span>
<span data-ttu-id="b896c-117">ASR doku nesnesi</span><span class="sxs-lookup"><span data-stu-id="b896c-117">ASR fabric object</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b896c-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b896c-118">-FriendlyName</span></span>
<span data-ttu-id="b896c-119">Ağ ASR nesnesinin kolay adı.</span><span class="sxs-lookup"><span data-stu-id="b896c-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="b896c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b896c-120">-Name</span></span>
<span data-ttu-id="b896c-121">Ağ ASR nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="b896c-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="b896c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b896c-122">CommonParameters</span></span>
<span data-ttu-id="b896c-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b896c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b896c-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b896c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b896c-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b896c-125">INPUTS</span></span>

### <span data-ttu-id="b896c-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b896c-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b896c-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b896c-127">OUTPUTS</span></span>

### <span data-ttu-id="b896c-128">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRNetwork, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b896c-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b896c-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b896c-129">NOTES</span></span>

## <span data-ttu-id="b896c-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b896c-130">RELATED LINKS</span></span>
