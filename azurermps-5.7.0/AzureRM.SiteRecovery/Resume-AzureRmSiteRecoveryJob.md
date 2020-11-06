---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/resume-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: aae0bf7c2ec4a166d48edb032d6c21918dc3ae6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589674"
---
# <span data-ttu-id="2b8ce-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="2b8ce-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="2b8ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8ce-103">Askıya alınan bir site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="2b8ce-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b8ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b8ce-104">SYNTAX</span></span>

### <span data-ttu-id="2b8ce-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b8ce-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b8ce-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2b8ce-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b8ce-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b8ce-107">DESCRIPTION</span></span>
<span data-ttu-id="2b8ce-108">**Resume-AzureRmSiteRecoveryJob** cmdlet 'i askıya alınmış bir Azure Site kurtarma işini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="2b8ce-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="2b8ce-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b8ce-109">EXAMPLES</span></span>

## <span data-ttu-id="2b8ce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b8ce-110">PARAMETERS</span></span>

### <span data-ttu-id="2b8ce-111">-Açıklamalar</span><span class="sxs-lookup"><span data-stu-id="2b8ce-111">-Comments</span></span>
<span data-ttu-id="2b8ce-112">İş günlüğü için açıklamaları belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b8ce-112">Specifies the comments for the job log.</span></span>

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

### <span data-ttu-id="2b8ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8ce-113">-DefaultProfile</span></span>
<span data-ttu-id="2b8ce-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b8ce-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b8ce-115">-Job</span><span class="sxs-lookup"><span data-stu-id="2b8ce-115">-Job</span></span>
<span data-ttu-id="2b8ce-116">Site kurtarma işi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b8ce-116">Specifies the Site Recovery job object.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8ce-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b8ce-117">-Name</span></span>
<span data-ttu-id="2b8ce-118">İşin benzersiz adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b8ce-118">Specifies the unique name for the job.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8ce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8ce-119">CommonParameters</span></span>
<span data-ttu-id="2b8ce-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b8ce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8ce-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8ce-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8ce-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b8ce-122">INPUTS</span></span>

### <span data-ttu-id="2b8ce-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="2b8ce-123">ASRJob</span></span>
<span data-ttu-id="2b8ce-124">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="2b8ce-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="2b8ce-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b8ce-125">OUTPUTS</span></span>

### <span data-ttu-id="2b8ce-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2b8ce-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2b8ce-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b8ce-127">NOTES</span></span>

## <span data-ttu-id="2b8ce-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b8ce-128">RELATED LINKS</span></span>

[<span data-ttu-id="2b8ce-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="2b8ce-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="2b8ce-130">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="2b8ce-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="2b8ce-131">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="2b8ce-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
