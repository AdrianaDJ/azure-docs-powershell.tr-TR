---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266484"
---
# <span data-ttu-id="227f6-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="227f6-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="227f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="227f6-102">SYNOPSIS</span></span>
<span data-ttu-id="227f6-103">Belirtilen Azure Site Recovery Ağ eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="227f6-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="227f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="227f6-104">SYNTAX</span></span>

### <span data-ttu-id="227f6-105">ByNetworkObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="227f6-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="227f6-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="227f6-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="227f6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="227f6-107">DESCRIPTION</span></span>
<span data-ttu-id="227f6-108">**Update-AzRecoveryServicesAsrNetworkMapping** cmdlet 'i, belirtilen Azure Site Recovery Ağ eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="227f6-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="227f6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="227f6-109">EXAMPLES</span></span>

### <span data-ttu-id="227f6-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="227f6-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="227f6-111">Belirtilen parametreleri kullanarak Ağ eşlemesini Güncelleştir işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="227f6-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="227f6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="227f6-112">PARAMETERS</span></span>

### <span data-ttu-id="227f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227f6-113">-DefaultProfile</span></span>
<span data-ttu-id="227f6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="227f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="227f6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="227f6-115">-InputObject</span></span>
<span data-ttu-id="227f6-116">Giriş nesnesi: güncelleştirilecek ASR ağ eşleme nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="227f6-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="227f6-117">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="227f6-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="227f6-118">Ağ eşlemesi için kurtarma Azure ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="227f6-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227f6-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="227f6-119">-RecoveryNetwork</span></span>
<span data-ttu-id="227f6-120">Ağ eşlemesi için kurtarma ağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="227f6-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227f6-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="227f6-121">-Confirm</span></span>
<span data-ttu-id="227f6-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="227f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227f6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="227f6-123">-WhatIf</span></span>
<span data-ttu-id="227f6-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="227f6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="227f6-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="227f6-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="227f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227f6-126">CommonParameters</span></span>
<span data-ttu-id="227f6-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="227f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227f6-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="227f6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227f6-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="227f6-129">INPUTS</span></span>

### <span data-ttu-id="227f6-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="227f6-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="227f6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="227f6-131">OUTPUTS</span></span>

### <span data-ttu-id="227f6-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="227f6-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="227f6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="227f6-133">NOTES</span></span>

## <span data-ttu-id="227f6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="227f6-134">RELATED LINKS</span></span>
