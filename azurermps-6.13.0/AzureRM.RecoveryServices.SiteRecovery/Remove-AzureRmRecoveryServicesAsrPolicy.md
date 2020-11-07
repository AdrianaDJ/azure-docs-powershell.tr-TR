---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: dcc0424cd1d6dbd823793a3dc77e813c6e182176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764318"
---
# <span data-ttu-id="aa4a1-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="aa4a1-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="aa4a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa4a1-102">SYNOPSIS</span></span>
<span data-ttu-id="aa4a1-103">Belirtilen ASR çoğaltma ilkesini kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="aa4a1-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa4a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa4a1-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa4a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa4a1-105">DESCRIPTION</span></span>
<span data-ttu-id="aa4a1-106">**Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet 'ı, kurtarma hizmetleri kasasından belirtilen çoğaltma ilkesini sildi.</span><span class="sxs-lookup"><span data-stu-id="aa4a1-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="aa4a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa4a1-107">EXAMPLES</span></span>

### <span data-ttu-id="aa4a1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="aa4a1-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="aa4a1-109">Belirtilen çoğaltma ilkesini silme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="aa4a1-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="aa4a1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa4a1-110">PARAMETERS</span></span>

### <span data-ttu-id="aa4a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa4a1-111">-DefaultProfile</span></span>
<span data-ttu-id="aa4a1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa4a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="aa4a1-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa4a1-113">-InputObject</span></span>
<span data-ttu-id="aa4a1-114">Cmdlet 'e giriş nesnesi: silinecek çoğaltma ilkesine karşılık gelen ASR çoğaltma ilkesi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aa4a1-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa4a1-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="aa4a1-115">-Confirm</span></span>
<span data-ttu-id="aa4a1-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aa4a1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa4a1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa4a1-117">-WhatIf</span></span>
<span data-ttu-id="aa4a1-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa4a1-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa4a1-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aa4a1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa4a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa4a1-120">CommonParameters</span></span>
<span data-ttu-id="aa4a1-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa4a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa4a1-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa4a1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa4a1-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa4a1-123">INPUTS</span></span>

### <span data-ttu-id="aa4a1-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="aa4a1-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="aa4a1-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa4a1-125">OUTPUTS</span></span>

### <span data-ttu-id="aa4a1-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="aa4a1-126">System.Object</span></span>

## <span data-ttu-id="aa4a1-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa4a1-127">NOTES</span></span>

## <span data-ttu-id="aa4a1-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa4a1-128">RELATED LINKS</span></span>

[<span data-ttu-id="aa4a1-129">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="aa4a1-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="aa4a1-130">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="aa4a1-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
