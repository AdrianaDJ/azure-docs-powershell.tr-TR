---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B5CA6FD9-49EE-4115-8477-551CE5D8E6CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 2365b806bd274bb9cc18f84c83a29423408780d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762401"
---
# <span data-ttu-id="58968-101">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="58968-101">Get-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="58968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58968-102">SYNOPSIS</span></span>
<span data-ttu-id="58968-103">Geçerli site kurtarma Kasası için işlem bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="58968-103">Gets the operation information for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58968-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58968-104">SYNTAX</span></span>

### <span data-ttu-id="58968-105">ByParam (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58968-105">ByParam (Default)</span></span>
```
Get-AzureRmSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58968-106">ByName</span><span class="sxs-lookup"><span data-stu-id="58968-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58968-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="58968-107">ByObject</span></span>
```
Get-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58968-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="58968-108">DESCRIPTION</span></span>
<span data-ttu-id="58968-109">**Get-AzureRmSiteRecoveryJob** cmdlet 'ı Azure Site Recovery işlerini alır.</span><span class="sxs-lookup"><span data-stu-id="58968-109">The **Get-AzureRmSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="58968-110">Bu cmdlet 'i, geçerli site kurtarma Kasası için işlem bilgilerini görüntülemek üzere kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="58968-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="58968-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58968-111">EXAMPLES</span></span>

## <span data-ttu-id="58968-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58968-112">PARAMETERS</span></span>

### <span data-ttu-id="58968-113">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="58968-113">-EndTime</span></span>
<span data-ttu-id="58968-114">İşlerin bitiş zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58968-114">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="58968-115">Bu cmdlet belirtilen süreden önce başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="58968-115">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="58968-116">Bu parametre için bir **DateTime** nesnesi almak istiyorsanız Get-Date cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="58968-116">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="58968-117">Daha fazla bilgi için yazın `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="58968-117">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58968-118">-Job</span><span class="sxs-lookup"><span data-stu-id="58968-118">-Job</span></span>
<span data-ttu-id="58968-119">Site kurtarma işini belirtir.</span><span class="sxs-lookup"><span data-stu-id="58968-119">Specifies the Site Recovery job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58968-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="58968-120">-Name</span></span>
<span data-ttu-id="58968-121">İşi tanımlayan benzersiz bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="58968-121">Specifies a unique name that identifies the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58968-122">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="58968-122">-StartTime</span></span>
<span data-ttu-id="58968-123">İşlerin başlangıç zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="58968-123">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="58968-124">Bu cmdlet belirtilen süreden sonra başlatılan tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="58968-124">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58968-125">Durumlu</span><span class="sxs-lookup"><span data-stu-id="58968-125">-State</span></span>
<span data-ttu-id="58968-126">Site kurtarma işi için giriş durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="58968-126">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="58968-127">Bu cmdlet belirtilen durumla eşleşen tüm işleri alır.</span><span class="sxs-lookup"><span data-stu-id="58968-127">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="58968-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="58968-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58968-129">NotStarted</span><span class="sxs-lookup"><span data-stu-id="58968-129">NotStarted</span></span>
- <span data-ttu-id="58968-130">Progress</span><span class="sxs-lookup"><span data-stu-id="58968-130">InProgress</span></span>
- <span data-ttu-id="58968-131">Oluşturuldu</span><span class="sxs-lookup"><span data-stu-id="58968-131">Succeeded</span></span>
- <span data-ttu-id="58968-132">Diğerini</span><span class="sxs-lookup"><span data-stu-id="58968-132">Other</span></span>
- <span data-ttu-id="58968-133">Erişilemedi</span><span class="sxs-lookup"><span data-stu-id="58968-133">Failed</span></span>
- <span data-ttu-id="58968-134">İptal</span><span class="sxs-lookup"><span data-stu-id="58968-134">Cancelled</span></span>
- <span data-ttu-id="58968-135">Etsin</span><span class="sxs-lookup"><span data-stu-id="58968-135">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58968-136">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="58968-136">-TargetObjectId</span></span>
<span data-ttu-id="58968-137">İş tarafından hedeflenen nesnenin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="58968-137">Specifies the ID of the object targeted by the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58968-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58968-138">-DefaultProfile</span></span>
<span data-ttu-id="58968-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58968-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58968-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58968-140">CommonParameters</span></span>
<span data-ttu-id="58968-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58968-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58968-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58968-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58968-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58968-143">INPUTS</span></span>

### <span data-ttu-id="58968-144">ASRJob</span><span class="sxs-lookup"><span data-stu-id="58968-144">ASRJob</span></span>
<span data-ttu-id="58968-145">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="58968-145">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="58968-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58968-146">OUTPUTS</span></span>

### <span data-ttu-id="58968-147">System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRJob]</span><span class="sxs-lookup"><span data-stu-id="58968-147">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRJob]</span></span>

## <span data-ttu-id="58968-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58968-148">NOTES</span></span>

## <span data-ttu-id="58968-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58968-149">RELATED LINKS</span></span>

[<span data-ttu-id="58968-150">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="58968-150">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="58968-151">Özgeçmiş-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="58968-151">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="58968-152">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="58968-152">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
