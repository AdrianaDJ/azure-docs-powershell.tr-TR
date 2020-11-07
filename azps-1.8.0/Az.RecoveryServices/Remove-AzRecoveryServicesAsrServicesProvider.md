---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 3ab29642bcf9a6ba42f211705f3d5c2c6973a061
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759630"
---
# <span data-ttu-id="e085a-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e085a-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="e085a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e085a-102">SYNOPSIS</span></span>
<span data-ttu-id="e085a-103">Belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kurtarma hizmetleri kasasından siler/kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e085a-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="e085a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e085a-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e085a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e085a-105">DESCRIPTION</span></span>
<span data-ttu-id="e085a-106">**Remove-AzRecoveryServicesAsrServicesProvider** cmdlet 'i, kasadan belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e085a-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="e085a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e085a-107">EXAMPLES</span></span>

### <span data-ttu-id="e085a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e085a-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="e085a-109">Belirtilen Azure Site Recovery Hizmetleri sağlayıcısının silinmesini/kaydını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e085a-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e085a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e085a-110">PARAMETERS</span></span>

### <span data-ttu-id="e085a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e085a-111">-DefaultProfile</span></span>
<span data-ttu-id="e085a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e085a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e085a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e085a-113">-Force</span></span>
<span data-ttu-id="e085a-114">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="e085a-114">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e085a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e085a-115">-InputObject</span></span>
<span data-ttu-id="e085a-116">Cmdlet 'e giriş nesnesi: ASR kurtarma hizmetleri sağlayıcısının silinmesine karşılık gelen ASR kurtarma hizmetleri sağlayıcısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e085a-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="e085a-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="e085a-117">-Confirm</span></span>
<span data-ttu-id="e085a-118">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="e085a-118">Specify if confirmation is required.</span></span> <span data-ttu-id="e085a-119">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e085a-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="e085a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e085a-120">-WhatIf</span></span>
<span data-ttu-id="e085a-121">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e085a-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="e085a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e085a-122">CommonParameters</span></span>
<span data-ttu-id="e085a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e085a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e085a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e085a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e085a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e085a-125">INPUTS</span></span>

### <span data-ttu-id="e085a-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e085a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="e085a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e085a-127">OUTPUTS</span></span>

### <span data-ttu-id="e085a-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e085a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e085a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e085a-129">NOTES</span></span>

## <span data-ttu-id="e085a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e085a-130">RELATED LINKS</span></span>

[<span data-ttu-id="e085a-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e085a-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="e085a-132">Güncelleştirme-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="e085a-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
