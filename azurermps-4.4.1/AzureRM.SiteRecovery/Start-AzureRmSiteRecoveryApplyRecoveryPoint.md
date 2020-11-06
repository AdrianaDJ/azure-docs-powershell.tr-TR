---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: d77ed7723ef9875413c551912563b4ee2f4ae306
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589067"
---
# <span data-ttu-id="e30b6-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e30b6-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="e30b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e30b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e30b6-103">Yük devretme işlemini uygulamadan önce korunan bir öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e30b6-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e30b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e30b6-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e30b6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e30b6-105">DESCRIPTION</span></span>
<span data-ttu-id="e30b6-106">**Start-Azurermsitereliplyrecoverypoint** , yük devretme işlemini kaydetmeden önce, yük devremeyen bir öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e30b6-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="e30b6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e30b6-107">EXAMPLES</span></span>

## <span data-ttu-id="e30b6-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e30b6-108">PARAMETERS</span></span>

### <span data-ttu-id="e30b6-109">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="e30b6-109">-DataEncryptionPrimaryCertFile</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30b6-110">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="e30b6-110">-DataEncryptionSecondaryCertFile</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30b6-111">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e30b6-111">-RecoveryPoint</span></span>
<span data-ttu-id="e30b6-112">Bu cmdlet 'in değiştirdiği kurtarma noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e30b6-112">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e30b6-113">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="e30b6-113">-ReplicationProtectedItem</span></span>
<span data-ttu-id="e30b6-114">Çoğaltma korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e30b6-114">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="e30b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e30b6-115">-DefaultProfile</span></span>
<span data-ttu-id="e30b6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e30b6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e30b6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e30b6-117">CommonParameters</span></span>
<span data-ttu-id="e30b6-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e30b6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e30b6-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e30b6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e30b6-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e30b6-120">INPUTS</span></span>

### <span data-ttu-id="e30b6-121">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="e30b6-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="e30b6-122">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e30b6-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="e30b6-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e30b6-123">OUTPUTS</span></span>

### <span data-ttu-id="e30b6-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e30b6-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e30b6-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e30b6-125">NOTES</span></span>

## <span data-ttu-id="e30b6-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e30b6-126">RELATED LINKS</span></span>

[<span data-ttu-id="e30b6-127">Azure Site kurtarma cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="e30b6-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
