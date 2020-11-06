---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 13c2f20f6d8ef7823244c62cfbe97e4b3a25eb73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589154"
---
# <span data-ttu-id="0c0c1-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0c0c1-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="0c0c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c0c1-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0c1-103">Belirtilen ASR Ağ eşlemesini kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="0c0c1-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c0c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c0c1-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c0c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c0c1-105">DESCRIPTION</span></span>
<span data-ttu-id="0c0c1-106">**Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet 'ı belirtilen ASR Ağ eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="0c0c1-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="0c0c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c0c1-107">EXAMPLES</span></span>

### <span data-ttu-id="0c0c1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c0c1-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="0c0c1-109">Belirtilen ASR ağ eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c0c1-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0c0c1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c0c1-110">PARAMETERS</span></span>

### <span data-ttu-id="0c0c1-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c0c1-111">-InputObject</span></span>
<span data-ttu-id="0c0c1-112">Cmdlet 'e giriş nesnesi: ASR ağ eşlemesine yönelik ASR ağ eşleme nesnesi silinecek.</span><span class="sxs-lookup"><span data-stu-id="0c0c1-112">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="0c0c1-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c0c1-113">-Confirm</span></span>
<span data-ttu-id="0c0c1-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c0c1-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c0c1-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c0c1-115">-WhatIf</span></span>
<span data-ttu-id="0c0c1-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c0c1-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c0c1-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c0c1-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c0c1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0c1-118">CommonParameters</span></span>
<span data-ttu-id="0c0c1-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c0c1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0c1-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c0c1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0c1-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c0c1-121">INPUTS</span></span>

### <span data-ttu-id="0c0c1-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0c0c1-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="0c0c1-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c0c1-123">OUTPUTS</span></span>

### <span data-ttu-id="0c0c1-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0c0c1-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0c0c1-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c0c1-125">NOTES</span></span>

## <span data-ttu-id="0c0c1-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c0c1-126">RELATED LINKS</span></span>

[<span data-ttu-id="0c0c1-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0c0c1-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="0c0c1-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0c0c1-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
