---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 20a57bd70c9cf9b1b533e040001afee0cc5809fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933474"
---
# <span data-ttu-id="d8115-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d8115-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="d8115-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8115-102">SYNOPSIS</span></span>
<span data-ttu-id="d8115-103">Belirtilen koruma kapsayıcısını yapıdan siler.</span><span class="sxs-lookup"><span data-stu-id="d8115-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="d8115-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8115-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8115-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8115-105">DESCRIPTION</span></span>
<span data-ttu-id="d8115-106">Remove-AzRecoveryServicesAsrProtectionContainer cmdlet 'i belirtilen Azure Site Recovery koruma kapsayıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="d8115-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d8115-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8115-107">EXAMPLES</span></span>

### <span data-ttu-id="d8115-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8115-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="d8115-109">Belirtilen koruma kapsayıcısının silinmesini başlatır ve Kaldır işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8115-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="d8115-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8115-110">PARAMETERS</span></span>

### <span data-ttu-id="d8115-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8115-111">-DefaultProfile</span></span>
<span data-ttu-id="d8115-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8115-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8115-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8115-113">-InputObject</span></span>
<span data-ttu-id="d8115-114">Kaldırılacak koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8115-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="d8115-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8115-115">-Confirm</span></span>
<span data-ttu-id="d8115-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8115-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8115-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8115-117">-WhatIf</span></span>
<span data-ttu-id="d8115-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8115-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8115-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8115-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8115-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8115-120">CommonParameters</span></span>
<span data-ttu-id="d8115-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8115-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8115-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8115-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8115-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8115-123">INPUTS</span></span>

### <span data-ttu-id="d8115-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d8115-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d8115-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8115-125">OUTPUTS</span></span>

### <span data-ttu-id="d8115-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d8115-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d8115-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8115-127">NOTES</span></span>

## <span data-ttu-id="d8115-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8115-128">RELATED LINKS</span></span>
