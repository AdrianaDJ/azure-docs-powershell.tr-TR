---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 9a9fbf8c25eba6206b3852476b5a72a2f96be423
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278031"
---
# <span data-ttu-id="7f355-101">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7f355-101">Remove-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="7f355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f355-102">SYNOPSIS</span></span>
<span data-ttu-id="7f355-103">Belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kurtarma hizmetleri kasasından siler/kaydını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7f355-103">Deletes/unregister the specified Azure Site Recovery recovery services provider from the recovery services vault.</span></span>

## <span data-ttu-id="7f355-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f355-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f355-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f355-105">DESCRIPTION</span></span>
<span data-ttu-id="7f355-106">**Remove-AzRecoveryServicesAsrServicesProvider** cmdlet 'i, kasadan belirtilen Azure Site Recovery kurtarma hizmetleri sağlayıcısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7f355-106">The **Remove-AzRecoveryServicesAsrServicesProvider** cmdlet removes the specified Azure Site Recovery recovery services provider from the vault.</span></span>

## <span data-ttu-id="7f355-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f355-107">EXAMPLES</span></span>

### <span data-ttu-id="7f355-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f355-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="7f355-109">Belirtilen Azure Site Recovery Hizmetleri sağlayıcısının silinmesini/kaydını başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7f355-109">Starts the deletion/unregistration of the specified Azure Site Recovery services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7f355-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f355-110">PARAMETERS</span></span>

### <span data-ttu-id="7f355-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f355-111">-DefaultProfile</span></span>
<span data-ttu-id="7f355-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f355-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7f355-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7f355-113">-Force</span></span>
<span data-ttu-id="7f355-114">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="7f355-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="7f355-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f355-115">-InputObject</span></span>
<span data-ttu-id="7f355-116">Cmdlet 'e giriş nesnesi: ASR kurtarma hizmetleri sağlayıcısının silinmesine karşılık gelen ASR kurtarma hizmetleri sağlayıcısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7f355-116">The input object to the cmdlet: The ASR recovery services provider object corresponding to the ASR recovery services provider to be deleted.</span></span>

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

### <span data-ttu-id="7f355-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f355-117">-Confirm</span></span>
<span data-ttu-id="7f355-118">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="7f355-118">Specify if confirmation is required.</span></span> <span data-ttu-id="7f355-119">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7f355-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="7f355-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f355-120">-WhatIf</span></span>
<span data-ttu-id="7f355-121">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f355-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="7f355-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f355-122">CommonParameters</span></span>
<span data-ttu-id="7f355-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f355-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f355-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7f355-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f355-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f355-125">INPUTS</span></span>

### <span data-ttu-id="7f355-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7f355-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="7f355-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f355-127">OUTPUTS</span></span>

### <span data-ttu-id="7f355-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7f355-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7f355-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f355-129">NOTES</span></span>

## <span data-ttu-id="7f355-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f355-130">RELATED LINKS</span></span>

[<span data-ttu-id="7f355-131">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7f355-131">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="7f355-132">Güncelleştirme-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="7f355-132">Update-AzRecoveryServicesAsrServicesProvider</span></span>](./Update-AzRecoveryServicesAsrServicesProvider.md)
