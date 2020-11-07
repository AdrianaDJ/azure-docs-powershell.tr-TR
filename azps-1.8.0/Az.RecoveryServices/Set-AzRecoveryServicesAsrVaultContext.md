---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 846c27dc521e13cb2814a4f9e004325da4263bf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759608"
---
# <span data-ttu-id="515f3-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="515f3-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="515f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="515f3-102">SYNOPSIS</span></span>
<span data-ttu-id="515f3-103">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kullanılacak Kurtarma Hizmetleri kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="515f3-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="515f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="515f3-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="515f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="515f3-105">DESCRIPTION</span></span>
<span data-ttu-id="515f3-106">**Set-AzRecoveryServicesAsrVaultContext** cmdlet 'i, diğer Işlemler Için Azure Site Recovery kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="515f3-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="515f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="515f3-107">EXAMPLES</span></span>

### <span data-ttu-id="515f3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="515f3-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="515f3-109">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kasa bağlamını belirtilen kurtarma hizmetleri kasasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="515f3-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="515f3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="515f3-110">PARAMETERS</span></span>

### <span data-ttu-id="515f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="515f3-111">-DefaultProfile</span></span>
<span data-ttu-id="515f3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="515f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="515f3-113">-Kasa</span><span class="sxs-lookup"><span data-stu-id="515f3-113">-Vault</span></span>
<span data-ttu-id="515f3-114">Kurtarma Hizmetleri Kasası 'na karşılık gelen kurtarma hizmetleri kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="515f3-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="515f3-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="515f3-115">-Confirm</span></span>
<span data-ttu-id="515f3-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="515f3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="515f3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="515f3-117">-WhatIf</span></span>
<span data-ttu-id="515f3-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="515f3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="515f3-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="515f3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="515f3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="515f3-120">CommonParameters</span></span>
<span data-ttu-id="515f3-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="515f3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="515f3-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="515f3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="515f3-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="515f3-123">INPUTS</span></span>

### <span data-ttu-id="515f3-124">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="515f3-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="515f3-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="515f3-125">OUTPUTS</span></span>

### <span data-ttu-id="515f3-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="515f3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="515f3-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="515f3-127">NOTES</span></span>

## <span data-ttu-id="515f3-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="515f3-128">RELATED LINKS</span></span>
