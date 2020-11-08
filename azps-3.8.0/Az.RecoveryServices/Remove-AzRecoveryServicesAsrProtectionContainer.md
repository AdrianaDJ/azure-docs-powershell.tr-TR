---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098118"
---
# <span data-ttu-id="3c06d-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3c06d-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="3c06d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c06d-102">SYNOPSIS</span></span>
<span data-ttu-id="3c06d-103">Belirtilen koruma kapsayıcısını yapıdan siler.</span><span class="sxs-lookup"><span data-stu-id="3c06d-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="3c06d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c06d-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c06d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c06d-105">DESCRIPTION</span></span>
<span data-ttu-id="3c06d-106">Remove-AzRecoveryServicesAsrProtectionContainer cmdlet 'i belirtilen Azure Site Recovery koruma kapsayıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="3c06d-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="3c06d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c06d-107">EXAMPLES</span></span>

### <span data-ttu-id="3c06d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c06d-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="3c06d-109">Belirtilen koruma kapsayıcısının silinmesini başlatır ve Kaldır işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3c06d-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="3c06d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c06d-110">PARAMETERS</span></span>

### <span data-ttu-id="3c06d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c06d-111">-DefaultProfile</span></span>
<span data-ttu-id="3c06d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c06d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c06d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c06d-113">-InputObject</span></span>
<span data-ttu-id="3c06d-114">Kaldırılacak koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3c06d-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c06d-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c06d-115">-Confirm</span></span>
<span data-ttu-id="3c06d-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3c06d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c06d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c06d-117">-WhatIf</span></span>
<span data-ttu-id="3c06d-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c06d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c06d-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c06d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c06d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c06d-120">CommonParameters</span></span>
<span data-ttu-id="3c06d-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c06d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c06d-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3c06d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c06d-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c06d-123">INPUTS</span></span>

### <span data-ttu-id="3c06d-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="3c06d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="3c06d-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c06d-125">OUTPUTS</span></span>

### <span data-ttu-id="3c06d-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="3c06d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3c06d-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c06d-127">NOTES</span></span>

## <span data-ttu-id="3c06d-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c06d-128">RELATED LINKS</span></span>
