---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 5220271538903206876dd8d5c476824e1ac10874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594587"
---
# <span data-ttu-id="20207-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="20207-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="20207-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20207-102">SYNOPSIS</span></span>
<span data-ttu-id="20207-103">Belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kurtarma hizmetleri kasasından siler/kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20207-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20207-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20207-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20207-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20207-105">DESCRIPTION</span></span>
<span data-ttu-id="20207-106">**Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet 'i, kasadan belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20207-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="20207-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20207-107">EXAMPLES</span></span>

### <span data-ttu-id="20207-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="20207-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="20207-109">Belirtilen Azure Site Recovery Hizmetleri sağlayıcısının silinmesini/kaydını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="20207-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="20207-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20207-110">PARAMETERS</span></span>

### <span data-ttu-id="20207-111">-Force</span><span class="sxs-lookup"><span data-stu-id="20207-111">-Force</span></span>
<span data-ttu-id="20207-112">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="20207-112">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20207-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20207-113">-InputObject</span></span>
<span data-ttu-id="20207-114">Cmdlet 'e giriş nesnesi: ASR kurtarma hizmetleri sağlayıcısının silinmesine karşılık gelen ASR kurtarma hizmetleri sağlayıcısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="20207-114">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20207-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="20207-115">-Confirm</span></span>
<span data-ttu-id="20207-116">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="20207-116">Specify if confirmation is required.</span></span> <span data-ttu-id="20207-117">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="20207-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="20207-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20207-118">-WhatIf</span></span>
<span data-ttu-id="20207-119">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="20207-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="20207-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20207-120">CommonParameters</span></span>
<span data-ttu-id="20207-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20207-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20207-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20207-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20207-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20207-123">INPUTS</span></span>

### <span data-ttu-id="20207-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="20207-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="20207-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20207-125">OUTPUTS</span></span>

### <span data-ttu-id="20207-126">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="20207-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="20207-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20207-127">NOTES</span></span>

## <span data-ttu-id="20207-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20207-128">RELATED LINKS</span></span>

[<span data-ttu-id="20207-129">Get-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="20207-129">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="20207-130">Update-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="20207-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
