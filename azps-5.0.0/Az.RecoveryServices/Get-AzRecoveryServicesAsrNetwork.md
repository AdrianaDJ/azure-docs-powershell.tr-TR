---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279844"
---
# <span data-ttu-id="50167-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="50167-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="50167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50167-102">SYNOPSIS</span></span>
<span data-ttu-id="50167-103">Geçerli kasa için site kurtarma tarafından yönetilen ağlar hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="50167-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="50167-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50167-104">SYNTAX</span></span>

### <span data-ttu-id="50167-105">ByFabricObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50167-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50167-106">ByName</span><span class="sxs-lookup"><span data-stu-id="50167-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50167-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="50167-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50167-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="50167-108">DESCRIPTION</span></span>
<span data-ttu-id="50167-109">**Get-AzRecoveryServicesAsrNetwork** cmdlet 'i, geçerli Azure Site Recovery Kasası Için Azure Site Recovery ağları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="50167-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="50167-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50167-110">EXAMPLES</span></span>

### <span data-ttu-id="50167-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="50167-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="50167-112">Belirtilen yapıda tüm bilinen ağları alır.</span><span class="sxs-lookup"><span data-stu-id="50167-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="50167-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50167-113">PARAMETERS</span></span>

### <span data-ttu-id="50167-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50167-114">-DefaultProfile</span></span>
<span data-ttu-id="50167-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50167-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50167-116">-Kumaş</span><span class="sxs-lookup"><span data-stu-id="50167-116">-Fabric</span></span>
<span data-ttu-id="50167-117">ASR doku nesnesi</span><span class="sxs-lookup"><span data-stu-id="50167-117">ASR fabric object</span></span>

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

### <span data-ttu-id="50167-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="50167-118">-FriendlyName</span></span>
<span data-ttu-id="50167-119">Ağ ASR nesnesinin kolay adı.</span><span class="sxs-lookup"><span data-stu-id="50167-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="50167-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="50167-120">-Name</span></span>
<span data-ttu-id="50167-121">Ağ ASR nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="50167-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="50167-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50167-122">CommonParameters</span></span>
<span data-ttu-id="50167-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50167-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50167-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="50167-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50167-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50167-125">INPUTS</span></span>

### <span data-ttu-id="50167-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="50167-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="50167-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50167-127">OUTPUTS</span></span>

### <span data-ttu-id="50167-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="50167-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="50167-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50167-129">NOTES</span></span>

## <span data-ttu-id="50167-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50167-130">RELATED LINKS</span></span>
