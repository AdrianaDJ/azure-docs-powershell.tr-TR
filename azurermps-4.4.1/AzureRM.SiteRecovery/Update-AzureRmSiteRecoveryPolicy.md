---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 313E7444-2EB4-4B91-9E56-5730CB006046
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 5279ca9664c827bdb85b42519f6776c10ab37e31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589057"
---
# <span data-ttu-id="8c043-101">Update-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="8c043-101">Update-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="8c043-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c043-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c043-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c043-103">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c043-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c043-104">DESCRIPTION</span></span>

## <span data-ttu-id="8c043-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c043-105">EXAMPLES</span></span>

## <span data-ttu-id="8c043-106">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c043-106">PARAMETERS</span></span>

### <span data-ttu-id="8c043-107">-Applicationpotentın</span><span class="sxs-lookup"><span data-stu-id="8c043-107">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-108">-Kimlik doğrulama</span><span class="sxs-lookup"><span data-stu-id="8c043-108">-Authentication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-109">Sıkıştırma</span><span class="sxs-lookup"><span data-stu-id="8c043-109">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-110">-Şifreleme</span><span class="sxs-lookup"><span data-stu-id="8c043-110">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-111">-İlke</span><span class="sxs-lookup"><span data-stu-id="8c043-111">-Policy</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-112">-Recoveryazurestorageaccountıd</span><span class="sxs-lookup"><span data-stu-id="8c043-112">-RecoveryAzureStorageAccountId</span></span>
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

### <span data-ttu-id="8c043-113">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="8c043-113">-RecoveryPoints</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-114">-Replicasilme</span><span class="sxs-lookup"><span data-stu-id="8c043-114">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-115">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="8c043-115">-ReplicationFrequencyInSeconds</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-116">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="8c043-116">-ReplicationMethod</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-117">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="8c043-117">-ReplicationPort</span></span>
```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-118">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="8c043-118">-ReplicationStartTime</span></span>
```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c043-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c043-119">-DefaultProfile</span></span>
<span data-ttu-id="8c043-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c043-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c043-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c043-121">CommonParameters</span></span>
<span data-ttu-id="8c043-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c043-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c043-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c043-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c043-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c043-124">INPUTS</span></span>

### <span data-ttu-id="8c043-125">Asrilkesi</span><span class="sxs-lookup"><span data-stu-id="8c043-125">ASRPolicy</span></span>
<span data-ttu-id="8c043-126">Parametre ' Ilke ', ardışık düzenin ' ASRPolicy ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="8c043-126">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="8c043-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c043-127">OUTPUTS</span></span>

## <span data-ttu-id="8c043-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c043-128">NOTES</span></span>

## <span data-ttu-id="8c043-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c043-129">RELATED LINKS</span></span>

