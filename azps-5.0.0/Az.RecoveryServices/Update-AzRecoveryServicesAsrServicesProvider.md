---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: ff280c11ff06d710eb8c74f88b839854506c6cd0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279170"
---
# <span data-ttu-id="92a90-101">Update-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="92a90-101">Update-AzRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="92a90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92a90-102">SYNOPSIS</span></span>
<span data-ttu-id="92a90-103">(Sunucuyu Yenile) Azure Site Recovery Hizmetleri sağlayıcısından alınan bilgileri yeniler.</span><span class="sxs-lookup"><span data-stu-id="92a90-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

## <span data-ttu-id="92a90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92a90-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92a90-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="92a90-105">DESCRIPTION</span></span>
<span data-ttu-id="92a90-106">**Update-AzRecoveryServicesAsrServicesProvider** cmdlet 'ı Azure Site Recovery Hizmetleri sağlayıcısından alınan bilgileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="92a90-106">The **Update-AzRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="92a90-107">Bu cmdlet 'i kullanarak, kurtarma hizmetleri sağlayıcısından alınan bilgilerin yenilenmesini tetikleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92a90-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="92a90-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92a90-108">EXAMPLES</span></span>

### <span data-ttu-id="92a90-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="92a90-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="92a90-110">Belirtilen ASR Hizmetleri sağlayıcısından bilgileri yenileme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="92a90-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="92a90-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92a90-111">PARAMETERS</span></span>

### <span data-ttu-id="92a90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a90-112">-DefaultProfile</span></span>
<span data-ttu-id="92a90-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92a90-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="92a90-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92a90-114">-InputObject</span></span>
<span data-ttu-id="92a90-115">Bilgilerin güncelleştirileceği sunucuyu tanımlayan ASR hizmetleri sağlayıcısı nesnesini belirtir (yenilenir.)</span><span class="sxs-lookup"><span data-stu-id="92a90-115">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="92a90-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="92a90-116">-Confirm</span></span>
<span data-ttu-id="92a90-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92a90-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a90-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a90-118">-WhatIf</span></span>
<span data-ttu-id="92a90-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92a90-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92a90-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92a90-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a90-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a90-121">CommonParameters</span></span>
<span data-ttu-id="92a90-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92a90-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a90-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="92a90-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a90-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92a90-124">INPUTS</span></span>

### <span data-ttu-id="92a90-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="92a90-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="92a90-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92a90-126">OUTPUTS</span></span>

### <span data-ttu-id="92a90-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="92a90-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="92a90-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92a90-128">NOTES</span></span>

## <span data-ttu-id="92a90-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92a90-129">RELATED LINKS</span></span>

[<span data-ttu-id="92a90-130">Get-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="92a90-130">Get-AzRecoveryServicesAsrServicesProvider</span></span>](./Get-AzRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="92a90-131">Remove-AzRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="92a90-131">Remove-AzRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzRecoveryServicesAsrServicesProvider.md)
