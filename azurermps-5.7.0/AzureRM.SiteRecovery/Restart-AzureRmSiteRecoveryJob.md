---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573249"
---
# <span data-ttu-id="8c477-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8c477-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="8c477-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c477-102">SYNOPSIS</span></span>
<span data-ttu-id="8c477-103">Azure Site kurtarma işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="8c477-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c477-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c477-104">SYNTAX</span></span>

### <span data-ttu-id="8c477-105">ByObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8c477-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c477-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8c477-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c477-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c477-107">DESCRIPTION</span></span>
<span data-ttu-id="8c477-108">**Restart-AzureRmSiteRecoveryJob** cmdlet 'ı bir Azure Site Recovery işini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="8c477-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="8c477-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c477-109">EXAMPLES</span></span>

## <span data-ttu-id="8c477-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c477-110">PARAMETERS</span></span>

### <span data-ttu-id="8c477-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c477-111">-DefaultProfile</span></span>
<span data-ttu-id="8c477-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c477-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c477-113">-Job</span><span class="sxs-lookup"><span data-stu-id="8c477-113">-Job</span></span>
<span data-ttu-id="8c477-114">Site kurtarma işi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c477-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="8c477-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="8c477-115">-Name</span></span>
<span data-ttu-id="8c477-116">İşin benzersiz adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c477-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="8c477-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c477-117">CommonParameters</span></span>
<span data-ttu-id="8c477-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c477-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c477-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c477-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c477-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c477-120">INPUTS</span></span>

### <span data-ttu-id="8c477-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="8c477-121">ASRJob</span></span>
<span data-ttu-id="8c477-122">Parametre ' Iş ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="8c477-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="8c477-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c477-123">OUTPUTS</span></span>

### <span data-ttu-id="8c477-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8c477-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8c477-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c477-125">NOTES</span></span>

## <span data-ttu-id="8c477-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c477-126">RELATED LINKS</span></span>

[<span data-ttu-id="8c477-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8c477-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="8c477-128">Özgeçmiş-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8c477-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="8c477-129">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8c477-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
