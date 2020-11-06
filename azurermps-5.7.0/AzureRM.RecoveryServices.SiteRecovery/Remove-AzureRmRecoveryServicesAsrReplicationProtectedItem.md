---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1df32bfcf049346b3f434b252a413eef020d0b77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589735"
---
# <span data-ttu-id="46591-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="46591-101">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="46591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46591-102">SYNOPSIS</span></span>
<span data-ttu-id="46591-103">Azure Site Recovery çoğaltması korumalı öğe için çoğaltmayı durdurur/devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="46591-103">Stops/Disables replication for an Azure Site Recovery replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46591-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46591-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46591-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="46591-105">DESCRIPTION</span></span>
<span data-ttu-id="46591-106">**Remove-Azurermrecoveryservicesasrreplicationkorunabilir** , belirtilen Azure Site Recovery çoğaltma korumalı öğesinin çoğaltılmasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="46591-106">The **Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet disables replication of the specified Azure Site Recovery replication protected item.</span></span>
<span data-ttu-id="46591-107">Bu işlem, korumalı öğe için çoğaltmanın durmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="46591-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="46591-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46591-108">EXAMPLES</span></span>

### <span data-ttu-id="46591-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="46591-109">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $ReplicationProtectedItem
```

<span data-ttu-id="46591-110">Belirtilen çoğaltma korumalı öğe için çoğaltmayı devre dışı bırak işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.</span><span class="sxs-lookup"><span data-stu-id="46591-110">Starts the disable replication operation for the specified replication protected item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="46591-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46591-111">PARAMETERS</span></span>

### <span data-ttu-id="46591-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="46591-112">-Confirm</span></span>
<span data-ttu-id="46591-113">Onayın gerekli olup olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="46591-113">Specify if confirmation is required.</span></span> <span data-ttu-id="46591-114">Onayı atlamak için Confirm parametresinin değerini $false olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="46591-114">Set the value of the confirm parameter to $false in order to skip confirmation.</span></span>

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

### <span data-ttu-id="46591-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46591-115">-DefaultProfile</span></span>
<span data-ttu-id="46591-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="46591-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="46591-117">-Force</span><span class="sxs-lookup"><span data-stu-id="46591-117">-Force</span></span>
<span data-ttu-id="46591-118">Ek bir uyarı vermeden komutu çalıştırmaya zorlayın.</span><span class="sxs-lookup"><span data-stu-id="46591-118">Force the command to run without providing an additional warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46591-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46591-119">-InputObject</span></span>
<span data-ttu-id="46591-120">Cmdlet 'e giriş nesnesi: çoğaltmanın devre dışı bırakıldığı çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesi.</span><span class="sxs-lookup"><span data-stu-id="46591-120">The input object to the cmdlet: The ASR replication protected item object corresponding to the replication protected item for which replication is to be disabled.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46591-121">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="46591-121">-WaitForCompletion</span></span>
<span data-ttu-id="46591-122">Cmdlet 'in işlemin tamamlanmasını beklemesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46591-122">Indicates that the cmdlet should wait for the operation to complete before returning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46591-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46591-123">-WhatIf</span></span>
<span data-ttu-id="46591-124">Cmdlet gerçekten yürütülmeden çalıştırıldığında ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46591-124">Shows what would happen if the cmdlet is executed without actually executing the cmdlet.</span></span>

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

### <span data-ttu-id="46591-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46591-125">CommonParameters</span></span>
<span data-ttu-id="46591-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46591-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46591-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46591-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46591-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46591-128">INPUTS</span></span>

### <span data-ttu-id="46591-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="46591-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="46591-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46591-130">OUTPUTS</span></span>

### <span data-ttu-id="46591-131">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="46591-131">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="46591-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46591-132">NOTES</span></span>

## <span data-ttu-id="46591-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46591-133">RELATED LINKS</span></span>

[<span data-ttu-id="46591-134">Get-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="46591-134">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="46591-135">New-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="46591-135">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="46591-136">Set-Azurermrecoveryservicesasrreplicationkorunabilir.</span><span class="sxs-lookup"><span data-stu-id="46591-136">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
