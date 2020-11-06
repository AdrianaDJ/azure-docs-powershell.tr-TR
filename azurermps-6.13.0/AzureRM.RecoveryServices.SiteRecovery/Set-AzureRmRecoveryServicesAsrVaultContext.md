---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 3d0761ff05a0cdcd775a234b4da0a50d27c2ba08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587209"
---
# <span data-ttu-id="3f7fe-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="3f7fe-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="3f7fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7fe-103">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kullanılacak Kurtarma Hizmetleri kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f7fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3f7fe-104">SYNTAX</span></span>

### <span data-ttu-id="3f7fe-105">AzureRecoveryServicesVault (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3f7fe-105">AzureRecoveryServicesVault (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f7fe-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="3f7fe-106">ByResourceId</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f7fe-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3f7fe-107">DESCRIPTION</span></span>
<span data-ttu-id="3f7fe-108">**Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet 'i, diğer Işlemler Için Azure Site Recovery kasa bağlamını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-108">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="3f7fe-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3f7fe-109">EXAMPLES</span></span>

### <span data-ttu-id="3f7fe-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3f7fe-110">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="3f7fe-111">Geçerli PowerShell oturumunda sonraki Azure Site kurtarma işlemleri için kasa bağlamını belirtilen kurtarma hizmetleri kasasına ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-111">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="3f7fe-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3f7fe-112">PARAMETERS</span></span>

### <span data-ttu-id="3f7fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f7fe-113">-DefaultProfile</span></span>
<span data-ttu-id="3f7fe-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f7fe-115">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3f7fe-115">-ResourceId</span></span>
<span data-ttu-id="3f7fe-116">Kasa bağlamı olarak ayarlanacak recoveryservices kasa kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-116">Specifies the recoveryservices vault resource id to be set as Vault context.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7fe-117">-Kasa</span><span class="sxs-lookup"><span data-stu-id="3f7fe-117">-Vault</span></span>
<span data-ttu-id="3f7fe-118">Kurtarma Hizmetleri Kasası 'na karşılık gelen kurtarma hizmetleri kasa nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-118">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f7fe-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="3f7fe-119">-Confirm</span></span>
<span data-ttu-id="3f7fe-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f7fe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f7fe-121">-WhatIf</span></span>
<span data-ttu-id="3f7fe-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f7fe-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f7fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f7fe-124">CommonParameters</span></span>
<span data-ttu-id="3f7fe-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3f7fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f7fe-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f7fe-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f7fe-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3f7fe-127">INPUTS</span></span>

### <span data-ttu-id="3f7fe-128">Microsoft. Azure. Commands. RecoveryServices. Arskasa</span><span class="sxs-lookup"><span data-stu-id="3f7fe-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="3f7fe-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3f7fe-129">OUTPUTS</span></span>

### <span data-ttu-id="3f7fe-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="3f7fe-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="3f7fe-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3f7fe-131">NOTES</span></span>

## <span data-ttu-id="3f7fe-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3f7fe-132">RELATED LINKS</span></span>
