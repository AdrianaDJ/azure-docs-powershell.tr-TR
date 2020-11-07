---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763310"
---
# <span data-ttu-id="ee7dd-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ee7dd-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="ee7dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee7dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ee7dd-103">Askıya alınan bir site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="ee7dd-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee7dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee7dd-104">SYNTAX</span></span>

### <span data-ttu-id="ee7dd-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee7dd-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ee7dd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ee7dd-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee7dd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee7dd-107">DESCRIPTION</span></span>
<span data-ttu-id="ee7dd-108">**Resume-AzureRmSiteRecoveryJob** cmdlet 'i askıya alınmış bir Azure Site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="ee7dd-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="ee7dd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee7dd-109">EXAMPLES</span></span>

## <span data-ttu-id="ee7dd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee7dd-110">PARAMETERS</span></span>

### <span data-ttu-id="ee7dd-111">-Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="ee7dd-111">-Comments</span></span>
<span data-ttu-id="ee7dd-112">İş günlüğü için açıklamaları belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee7dd-112">Specifies the comments for the job log.</span></span>

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

### <span data-ttu-id="ee7dd-113">-Job</span><span class="sxs-lookup"><span data-stu-id="ee7dd-113">-Job</span></span>
<span data-ttu-id="ee7dd-114">Site kurtarma işi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee7dd-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="ee7dd-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ee7dd-115">-Name</span></span>
<span data-ttu-id="ee7dd-116">İşin benzersiz adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ee7dd-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="ee7dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee7dd-117">-DefaultProfile</span></span>
<span data-ttu-id="ee7dd-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ee7dd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee7dd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee7dd-119">CommonParameters</span></span>
<span data-ttu-id="ee7dd-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee7dd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee7dd-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee7dd-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee7dd-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee7dd-122">INPUTS</span></span>

### <span data-ttu-id="ee7dd-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="ee7dd-123">ASRJob</span></span>
<span data-ttu-id="ee7dd-124">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="ee7dd-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="ee7dd-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee7dd-125">OUTPUTS</span></span>

### <span data-ttu-id="ee7dd-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ee7dd-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ee7dd-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee7dd-127">NOTES</span></span>

## <span data-ttu-id="ee7dd-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee7dd-128">RELATED LINKS</span></span>

[<span data-ttu-id="ee7dd-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ee7dd-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="ee7dd-130">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ee7dd-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="ee7dd-131">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ee7dd-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
