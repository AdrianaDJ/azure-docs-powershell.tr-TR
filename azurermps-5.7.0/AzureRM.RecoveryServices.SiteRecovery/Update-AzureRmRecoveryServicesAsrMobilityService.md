---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: de9e07da334e252db4af87819d2719b5251b576c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573345"
---
# <span data-ttu-id="e0fb1-101">Update-AzureRmRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="e0fb1-101">Update-AzureRmRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="e0fb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="e0fb1-103">Korumalı makinelere Mobility Service Agent güncelleştirmelerini itme.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-103">Push mobility service agent updates to protected machines.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0fb1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0fb1-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0fb1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0fb1-105">DESCRIPTION</span></span>
<span data-ttu-id="e0fb1-106">**Update-Azurermrecoveryservicesasrsoityservice** cmdlet 'i korumalı makinelere Mobility hizmet Aracısı güncelleştirmelerini itme girişiminde bulunur (güncelleştirme varsa).</span><span class="sxs-lookup"><span data-stu-id="e0fb1-106">The **Update-AzureRmRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="e0fb1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0fb1-107">EXAMPLES</span></span>

### <span data-ttu-id="e0fb1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e0fb1-108">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="e0fb1-109">Güncelleştirme çoğaltması korumalı öğenin Sloglık hizmet aracısının izlenmesi işi.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-109">Job to track Update Replication Protected Item's Moblility Service Agent.</span></span>

## <span data-ttu-id="e0fb1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0fb1-110">PARAMETERS</span></span>

### <span data-ttu-id="e0fb1-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="e0fb1-111">-Account</span></span>
<span data-ttu-id="e0fb1-112">Güncelleştirmeyi göndermek için kullanılacak farklı hesapla hesap KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="e0fb1-113">Makine güncellenecek olan ASR dokuda farklı bir Run as hesabı listesinden bir tane olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0fb1-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0fb1-114">-Confirm</span></span>
<span data-ttu-id="e0fb1-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0fb1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0fb1-116">-DefaultProfile</span></span>
<span data-ttu-id="e0fb1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0fb1-118">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="e0fb1-118">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e0fb1-119">Güncelleştirilecek Azure Site Recovery çoğaltma korumalı öğesi.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-119">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0fb1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0fb1-120">-WhatIf</span></span>
<span data-ttu-id="e0fb1-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0fb1-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0fb1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0fb1-123">CommonParameters</span></span>
<span data-ttu-id="e0fb1-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0fb1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0fb1-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0fb1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0fb1-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0fb1-126">INPUTS</span></span>

### <span data-ttu-id="e0fb1-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="e0fb1-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="e0fb1-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0fb1-128">OUTPUTS</span></span>

### <span data-ttu-id="e0fb1-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e0fb1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e0fb1-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0fb1-130">NOTES</span></span>

## <span data-ttu-id="e0fb1-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0fb1-131">RELATED LINKS</span></span>
