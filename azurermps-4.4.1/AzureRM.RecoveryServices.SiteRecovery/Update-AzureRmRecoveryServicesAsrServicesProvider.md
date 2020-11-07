---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763644"
---
# <span data-ttu-id="5ca85-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5ca85-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="5ca85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca85-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca85-103">(Sunucuyu Yenile) Azure Site Recovery Hizmetleri sağlayıcısından alınan bilgileri yeniler.</span><span class="sxs-lookup"><span data-stu-id="5ca85-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ca85-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ca85-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ca85-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ca85-105">DESCRIPTION</span></span>
<span data-ttu-id="5ca85-106">**Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet 'ı Azure Site Recovery Hizmetleri sağlayıcısından alınan bilgileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5ca85-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="5ca85-107">Bu cmdlet 'i kullanarak, kurtarma hizmetleri sağlayıcısından alınan bilgilerin yenilenmesini tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ca85-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="5ca85-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ca85-108">EXAMPLES</span></span>

### <span data-ttu-id="5ca85-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5ca85-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="5ca85-110">Belirtilen ASR Hizmetleri sağlayıcısından bilgileri yenileme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5ca85-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span> 

## <span data-ttu-id="5ca85-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ca85-111">PARAMETERS</span></span>

### <span data-ttu-id="5ca85-112">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ca85-112">-InputObject</span></span>
<span data-ttu-id="5ca85-113">Giriş nesnesi: bilgilerin güncelleştirileceği sunucuyu tanımlayan ASR hizmetleri sağlayıcısına karşılık gelen ASR hizmetleri sağlayıcısı nesnesini belirtir (yenilenir.)</span><span class="sxs-lookup"><span data-stu-id="5ca85-113">Input Object: Specifies the ASR services provider object corresponding to the ASR services provider that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="5ca85-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ca85-114">-Confirm</span></span>
<span data-ttu-id="5ca85-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ca85-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ca85-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca85-116">-WhatIf</span></span>
<span data-ttu-id="5ca85-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ca85-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ca85-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ca85-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ca85-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca85-119">CommonParameters</span></span>
<span data-ttu-id="5ca85-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ca85-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca85-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ca85-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca85-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ca85-122">INPUTS</span></span>

### <span data-ttu-id="5ca85-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="5ca85-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="5ca85-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ca85-124">OUTPUTS</span></span>

### <span data-ttu-id="5ca85-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="5ca85-125">System.Object</span></span>

## <span data-ttu-id="5ca85-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ca85-126">NOTES</span></span>

## <span data-ttu-id="5ca85-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ca85-127">RELATED LINKS</span></span>

[<span data-ttu-id="5ca85-128">Get-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="5ca85-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="5ca85-129">Remove-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="5ca85-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
