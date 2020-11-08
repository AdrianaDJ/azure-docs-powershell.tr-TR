---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 095759ca2753cac4f7155430a241e0554e910fd6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098121"
---
# <span data-ttu-id="63cd8-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="63cd8-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="63cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="63cd8-103">Belirtilen Azure Site Recovery yapınızı kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="63cd8-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="63cd8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63cd8-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63cd8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="63cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="63cd8-106">**Remove-AzRecoveryServicesAsrFabric** cmdlet 'ı, kurtarma hizmetleri kasasından belirtilen Azure Site Recovery yapınızı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="63cd8-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="63cd8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63cd8-107">EXAMPLES</span></span>

### <span data-ttu-id="63cd8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63cd8-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="63cd8-109">Belirtilen yapının silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="63cd8-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="63cd8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63cd8-110">PARAMETERS</span></span>

### <span data-ttu-id="63cd8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63cd8-111">-DefaultProfile</span></span>
<span data-ttu-id="63cd8-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63cd8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="63cd8-113">-Force</span><span class="sxs-lookup"><span data-stu-id="63cd8-113">-Force</span></span>
<span data-ttu-id="63cd8-114">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="63cd8-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="63cd8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63cd8-115">-InputObject</span></span>
<span data-ttu-id="63cd8-116">Cmdlet 'e giriş nesnesi: silinecek yapıya karşılık gelen ASR Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="63cd8-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: Fabric

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63cd8-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="63cd8-117">-Confirm</span></span>
<span data-ttu-id="63cd8-118">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="63cd8-118">Specify if confirmation is required.</span></span> <span data-ttu-id="63cd8-119">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="63cd8-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="63cd8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63cd8-120">-WhatIf</span></span>
<span data-ttu-id="63cd8-121">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="63cd8-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="63cd8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63cd8-122">CommonParameters</span></span>
<span data-ttu-id="63cd8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63cd8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63cd8-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="63cd8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63cd8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63cd8-125">INPUTS</span></span>

### <span data-ttu-id="63cd8-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="63cd8-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="63cd8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63cd8-127">OUTPUTS</span></span>

### <span data-ttu-id="63cd8-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="63cd8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="63cd8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63cd8-129">NOTES</span></span>

## <span data-ttu-id="63cd8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63cd8-130">RELATED LINKS</span></span>

[<span data-ttu-id="63cd8-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="63cd8-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="63cd8-132">Yeni-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="63cd8-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)