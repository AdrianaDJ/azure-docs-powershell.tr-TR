---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: e1d5dd0c8548b52fde37044d304269358a11af70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764215"
---
# <span data-ttu-id="ec8b8-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ec8b8-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="ec8b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8b8-103">Azure Site Recovery çoğaltması korumalı öğeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec8b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec8b8-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec8b8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec8b8-105">DESCRIPTION</span></span>
<span data-ttu-id="ec8b8-106">**Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet 'ı, Azure Site Recovery çoğaltması korumalı öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="ec8b8-107">Bu işlem, korumalı öğe için çoğaltmanın durmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="ec8b8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec8b8-108">EXAMPLES</span></span>

## <span data-ttu-id="ec8b8-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec8b8-109">PARAMETERS</span></span>

### <span data-ttu-id="ec8b8-110">-Force</span><span class="sxs-lookup"><span data-stu-id="ec8b8-110">-Force</span></span>
<span data-ttu-id="ec8b8-111">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-111">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ec8b8-112">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="ec8b8-112">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ec8b8-113">Çoğaltma korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-113">Specifies the Replication Protected Item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec8b8-114">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ec8b8-114">-WaitForCompletion</span></span>
<span data-ttu-id="ec8b8-115">Cmdlet 'in işlemin tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-115">Indicates that the cmdlet waits for the operation to complete.</span></span>

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

### <span data-ttu-id="ec8b8-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec8b8-116">-Confirm</span></span>
<span data-ttu-id="ec8b8-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8b8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec8b8-118">-WhatIf</span></span>
<span data-ttu-id="ec8b8-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-119">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ec8b8-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec8b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8b8-121">-DefaultProfile</span></span>
<span data-ttu-id="ec8b8-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec8b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8b8-123">CommonParameters</span></span>
<span data-ttu-id="ec8b8-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec8b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8b8-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec8b8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8b8-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec8b8-126">INPUTS</span></span>

### <span data-ttu-id="ec8b8-127">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="ec8b8-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="ec8b8-128">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ec8b8-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="ec8b8-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec8b8-129">OUTPUTS</span></span>

### <span data-ttu-id="ec8b8-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ec8b8-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ec8b8-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec8b8-131">NOTES</span></span>

## <span data-ttu-id="ec8b8-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec8b8-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec8b8-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ec8b8-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="ec8b8-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ec8b8-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="ec8b8-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ec8b8-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
