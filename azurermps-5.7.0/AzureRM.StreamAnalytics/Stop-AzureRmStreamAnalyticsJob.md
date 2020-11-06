---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 13e977ebe4acdfb799d830620ce7963ad1066177
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573138"
---
# <span data-ttu-id="e1515-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e1515-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="e1515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1515-102">SYNOPSIS</span></span>
<span data-ttu-id="e1515-103">Stream Analytics işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="e1515-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1515-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1515-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1515-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1515-105">DESCRIPTION</span></span>
<span data-ttu-id="e1515-106">**Stop-AzureRmStreamAnalyticsJob** cmdlet 'i, bir akış analizi işinin Azure 'da çalışmasını zaman uyumsuz olarak durdurur ve kullanılmış olan kaynakları ayırır.</span><span class="sxs-lookup"><span data-stu-id="e1515-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="e1515-107">İş tanımı ve meta veriler, hem Azure Portal hem de yönetim API 'Leri ile aboneliğinizde kullanılabilir durumda kalır, böylece iş düzenlenebilir ve yeniden başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="e1515-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="e1515-108">Durdurulmuş durumda bir iş için ücret ödemeyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="e1515-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="e1515-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1515-109">EXAMPLES</span></span>

### <span data-ttu-id="e1515-110">Örnek 1: çalışan işi durdurma</span><span class="sxs-lookup"><span data-stu-id="e1515-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="e1515-111">Bu komut, iş StreamingJob işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="e1515-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="e1515-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1515-112">PARAMETERS</span></span>

### <span data-ttu-id="e1515-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1515-113">-DefaultProfile</span></span>
<span data-ttu-id="e1515-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1515-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1515-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e1515-115">-Name</span></span>
<span data-ttu-id="e1515-116">Durdurulacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1515-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1515-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1515-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1515-118">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1515-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1515-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1515-119">CommonParameters</span></span>
<span data-ttu-id="e1515-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1515-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1515-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1515-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1515-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1515-122">INPUTS</span></span>

### <span data-ttu-id="e1515-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e1515-123">None</span></span>
<span data-ttu-id="e1515-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e1515-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1515-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1515-125">OUTPUTS</span></span>

### <span data-ttu-id="e1515-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="e1515-126">System.Object</span></span>

## <span data-ttu-id="e1515-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1515-127">NOTES</span></span>

## <span data-ttu-id="e1515-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1515-128">RELATED LINKS</span></span>

[<span data-ttu-id="e1515-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e1515-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e1515-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e1515-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e1515-131">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e1515-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e1515-132">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e1515-132">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e1515-133">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e1515-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


