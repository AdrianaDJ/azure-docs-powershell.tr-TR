---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 9a67729b384703ccc102b14d521d4422825bdb6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759644"
---
# <span data-ttu-id="adadf-101">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="adadf-101">Remove-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="adadf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adadf-102">SYNOPSIS</span></span>
<span data-ttu-id="adadf-103">Belirtilen Azure Site Recovery yapınızı kurtarma hizmetleri kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="adadf-103">Deletes the specified Azure Site Recovery Fabric from the Recovery Services vault.</span></span>

## <span data-ttu-id="adadf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="adadf-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrFabric -InputObject <ASRFabric> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adadf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="adadf-105">DESCRIPTION</span></span>
<span data-ttu-id="adadf-106">**Remove-AzRecoveryServicesAsrFabric** cmdlet 'ı, kurtarma hizmetleri kasasından belirtilen Azure Site Recovery yapınızı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="adadf-106">The **Remove-AzRecoveryServicesAsrFabric** cmdlet removes the specified Azure Site Recovery fabric from the Recovery services vault.</span></span>

## <span data-ttu-id="adadf-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="adadf-107">EXAMPLES</span></span>

### <span data-ttu-id="adadf-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="adadf-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrFabric -Fabric $Fabric
```

<span data-ttu-id="adadf-109">Belirtilen yapının silinmesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="adadf-109">Starts the deletion of specified fabric and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="adadf-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="adadf-110">PARAMETERS</span></span>

### <span data-ttu-id="adadf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adadf-111">-DefaultProfile</span></span>
<span data-ttu-id="adadf-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="adadf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="adadf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="adadf-113">-Force</span></span>
<span data-ttu-id="adadf-114">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="adadf-114">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="adadf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adadf-115">-InputObject</span></span>
<span data-ttu-id="adadf-116">Cmdlet 'e giriş nesnesi: silinecek yapıya karşılık gelen ASR Fabric nesnesi.</span><span class="sxs-lookup"><span data-stu-id="adadf-116">The input object to the cmdlet: The ASR fabric object corresponding to the fabric to be deleted.</span></span>

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

### <span data-ttu-id="adadf-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="adadf-117">-Confirm</span></span>
<span data-ttu-id="adadf-118">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="adadf-118">Specify if confirmation is required.</span></span> <span data-ttu-id="adadf-119">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="adadf-119">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="adadf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adadf-120">-WhatIf</span></span>
<span data-ttu-id="adadf-121">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="adadf-121">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="adadf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adadf-122">CommonParameters</span></span>
<span data-ttu-id="adadf-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="adadf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adadf-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adadf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adadf-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="adadf-125">INPUTS</span></span>

### <span data-ttu-id="adadf-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="adadf-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="adadf-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="adadf-127">OUTPUTS</span></span>

### <span data-ttu-id="adadf-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="adadf-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="adadf-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="adadf-129">NOTES</span></span>

## <span data-ttu-id="adadf-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="adadf-130">RELATED LINKS</span></span>

[<span data-ttu-id="adadf-131">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="adadf-131">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="adadf-132">Yeni-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="adadf-132">New-AzRecoveryServicesAsrFabric</span></span>](./New-AzRecoveryServicesAsrFabric.md)
