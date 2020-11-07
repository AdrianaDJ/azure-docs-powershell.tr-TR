---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 7a2508669c0beba7fc9edd92ac645ce149633e05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762846"
---
# <span data-ttu-id="b5617-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b5617-101">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="b5617-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5617-102">SYNOPSIS</span></span>
<span data-ttu-id="b5617-103">Belirtilen Azure Site Recovery koruma kapsayıcısı eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="b5617-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5617-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5617-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5617-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5617-105">DESCRIPTION</span></span>
<span data-ttu-id="b5617-106">**Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet 'ı belirtilen Azure Site Recovery koruma kapsayıcısı eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="b5617-106">The **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="b5617-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5617-107">EXAMPLES</span></span>

### <span data-ttu-id="b5617-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b5617-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="b5617-109">Belirtilen koruma kapsayıcısı eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b5617-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b5617-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5617-110">PARAMETERS</span></span>

### <span data-ttu-id="b5617-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5617-111">-Confirm</span></span>
<span data-ttu-id="b5617-112">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="b5617-112">Specify if confirmation is required.</span></span> <span data-ttu-id="b5617-113">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="b5617-113">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="b5617-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5617-114">-DefaultProfile</span></span>
<span data-ttu-id="b5617-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5617-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="b5617-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b5617-116">-Force</span></span>
<span data-ttu-id="b5617-117">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="b5617-117">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="b5617-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5617-118">-InputObject</span></span>
<span data-ttu-id="b5617-119">Cmdlet 'e giriş nesnesi: silinecek koruma kapsayıcısına karşılık gelen ASR koruma kapsayıcısı eşleme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="b5617-119">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5617-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5617-120">-WhatIf</span></span>
<span data-ttu-id="b5617-121">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5617-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="b5617-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5617-122">CommonParameters</span></span>
<span data-ttu-id="b5617-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5617-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5617-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5617-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5617-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5617-125">INPUTS</span></span>

### <span data-ttu-id="b5617-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b5617-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="b5617-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5617-127">OUTPUTS</span></span>

### <span data-ttu-id="b5617-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b5617-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b5617-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5617-129">NOTES</span></span>

## <span data-ttu-id="b5617-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5617-130">RELATED LINKS</span></span>

[<span data-ttu-id="b5617-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b5617-131">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="b5617-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b5617-132">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
