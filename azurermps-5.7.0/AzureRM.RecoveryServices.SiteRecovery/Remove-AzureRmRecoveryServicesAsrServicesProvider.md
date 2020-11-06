---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 2aa8855365ea74a00df875fb62bfec49a8c591ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589734"
---
# <span data-ttu-id="4b75a-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4b75a-101">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="4b75a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b75a-102">SYNOPSIS</span></span>
<span data-ttu-id="4b75a-103">Belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kurtarma hizmetleri kasasından siler/kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b75a-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b75a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b75a-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b75a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b75a-105">DESCRIPTION</span></span>
<span data-ttu-id="4b75a-106">**Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet 'i, kasadan belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b75a-106">The **Remove-AzureRmRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="4b75a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b75a-107">EXAMPLES</span></span>

### <span data-ttu-id="4b75a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4b75a-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="4b75a-109">Belirtilen Azure Site Recovery Hizmetleri sağlayıcısının silinmesini/kaydını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="4b75a-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4b75a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b75a-110">PARAMETERS</span></span>

### <span data-ttu-id="4b75a-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b75a-111">-Confirm</span></span>
<span data-ttu-id="4b75a-112">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4b75a-112">Specify if confirmation is required.</span></span> <span data-ttu-id="4b75a-113">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4b75a-113">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="4b75a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b75a-114">-DefaultProfile</span></span>
<span data-ttu-id="4b75a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b75a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="4b75a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4b75a-116">-Force</span></span>
<span data-ttu-id="4b75a-117">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="4b75a-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="4b75a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b75a-118">-InputObject</span></span>
<span data-ttu-id="4b75a-119">Cmdlet 'e giriş nesnesi: ASR kurtarma hizmetleri sağlayıcısının silinmesine karşılık gelen ASR kurtarma hizmetleri sağlayıcısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4b75a-119">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="4b75a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b75a-120">-WhatIf</span></span>
<span data-ttu-id="4b75a-121">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b75a-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="4b75a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b75a-122">CommonParameters</span></span>
<span data-ttu-id="4b75a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b75a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b75a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b75a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b75a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b75a-125">INPUTS</span></span>

### <span data-ttu-id="4b75a-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="4b75a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="4b75a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b75a-127">OUTPUTS</span></span>

### <span data-ttu-id="4b75a-128">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. Sıterecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4b75a-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4b75a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b75a-129">NOTES</span></span>

## <span data-ttu-id="4b75a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b75a-130">RELATED LINKS</span></span>

[<span data-ttu-id="4b75a-131">Get-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="4b75a-131">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="4b75a-132">Update-Azurermrecoveryservicesasrservices sağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="4b75a-132">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
