---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dd17eef73ab07d662a10177ffb68776aa4ec6016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593034"
---
# <span data-ttu-id="a5962-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="a5962-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="a5962-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5962-102">SYNOPSIS</span></span>
<span data-ttu-id="a5962-103">Belirtilen ASR Ağ eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5962-103">Updates the specified ASR network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5962-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5962-104">SYNTAX</span></span>

### <span data-ttu-id="a5962-105">ByNetworkObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5962-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5962-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="a5962-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5962-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5962-107">DESCRIPTION</span></span>
<span data-ttu-id="a5962-108">**Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet 'ı belirtilen Azure Site Recovery Ağ eşlemesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5962-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="a5962-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5962-109">EXAMPLES</span></span>

### <span data-ttu-id="a5962-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5962-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="a5962-111">Belirtilen parametreleri kullanarak Ağ eşlemesini Güncelleştir işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a5962-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a5962-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5962-112">PARAMETERS</span></span>

### <span data-ttu-id="a5962-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5962-113">-InputObject</span></span>
<span data-ttu-id="a5962-114">Giriş nesnesi: güncelleştirilecek ASR ağ eşleme nesnesini belirtir</span><span class="sxs-lookup"><span data-stu-id="a5962-114">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated</span></span> 

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5962-115">-Recoveryazurenetworkıd</span><span class="sxs-lookup"><span data-stu-id="a5962-115">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="a5962-116">Ağ eşlemesi için kurtarma Azure ağ KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5962-116">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5962-117">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="a5962-117">-RecoveryNetwork</span></span>
<span data-ttu-id="a5962-118">Ağ eşlemesi için kurtarma ağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5962-118">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5962-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5962-119">-Confirm</span></span>
<span data-ttu-id="a5962-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5962-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5962-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5962-121">-WhatIf</span></span>
<span data-ttu-id="a5962-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5962-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5962-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5962-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5962-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5962-124">CommonParameters</span></span>
<span data-ttu-id="a5962-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5962-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5962-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5962-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5962-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5962-127">INPUTS</span></span>

### <span data-ttu-id="a5962-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a5962-128">None</span></span>

## <span data-ttu-id="a5962-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5962-129">OUTPUTS</span></span>

### <span data-ttu-id="a5962-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a5962-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a5962-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5962-131">NOTES</span></span>

## <span data-ttu-id="a5962-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5962-132">RELATED LINKS</span></span>
