---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 79ad35a00fcd0aef62e99a217071589e10f973c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589059"
---
# <span data-ttu-id="84cea-101">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="84cea-101">Stop-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="84cea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84cea-102">SYNOPSIS</span></span>
<span data-ttu-id="84cea-103">Site kurtarma işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="84cea-103">Stops a Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84cea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84cea-104">SYNTAX</span></span>

### <span data-ttu-id="84cea-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="84cea-105">ByObject (Default)</span></span>
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84cea-106">ByName</span><span class="sxs-lookup"><span data-stu-id="84cea-106">ByName</span></span>
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84cea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="84cea-107">DESCRIPTION</span></span>
<span data-ttu-id="84cea-108">**Stop-AzureRmSiteRecoveryJob** cmdlet 'ı bir Azure Site Recovery işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="84cea-108">The **Stop-AzureRmSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="84cea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84cea-109">EXAMPLES</span></span>

## <span data-ttu-id="84cea-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84cea-110">PARAMETERS</span></span>

### <span data-ttu-id="84cea-111">-Job</span><span class="sxs-lookup"><span data-stu-id="84cea-111">-Job</span></span>
<span data-ttu-id="84cea-112">Durdurulacak Site Recovery iş nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="84cea-112">Specifies the Site Recovery job object to stop.</span></span>

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

### <span data-ttu-id="84cea-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="84cea-113">-Name</span></span>
<span data-ttu-id="84cea-114">Site kurtarma işinin durması için benzersiz bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="84cea-114">Specifies the unique name for the Site Recovery job to stop.</span></span>

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

### <span data-ttu-id="84cea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84cea-115">-DefaultProfile</span></span>
<span data-ttu-id="84cea-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84cea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84cea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84cea-117">CommonParameters</span></span>
<span data-ttu-id="84cea-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84cea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84cea-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84cea-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84cea-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84cea-120">INPUTS</span></span>

### <span data-ttu-id="84cea-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="84cea-121">ASRJob</span></span>
<span data-ttu-id="84cea-122">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="84cea-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="84cea-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84cea-123">OUTPUTS</span></span>

### <span data-ttu-id="84cea-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="84cea-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="84cea-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84cea-125">NOTES</span></span>

## <span data-ttu-id="84cea-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84cea-126">RELATED LINKS</span></span>

[<span data-ttu-id="84cea-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="84cea-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="84cea-128">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="84cea-128">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="84cea-129">Özgeçmiş-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="84cea-129">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)
