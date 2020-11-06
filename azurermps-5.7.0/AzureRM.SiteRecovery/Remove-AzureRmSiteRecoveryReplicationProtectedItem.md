---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B29B8CA8-091D-4521-BE97-33C10BC9139C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 121d45d626a226542f495cd197781b795823b1fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593379"
---
# <span data-ttu-id="ca12b-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ca12b-101">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="ca12b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca12b-102">SYNOPSIS</span></span>
<span data-ttu-id="ca12b-103">Azure Site Recovery çoğaltması korumalı öğeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ca12b-103">Removes an Azure Site Recovery Replication Protected Item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca12b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca12b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca12b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca12b-105">DESCRIPTION</span></span>
<span data-ttu-id="ca12b-106">**Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet 'ı, Azure Site Recovery çoğaltması korumalı öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ca12b-106">The **Remove-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet removes an Azure Site Recovery Replication Protected Item.</span></span>
<span data-ttu-id="ca12b-107">Bu işlem, korumalı öğe için çoğaltmanın durmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="ca12b-107">This operation causes replication to stop for the protected item.</span></span>

## <span data-ttu-id="ca12b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca12b-108">EXAMPLES</span></span>

## <span data-ttu-id="ca12b-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca12b-109">PARAMETERS</span></span>

### <span data-ttu-id="ca12b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca12b-110">-DefaultProfile</span></span>
<span data-ttu-id="ca12b-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca12b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca12b-112">-Force</span><span class="sxs-lookup"><span data-stu-id="ca12b-112">-Force</span></span>
<span data-ttu-id="ca12b-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ca12b-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ca12b-114">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="ca12b-114">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ca12b-115">Çoğaltma korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca12b-115">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="ca12b-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ca12b-116">-WaitForCompletion</span></span>
<span data-ttu-id="ca12b-117">Cmdlet 'in işlemin tamamlamasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca12b-117">Indicates that the cmdlet waits for the operation to complete.</span></span>

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

### <span data-ttu-id="ca12b-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca12b-118">-Confirm</span></span>
<span data-ttu-id="ca12b-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca12b-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca12b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca12b-120">-WhatIf</span></span>
<span data-ttu-id="ca12b-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca12b-121">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ca12b-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca12b-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca12b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca12b-123">CommonParameters</span></span>
<span data-ttu-id="ca12b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca12b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca12b-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca12b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca12b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca12b-126">INPUTS</span></span>

### <span data-ttu-id="ca12b-127">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="ca12b-127">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="ca12b-128">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ca12b-128">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="ca12b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca12b-129">OUTPUTS</span></span>

### <span data-ttu-id="ca12b-130">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ca12b-130">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ca12b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca12b-131">NOTES</span></span>

## <span data-ttu-id="ca12b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca12b-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca12b-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ca12b-133">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="ca12b-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ca12b-134">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="ca12b-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ca12b-135">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
