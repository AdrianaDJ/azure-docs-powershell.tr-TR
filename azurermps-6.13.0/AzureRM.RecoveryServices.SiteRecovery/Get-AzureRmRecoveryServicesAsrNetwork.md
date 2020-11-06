---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 4eac63104f9e75643119c371d2a4d0e882945966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590079"
---
# <span data-ttu-id="905e8-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="905e8-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="905e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="905e8-102">SYNOPSIS</span></span>
<span data-ttu-id="905e8-103">Geçerli kasa için site kurtarma tarafından yönetilen ağlar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="905e8-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="905e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="905e8-104">SYNTAX</span></span>

### <span data-ttu-id="905e8-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="905e8-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="905e8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="905e8-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="905e8-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="905e8-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="905e8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="905e8-108">DESCRIPTION</span></span>
<span data-ttu-id="905e8-109">**Get-AzureRmRecoveryServicesAsrNetwork** cmdlet 'i, geçerli Azure Site Recovery Kasası Için Azure Site Recovery ağları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="905e8-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="905e8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="905e8-110">EXAMPLES</span></span>

### <span data-ttu-id="905e8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="905e8-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="905e8-112">Belirtilen yapıda tüm bilinen ağları alır.</span><span class="sxs-lookup"><span data-stu-id="905e8-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="905e8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="905e8-113">PARAMETERS</span></span>

### <span data-ttu-id="905e8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905e8-114">-DefaultProfile</span></span>
<span data-ttu-id="905e8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="905e8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="905e8-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="905e8-116">-Fabric</span></span>
<span data-ttu-id="905e8-117">ASR doku nesnesi</span><span class="sxs-lookup"><span data-stu-id="905e8-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="905e8-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="905e8-118">-FriendlyName</span></span>
<span data-ttu-id="905e8-119">Ağ ASR nesnesinin kolay adı.</span><span class="sxs-lookup"><span data-stu-id="905e8-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="905e8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="905e8-120">-Name</span></span>
<span data-ttu-id="905e8-121">Ağ ASR nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="905e8-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="905e8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905e8-122">CommonParameters</span></span>
<span data-ttu-id="905e8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="905e8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905e8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="905e8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905e8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="905e8-125">INPUTS</span></span>

### <span data-ttu-id="905e8-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="905e8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="905e8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="905e8-127">OUTPUTS</span></span>

### <span data-ttu-id="905e8-128">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRNetwork, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="905e8-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="905e8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="905e8-129">NOTES</span></span>

## <span data-ttu-id="905e8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="905e8-130">RELATED LINKS</span></span>
