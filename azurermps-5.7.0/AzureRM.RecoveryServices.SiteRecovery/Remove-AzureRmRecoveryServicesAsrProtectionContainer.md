---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 496eeed8b4ed4b41ce2c67d47fc636711cd5cb84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589738"
---
# <span data-ttu-id="eff8b-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eff8b-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="eff8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eff8b-102">SYNOPSIS</span></span>
<span data-ttu-id="eff8b-103">Belirtilen koruma kapsayıcısını yapıdan siler.</span><span class="sxs-lookup"><span data-stu-id="eff8b-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eff8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eff8b-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eff8b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eff8b-105">DESCRIPTION</span></span>
<span data-ttu-id="eff8b-106">Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet 'i belirtilen Azure Site Recovery koruma kapsayıcısını siler.</span><span class="sxs-lookup"><span data-stu-id="eff8b-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="eff8b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eff8b-107">EXAMPLES</span></span>

### <span data-ttu-id="eff8b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eff8b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="eff8b-109">Belirtilen koruma kapsayıcısının silinmesini başlatır ve Kaldır işlemini izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="eff8b-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="eff8b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eff8b-110">PARAMETERS</span></span>

### <span data-ttu-id="eff8b-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="eff8b-111">-Confirm</span></span>
<span data-ttu-id="eff8b-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eff8b-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eff8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff8b-113">-DefaultProfile</span></span>
<span data-ttu-id="eff8b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eff8b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eff8b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eff8b-115">-InputObject</span></span>
<span data-ttu-id="eff8b-116">Kaldırılacak koruma kapsayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eff8b-116">Specifies the protection container to be removed .</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eff8b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eff8b-117">-WhatIf</span></span>
<span data-ttu-id="eff8b-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eff8b-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eff8b-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eff8b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eff8b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff8b-120">CommonParameters</span></span>
<span data-ttu-id="eff8b-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eff8b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff8b-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff8b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff8b-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eff8b-123">INPUTS</span></span>

### <span data-ttu-id="eff8b-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="eff8b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="eff8b-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eff8b-125">OUTPUTS</span></span>

### <span data-ttu-id="eff8b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eff8b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eff8b-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eff8b-127">NOTES</span></span>

## <span data-ttu-id="eff8b-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eff8b-128">RELATED LINKS</span></span>
