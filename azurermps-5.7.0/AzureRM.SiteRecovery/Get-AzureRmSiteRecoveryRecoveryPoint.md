---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77AFEF57-A4ED-4F82-A3FF-0E33D7810B3B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPoint.md
ms.openlocfilehash: 42a0a96a32bf1b7f556ee2787f43a5777afa1115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593401"
---
# <span data-ttu-id="e5f06-101">Get-AzureRmSiteRecoveryRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e5f06-101">Get-AzureRmSiteRecoveryRecoveryPoint</span></span>

## <span data-ttu-id="e5f06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f06-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f06-103">Çoğaltma korumalı öğe için kullanılabilir kurtarma noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="e5f06-103">Gets available recovery points for a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5f06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5f06-104">SYNTAX</span></span>

### <span data-ttu-id="e5f06-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5f06-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5f06-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="e5f06-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPoint -Name <String> -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5f06-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5f06-107">DESCRIPTION</span></span>
<span data-ttu-id="e5f06-108">**Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet 'i, çoğaltma korumalı bir öğe için kullanılabilir kurtarma noktalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e5f06-108">The **Get-AzureRmSiteRecoveryRecoveryPoint** cmdlet gets the list of available recovery points for a replication protected item.</span></span>

## <span data-ttu-id="e5f06-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5f06-109">EXAMPLES</span></span>

## <span data-ttu-id="e5f06-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5f06-110">PARAMETERS</span></span>

### <span data-ttu-id="e5f06-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f06-111">-DefaultProfile</span></span>
<span data-ttu-id="e5f06-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5f06-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5f06-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5f06-113">-Name</span></span>
<span data-ttu-id="e5f06-114">Bu cmdlet 'in aldığı kurtarma noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5f06-114">Specifies the name of the recovery point this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f06-115">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="e5f06-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e5f06-116">Azure Site Recovery çoğaltması korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5f06-116">Specifies the Azure Site Recovery Replication Protected Item object.</span></span>

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

### <span data-ttu-id="e5f06-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f06-117">CommonParameters</span></span>
<span data-ttu-id="e5f06-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5f06-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f06-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f06-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f06-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5f06-120">INPUTS</span></span>

### <span data-ttu-id="e5f06-121">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="e5f06-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="e5f06-122">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e5f06-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="e5f06-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5f06-123">OUTPUTS</span></span>

### <span data-ttu-id="e5f06-124">System. Koleksiyonlar. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPoint, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e5f06-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e5f06-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5f06-125">NOTES</span></span>

## <span data-ttu-id="e5f06-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5f06-126">RELATED LINKS</span></span>

[<span data-ttu-id="e5f06-127">Düzenle-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5f06-127">Edit-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Edit-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="e5f06-128">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5f06-128">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Get-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="e5f06-129">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5f06-129">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="e5f06-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5f06-130">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="e5f06-131">Güncelleştirme-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e5f06-131">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
