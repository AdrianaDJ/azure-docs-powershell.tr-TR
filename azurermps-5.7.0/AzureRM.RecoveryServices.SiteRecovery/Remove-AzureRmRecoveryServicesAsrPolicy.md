---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: c8ef77367c66cc479bcbab25aba427c50a38447e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762848"
---
# <span data-ttu-id="e2dca-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e2dca-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="e2dca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2dca-102">SYNOPSIS</span></span>
<span data-ttu-id="e2dca-103">Belirtilen ASR çoğaltma ilkesini kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="e2dca-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2dca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2dca-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2dca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2dca-105">DESCRIPTION</span></span>
<span data-ttu-id="e2dca-106">**Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet 'ı, kurtarma hizmetleri kasasından belirtilen çoğaltma ilkesini sildi.</span><span class="sxs-lookup"><span data-stu-id="e2dca-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="e2dca-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2dca-107">EXAMPLES</span></span>

### <span data-ttu-id="e2dca-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2dca-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="e2dca-109">Belirtilen çoğaltma ilkesini silme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e2dca-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e2dca-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2dca-110">PARAMETERS</span></span>

### <span data-ttu-id="e2dca-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="e2dca-111">-Confirm</span></span>
<span data-ttu-id="e2dca-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e2dca-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2dca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2dca-113">-DefaultProfile</span></span>
<span data-ttu-id="e2dca-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2dca-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="e2dca-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2dca-115">-InputObject</span></span>
<span data-ttu-id="e2dca-116">Cmdlet 'e giriş nesnesi: silinecek çoğaltma ilkesine karşılık gelen ASR çoğaltma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e2dca-116">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2dca-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2dca-117">-WhatIf</span></span>
<span data-ttu-id="e2dca-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2dca-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2dca-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e2dca-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2dca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2dca-120">CommonParameters</span></span>
<span data-ttu-id="e2dca-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2dca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2dca-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2dca-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2dca-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2dca-123">INPUTS</span></span>

### <span data-ttu-id="e2dca-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="e2dca-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="e2dca-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2dca-125">OUTPUTS</span></span>

### <span data-ttu-id="e2dca-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="e2dca-126">System.Object</span></span>

## <span data-ttu-id="e2dca-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2dca-127">NOTES</span></span>

## <span data-ttu-id="e2dca-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2dca-128">RELATED LINKS</span></span>

[<span data-ttu-id="e2dca-129">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e2dca-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="e2dca-130">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="e2dca-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
