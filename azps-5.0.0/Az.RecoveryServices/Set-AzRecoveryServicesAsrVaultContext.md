---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275703"
---
# <span data-ttu-id="7e051-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="7e051-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="7e051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e051-102">SYNOPSIS</span></span>
<span data-ttu-id="7e051-103">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kullanılacak Kurtarma Hizmetleri kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7e051-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="7e051-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e051-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e051-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e051-105">DESCRIPTION</span></span>
<span data-ttu-id="7e051-106">**Set-AzRecoveryServicesAsrVaultContext** cmdlet 'i, diğer Işlemler Için Azure Site Recovery kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7e051-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="7e051-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e051-107">EXAMPLES</span></span>

### <span data-ttu-id="7e051-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e051-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="7e051-109">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kasa bağlamını belirtilen kurtarma hizmetleri kasasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7e051-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="7e051-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e051-110">PARAMETERS</span></span>

### <span data-ttu-id="7e051-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e051-111">-DefaultProfile</span></span>
<span data-ttu-id="7e051-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e051-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e051-113">-Kasa</span><span class="sxs-lookup"><span data-stu-id="7e051-113">-Vault</span></span>
<span data-ttu-id="7e051-114">Kurtarma Hizmetleri Kasası 'na karşılık gelen kurtarma hizmetleri kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7e051-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e051-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e051-115">-Confirm</span></span>
<span data-ttu-id="7e051-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e051-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e051-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e051-117">-WhatIf</span></span>
<span data-ttu-id="7e051-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e051-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e051-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e051-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e051-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e051-120">CommonParameters</span></span>
<span data-ttu-id="7e051-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e051-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e051-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e051-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e051-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e051-123">INPUTS</span></span>

### <span data-ttu-id="7e051-124">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="7e051-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7e051-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e051-125">OUTPUTS</span></span>

### <span data-ttu-id="7e051-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="7e051-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="7e051-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e051-127">NOTES</span></span>

## <span data-ttu-id="7e051-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e051-128">RELATED LINKS</span></span>
