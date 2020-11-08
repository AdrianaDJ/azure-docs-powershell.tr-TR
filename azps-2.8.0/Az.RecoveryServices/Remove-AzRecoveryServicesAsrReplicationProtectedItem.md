---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 19a10312046a4c52ed1fad29732347f719065b95
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933469"
---
# <span data-ttu-id="cc97f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="cc97f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="cc97f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc97f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc97f-103">Azure Site Recovery çoğaltması korumalı öğe için çoğaltmayı durdurur/devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="cc97f-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

## <span data-ttu-id="cc97f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc97f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc97f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc97f-105">DESCRIPTION</span></span>
<span data-ttu-id="cc97f-106">**Remove-Azrecoveryservicesasrreplicationkorutdıtem** cmdlet 'ı belirtilen Azure Site Recovery çoğaltması korumalı öğenin çoğaltılmasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="cc97f-106">The **Remove-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="cc97f-107">Bu işlem, korumalı öğe için çoğaltmanın durmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="cc97f-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="cc97f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc97f-108">EXAMPLES</span></span>

### <span data-ttu-id="cc97f-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cc97f-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="cc97f-110">Belirtilen çoğaltma korumalı öğe için çoğaltmayı devre dışı bırak işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="cc97f-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cc97f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc97f-111">PARAMETERS</span></span>

### <span data-ttu-id="cc97f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc97f-112">-DefaultProfile</span></span>
<span data-ttu-id="cc97f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc97f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cc97f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="cc97f-114">-Force</span></span>
<span data-ttu-id="cc97f-115">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="cc97f-115">Force the command to run without providing an additional warning.</span></span>

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

### <span data-ttu-id="cc97f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc97f-116">-InputObject</span></span>
<span data-ttu-id="cc97f-117">Cmdlet 'e giriş nesnesi: çoğaltmanın devre dışı bırakıldığı çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cc97f-117">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc97f-118">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="cc97f-118">-WaitForCompletion</span></span>
<span data-ttu-id="cc97f-119">Cmdlet 'in işlemin tamamlanmasını beklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc97f-119">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

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

### <span data-ttu-id="cc97f-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc97f-120">-Confirm</span></span>
<span data-ttu-id="cc97f-121">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="cc97f-121">Specify if confirmation is required.</span></span> <span data-ttu-id="cc97f-122">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cc97f-122">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="cc97f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc97f-123">-WhatIf</span></span>
<span data-ttu-id="cc97f-124">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc97f-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="cc97f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc97f-125">CommonParameters</span></span>
<span data-ttu-id="cc97f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc97f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc97f-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc97f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc97f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc97f-128">INPUTS</span></span>

### <span data-ttu-id="cc97f-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="cc97f-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="cc97f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc97f-130">OUTPUTS</span></span>

### <span data-ttu-id="cc97f-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="cc97f-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cc97f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc97f-132">NOTES</span></span>

## <span data-ttu-id="cc97f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc97f-133">RELATED LINKS</span></span>

[<span data-ttu-id="cc97f-134">Get-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="cc97f-134">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="cc97f-135">New-Azrecoveryservicesasrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="cc97f-135">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="cc97f-136">Set-Azrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="cc97f-136">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)