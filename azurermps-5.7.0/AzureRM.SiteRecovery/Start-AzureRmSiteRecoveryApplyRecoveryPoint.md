---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 86A60FD6-551A-4A6B-A4D1-466F33CE714A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryapplyrecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryApplyRecoveryPoint.md
ms.openlocfilehash: 97ebacf9f5c51778122bfb8e8157692b7f1dfd03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593373"
---
# <span data-ttu-id="a613f-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a613f-101">Start-AzureRmSiteRecoveryApplyRecoveryPoint</span></span>

## <span data-ttu-id="a613f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a613f-102">SYNOPSIS</span></span>
<span data-ttu-id="a613f-103">Yük devretme işlemini uygulamadan önce korunan bir öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a613f-103">Changes a recovery point for a failed over protected item before commiting the failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a613f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a613f-104">SYNTAX</span></span>

```
Start-AzureRmSiteRecoveryApplyRecoveryPoint -RecoveryPoint <ASRRecoveryPoint>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a613f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a613f-105">DESCRIPTION</span></span>
<span data-ttu-id="a613f-106">**Start-Azurermsitereliplyrecoverypoint** , yük devretme işlemini kaydetmeden önce, yük devremeyen bir öğenin kurtarma noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a613f-106">The **Start-AzureRmSiteRecoveryApplyRecoveryPoint** changes a recovery point for a failed over protected item before it commits the failover operation.</span></span>

## <span data-ttu-id="a613f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a613f-107">EXAMPLES</span></span>

## <span data-ttu-id="a613f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a613f-108">PARAMETERS</span></span>

### <span data-ttu-id="a613f-109">-Dataencryptionprimarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="a613f-109">-DataEncryptionPrimaryCertFile</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a613f-110">-Dataencryptionsecondarysertifikadosyası</span><span class="sxs-lookup"><span data-stu-id="a613f-110">-DataEncryptionSecondaryCertFile</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a613f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a613f-111">-DefaultProfile</span></span>
<span data-ttu-id="a613f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a613f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a613f-113">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="a613f-113">-RecoveryPoint</span></span>
<span data-ttu-id="a613f-114">Bu cmdlet 'in değiştirdiği kurtarma noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a613f-114">Specifies the recovery point object that this cmdlet changes.</span></span>

```yaml
Type: ASRRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a613f-115">-Replicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="a613f-115">-ReplicationProtectedItem</span></span>
<span data-ttu-id="a613f-116">Çoğaltma korumalı öğe nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a613f-116">Specifies the Replication Protected Item object.</span></span>

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

### <span data-ttu-id="a613f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a613f-117">CommonParameters</span></span>
<span data-ttu-id="a613f-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a613f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a613f-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a613f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a613f-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a613f-120">INPUTS</span></span>

### <span data-ttu-id="a613f-121">Asrreplicationkorunabilir</span><span class="sxs-lookup"><span data-stu-id="a613f-121">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="a613f-122">' Replicationkorunabilir ' parametresi, ardışık düzenin ' Asrreplicationkorunabilir ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a613f-122">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="a613f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a613f-123">OUTPUTS</span></span>

### <span data-ttu-id="a613f-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="a613f-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a613f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a613f-125">NOTES</span></span>

## <span data-ttu-id="a613f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a613f-126">RELATED LINKS</span></span>

[<span data-ttu-id="a613f-127">Azure Site kurtarma cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="a613f-127">Azure Site Recovery Cmdlets</span></span>](./AzureRM.SiteRecovery.md)
