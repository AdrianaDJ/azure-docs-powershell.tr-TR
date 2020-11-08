---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 25475bd87579b693555280f3c465f157d69c807a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098115"
---
# <span data-ttu-id="1724d-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1724d-101">Remove-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="1724d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1724d-102">SYNOPSIS</span></span>
<span data-ttu-id="1724d-103">Belirtilen Azure Site Recovery koruma kapsayıcısı eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="1724d-103">Deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="1724d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1724d-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1724d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1724d-105">DESCRIPTION</span></span>
<span data-ttu-id="1724d-106">**Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet 'ı belirtilen Azure Site Recovery koruma kapsayıcısı eşlemesini siler.</span><span class="sxs-lookup"><span data-stu-id="1724d-106">The **Remove-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet deletes the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="1724d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1724d-107">EXAMPLES</span></span>

### <span data-ttu-id="1724d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1724d-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="1724d-109">Belirtilen koruma kapsayıcısı eşlemesinin silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1724d-109">Starts the deletion of specified protection container mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1724d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1724d-110">PARAMETERS</span></span>

### <span data-ttu-id="1724d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1724d-111">-DefaultProfile</span></span>
<span data-ttu-id="1724d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1724d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1724d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1724d-113">-Force</span></span>
<span data-ttu-id="1724d-114">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="1724d-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="1724d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1724d-115">-InputObject</span></span>
<span data-ttu-id="1724d-116">Cmdlet 'e giriş nesnesi: silinecek koruma kapsayıcısına karşılık gelen ASR koruma kapsayıcısı eşleme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1724d-116">The input object to the cmdlet: the ASR protection container mapping object corresponding to the protection container to be deleted.</span></span>

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

### <span data-ttu-id="1724d-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="1724d-117">-Confirm</span></span>
<span data-ttu-id="1724d-118">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="1724d-118">Specify if confirmation is required.</span></span> <span data-ttu-id="1724d-119">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="1724d-119">Set the value of the confirm parameter to $false in order to skip confirmation</span></span>

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

### <span data-ttu-id="1724d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1724d-120">-WhatIf</span></span>
<span data-ttu-id="1724d-121">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1724d-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="1724d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1724d-122">CommonParameters</span></span>
<span data-ttu-id="1724d-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1724d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1724d-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1724d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1724d-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1724d-125">INPUTS</span></span>

### <span data-ttu-id="1724d-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1724d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="1724d-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1724d-127">OUTPUTS</span></span>

### <span data-ttu-id="1724d-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1724d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1724d-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1724d-129">NOTES</span></span>

## <span data-ttu-id="1724d-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1724d-130">RELATED LINKS</span></span>

[<span data-ttu-id="1724d-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1724d-131">Get-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./Get-AzRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="1724d-132">Yeni-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="1724d-132">New-AzRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzRecoveryServicesAsrProtectionContainerMapping.md)
