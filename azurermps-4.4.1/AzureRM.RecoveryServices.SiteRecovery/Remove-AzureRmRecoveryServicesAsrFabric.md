---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 3f380110359668af5c1b506e1736d3ecc9f39b3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589157"
---
# <span data-ttu-id="945d7-101">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="945d7-101">Remove-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="945d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="945d7-102">SYNOPSIS</span></span>
<span data-ttu-id="945d7-103">Belirtilen Azure Site Recovery yapınızı kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="945d7-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="945d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="945d7-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="945d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="945d7-105">DESCRIPTION</span></span>
<span data-ttu-id="945d7-106">**Remove-AzureRmRecoveryServicesAsrFabric** cmdlet 'ı, kurtarma hizmetleri kasasından belirtilen Azure Site Recovery yapınızı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="945d7-106">The **Remove-AzureRmRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="945d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="945d7-107">EXAMPLES</span></span>

### <span data-ttu-id="945d7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="945d7-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="945d7-109">Belirtilen yapının silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="945d7-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="945d7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="945d7-110">PARAMETERS</span></span>

### <span data-ttu-id="945d7-111">-Force</span><span class="sxs-lookup"><span data-stu-id="945d7-111">-Force</span></span>
<span data-ttu-id="945d7-112">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="945d7-112">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="945d7-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="945d7-113">-InputObject</span></span>
<span data-ttu-id="945d7-114">Cmdlet 'e giriş nesnesi: silinecek yapıya karşılık gelen ASR Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="945d7-114">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="945d7-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="945d7-115">-Confirm</span></span>
<span data-ttu-id="945d7-116">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="945d7-116">Specify if confirmation is required.</span></span> <span data-ttu-id="945d7-117">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="945d7-117">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="945d7-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="945d7-118">-WhatIf</span></span>
<span data-ttu-id="945d7-119">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="945d7-119">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="945d7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="945d7-120">CommonParameters</span></span>
<span data-ttu-id="945d7-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="945d7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="945d7-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="945d7-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="945d7-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="945d7-123">INPUTS</span></span>

### <span data-ttu-id="945d7-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="945d7-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="945d7-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="945d7-125">OUTPUTS</span></span>

### <span data-ttu-id="945d7-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="945d7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="945d7-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="945d7-127">NOTES</span></span>

## <span data-ttu-id="945d7-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="945d7-128">RELATED LINKS</span></span>

[<span data-ttu-id="945d7-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="945d7-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="945d7-130">Yeni-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="945d7-130">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)
