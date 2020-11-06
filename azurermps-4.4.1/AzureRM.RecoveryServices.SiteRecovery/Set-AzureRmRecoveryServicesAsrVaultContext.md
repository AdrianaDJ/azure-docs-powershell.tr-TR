---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: f8d55ec80c6120f2159969ae6a58a531bea50b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589151"
---
# <span data-ttu-id="34453-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="34453-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="34453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34453-102">SYNOPSIS</span></span>
<span data-ttu-id="34453-103">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kullanılacak Kurtarma Hizmetleri kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34453-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34453-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34453-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34453-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34453-105">DESCRIPTION</span></span>
<span data-ttu-id="34453-106">**Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet 'i, diğer Işlemler Için Azure Site Recovery kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34453-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="34453-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34453-107">EXAMPLES</span></span>

### <span data-ttu-id="34453-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34453-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="34453-109">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kasa bağlamını belirtilen kurtarma hizmetleri kasasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34453-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="34453-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34453-110">PARAMETERS</span></span>

### <span data-ttu-id="34453-111">-Kasa</span><span class="sxs-lookup"><span data-stu-id="34453-111">-Vault</span></span>
<span data-ttu-id="34453-112">Kurtarma Hizmetleri Kasası 'na karşılık gelen kurtarma hizmetleri kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="34453-112">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34453-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="34453-113">-Confirm</span></span>
<span data-ttu-id="34453-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34453-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34453-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34453-115">-WhatIf</span></span>
<span data-ttu-id="34453-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34453-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34453-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34453-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34453-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34453-118">CommonParameters</span></span>
<span data-ttu-id="34453-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34453-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34453-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34453-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34453-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34453-121">INPUTS</span></span>

### <span data-ttu-id="34453-122">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="34453-122">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="34453-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34453-123">OUTPUTS</span></span>

### <span data-ttu-id="34453-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="34453-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="34453-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34453-125">NOTES</span></span>

## <span data-ttu-id="34453-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34453-126">RELATED LINKS</span></span>

