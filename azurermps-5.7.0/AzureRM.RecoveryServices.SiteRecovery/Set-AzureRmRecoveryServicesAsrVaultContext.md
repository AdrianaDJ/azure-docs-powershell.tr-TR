---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: c85d372ccd17b23fec46655245d050b668a32dc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589719"
---
# <span data-ttu-id="aea1f-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="aea1f-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="aea1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea1f-102">SYNOPSIS</span></span>
<span data-ttu-id="aea1f-103">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kullanılacak Kurtarma Hizmetleri kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aea1f-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aea1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aea1f-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aea1f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aea1f-105">DESCRIPTION</span></span>
<span data-ttu-id="aea1f-106">**Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet 'i, diğer Işlemler Için Azure Site Recovery kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aea1f-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="aea1f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aea1f-107">EXAMPLES</span></span>

### <span data-ttu-id="aea1f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aea1f-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="aea1f-109">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kasa bağlamını belirtilen kurtarma hizmetleri kasasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aea1f-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="aea1f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aea1f-110">PARAMETERS</span></span>

### <span data-ttu-id="aea1f-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="aea1f-111">-Confirm</span></span>
<span data-ttu-id="aea1f-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aea1f-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aea1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea1f-113">-DefaultProfile</span></span>
<span data-ttu-id="aea1f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aea1f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aea1f-115">-Kasa</span><span class="sxs-lookup"><span data-stu-id="aea1f-115">-Vault</span></span>
<span data-ttu-id="aea1f-116">Kurtarma Hizmetleri Kasası 'na karşılık gelen kurtarma hizmetleri kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aea1f-116">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="aea1f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea1f-117">-WhatIf</span></span>
<span data-ttu-id="aea1f-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aea1f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aea1f-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aea1f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aea1f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea1f-120">CommonParameters</span></span>
<span data-ttu-id="aea1f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aea1f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea1f-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea1f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea1f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aea1f-123">INPUTS</span></span>

### <span data-ttu-id="aea1f-124">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="aea1f-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="aea1f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aea1f-125">OUTPUTS</span></span>

### <span data-ttu-id="aea1f-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="aea1f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="aea1f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aea1f-127">NOTES</span></span>

## <span data-ttu-id="aea1f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aea1f-128">RELATED LINKS</span></span>
