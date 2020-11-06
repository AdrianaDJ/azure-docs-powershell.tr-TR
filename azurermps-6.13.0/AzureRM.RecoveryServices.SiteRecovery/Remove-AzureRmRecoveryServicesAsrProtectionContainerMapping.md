---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: f034f91f026538bbae475466fbd9d3afa7067145
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593921"
---
# <span data-ttu-id="44975-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="44975-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="44975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44975-102">SYNOPSIS</span></span>
<span data-ttu-id="44975-103">Belirtilen Azure Site Recovery koruma kapsayıcısı eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="44975-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44975-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44975-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44975-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="44975-105">DESCRIPTION</span></span>
<span data-ttu-id="44975-106">**Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet 'ı belirtilen Azure Site Recovery koruma kapsayıcısı eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="44975-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="44975-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44975-107">EXAMPLES</span></span>

### <span data-ttu-id="44975-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="44975-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="44975-109">Belirtilen koruma kapsayıcısı eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="44975-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="44975-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44975-110">PARAMETERS</span></span>

### <span data-ttu-id="44975-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44975-111">-DefaultProfile</span></span>
<span data-ttu-id="44975-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="44975-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="44975-113">-Force</span><span class="sxs-lookup"><span data-stu-id="44975-113">-Force</span></span>
<span data-ttu-id="44975-114">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="44975-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="44975-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44975-115">-InputObject</span></span>
<span data-ttu-id="44975-116">Cmdlet 'e giriş nesnesi: silinecek koruma kapsayıcısına karşılık gelen ASR koruma kapsayıcısı eşleme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="44975-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44975-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="44975-117">-Confirm</span></span>
<span data-ttu-id="44975-118">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="44975-118">Specify if confirmation is required.</span></span> <span data-ttu-id="44975-119">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="44975-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="44975-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44975-120">-WhatIf</span></span>
<span data-ttu-id="44975-121">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="44975-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="44975-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44975-122">CommonParameters</span></span>
<span data-ttu-id="44975-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44975-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44975-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44975-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44975-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44975-125">INPUTS</span></span>

### <span data-ttu-id="44975-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="44975-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="44975-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44975-127">OUTPUTS</span></span>

### <span data-ttu-id="44975-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="44975-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="44975-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44975-129">NOTES</span></span>

## <span data-ttu-id="44975-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44975-130">RELATED LINKS</span></span>

[<span data-ttu-id="44975-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="44975-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="44975-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="44975-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
