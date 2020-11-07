---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 68e005a4e54277ad1be304911645c3eeda455d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764769"
---
# <span data-ttu-id="f860a-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f860a-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="f860a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f860a-102">SYNOPSIS</span></span>
<span data-ttu-id="f860a-103">Çoğaltma korumalı öğe için kullanılabilir kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="f860a-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f860a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f860a-104">SYNTAX</span></span>

### <span data-ttu-id="f860a-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f860a-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f860a-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f860a-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f860a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f860a-107">DESCRIPTION</span></span>
<span data-ttu-id="f860a-108">**Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet 'i, çoğaltma korumalı bir öğe için kullanılabilir kurtarma noktalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="f860a-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="f860a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f860a-109">EXAMPLES</span></span>

## <span data-ttu-id="f860a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f860a-110">PARAMETERS</span></span>

### <span data-ttu-id="f860a-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="f860a-111">-Name</span></span>
<span data-ttu-id="f860a-112">Bu cmdlet 'in aldığı kurtarma noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f860a-112">Specifies the name of the recovery point this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f860a-113">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="f860a-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="f860a-114">Azure Site Recovery çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f860a-114">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

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

### <span data-ttu-id="f860a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f860a-115">-DefaultProfile</span></span>
<span data-ttu-id="f860a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f860a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f860a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f860a-117">CommonParameters</span></span>
<span data-ttu-id="f860a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f860a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f860a-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f860a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f860a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f860a-120">INPUTS</span></span>

### <span data-ttu-id="f860a-121">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="f860a-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="f860a-122">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f860a-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="f860a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f860a-123">OUTPUTS</span></span>

### <span data-ttu-id="f860a-124">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f860a-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f860a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f860a-125">NOTES</span></span>

## <span data-ttu-id="f860a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f860a-126">RELATED LINKS</span></span>

[<span data-ttu-id="f860a-127">Düzenle-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f860a-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f860a-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f860a-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f860a-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f860a-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f860a-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f860a-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="f860a-131">Güncelleştirme-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f860a-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
