---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9d7cfb1b5bdba7d82d42347dad697c5efa764919
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765084"
---
# <span data-ttu-id="33d5d-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="33d5d-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="33d5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="33d5d-103">(Sunucuyu Yenile) Azure Site Recovery Hizmetleri sağlayıcısından alınan bilgileri yeniler.</span><span class="sxs-lookup"><span data-stu-id="33d5d-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33d5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33d5d-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d5d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="33d5d-105">DESCRIPTION</span></span>
<span data-ttu-id="33d5d-106">**Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet 'ı Azure Site Recovery Hizmetleri sağlayıcısından alınan bilgileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="33d5d-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="33d5d-107">Bu cmdlet 'i kullanarak, kurtarma hizmetleri sağlayıcısından alınan bilgilerin yenilenmesini tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="33d5d-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="33d5d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33d5d-108">EXAMPLES</span></span>

### <span data-ttu-id="33d5d-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="33d5d-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="33d5d-110">Belirtilen ASR Hizmetleri sağlayıcısından bilgileri yenileme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="33d5d-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="33d5d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33d5d-111">PARAMETERS</span></span>

### <span data-ttu-id="33d5d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d5d-112">-DefaultProfile</span></span>
<span data-ttu-id="33d5d-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33d5d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="33d5d-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33d5d-114">-InputObject</span></span>
<span data-ttu-id="33d5d-115">Bilgilerin güncelleştirileceği sunucuyu tanımlayan ASR hizmetleri sağlayıcısı nesnesini belirtir (yenilenir.)</span><span class="sxs-lookup"><span data-stu-id="33d5d-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33d5d-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="33d5d-116">-Confirm</span></span>
<span data-ttu-id="33d5d-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="33d5d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d5d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d5d-118">-WhatIf</span></span>
<span data-ttu-id="33d5d-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="33d5d-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33d5d-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="33d5d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33d5d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d5d-121">CommonParameters</span></span>
<span data-ttu-id="33d5d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33d5d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d5d-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d5d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d5d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33d5d-124">INPUTS</span></span>

### <span data-ttu-id="33d5d-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="33d5d-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="33d5d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33d5d-126">OUTPUTS</span></span>

### <span data-ttu-id="33d5d-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="33d5d-127">System.Object</span></span>

## <span data-ttu-id="33d5d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33d5d-128">NOTES</span></span>

## <span data-ttu-id="33d5d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33d5d-129">RELATED LINKS</span></span>

[<span data-ttu-id="33d5d-130">Get-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="33d5d-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="33d5d-131">Remove-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="33d5d-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
