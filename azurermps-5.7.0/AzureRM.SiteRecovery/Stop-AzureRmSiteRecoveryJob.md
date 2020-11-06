---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/stop-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 44875207b5a4317b2ceb9a0284a3818a6be36298
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573242"
---
# <span data-ttu-id="fa43b-101">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="fa43b-101">Stop-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="fa43b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa43b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa43b-103">Site kurtarma işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="fa43b-103">Stops a Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa43b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa43b-104">SYNTAX</span></span>

### <span data-ttu-id="fa43b-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa43b-105">ByObject (Default)</span></span>
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa43b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fa43b-106">ByName</span></span>
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa43b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa43b-107">DESCRIPTION</span></span>
<span data-ttu-id="fa43b-108">**Stop-AzureRmSiteRecoveryJob** cmdlet 'ı bir Azure Site Recovery işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="fa43b-108">The **Stop-AzureRmSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="fa43b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa43b-109">EXAMPLES</span></span>

## <span data-ttu-id="fa43b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa43b-110">PARAMETERS</span></span>

### <span data-ttu-id="fa43b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa43b-111">-DefaultProfile</span></span>
<span data-ttu-id="fa43b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa43b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa43b-113">-Job</span><span class="sxs-lookup"><span data-stu-id="fa43b-113">-Job</span></span>
<span data-ttu-id="fa43b-114">Durdurulacak Site Recovery iş nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa43b-114">Specifies the Site Recovery job object to stop.</span></span>

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

### <span data-ttu-id="fa43b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa43b-115">-Name</span></span>
<span data-ttu-id="fa43b-116">Site kurtarma işinin durması için benzersiz bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa43b-116">Specifies the unique name for the Site Recovery job to stop.</span></span>

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

### <span data-ttu-id="fa43b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa43b-117">CommonParameters</span></span>
<span data-ttu-id="fa43b-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa43b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa43b-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa43b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa43b-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa43b-120">INPUTS</span></span>

### <span data-ttu-id="fa43b-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="fa43b-121">ASRJob</span></span>
<span data-ttu-id="fa43b-122">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="fa43b-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="fa43b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa43b-123">OUTPUTS</span></span>

### <span data-ttu-id="fa43b-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fa43b-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fa43b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa43b-125">NOTES</span></span>

## <span data-ttu-id="fa43b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa43b-126">RELATED LINKS</span></span>

[<span data-ttu-id="fa43b-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="fa43b-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="fa43b-128">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="fa43b-128">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="fa43b-129">Özgeçmiş-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="fa43b-129">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)
