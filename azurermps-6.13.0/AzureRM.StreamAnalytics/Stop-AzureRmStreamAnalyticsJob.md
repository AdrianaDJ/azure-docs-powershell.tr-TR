---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/stop-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Stop-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: d4ec2865f0a0efcc4a306d0614df1c27adddc5b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593605"
---
# <span data-ttu-id="0b5b7-101">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b5b7-101">Stop-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="0b5b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5b7-103">Stream Analytics işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="0b5b7-103">Stops a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b5b7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b5b7-104">SYNTAX</span></span>

```
Stop-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b5b7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b5b7-105">DESCRIPTION</span></span>
<span data-ttu-id="0b5b7-106">**Stop-AzureRmStreamAnalyticsJob** cmdlet 'i, bir akış analizi işinin Azure 'da çalışmasını zaman uyumsuz olarak durdurur ve kullanılmış olan kaynakları ayırır.</span><span class="sxs-lookup"><span data-stu-id="0b5b7-106">The **Stop-AzureRmStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="0b5b7-107">İş tanımı ve meta veriler, hem Azure Portal hem de yönetim API 'Leri ile aboneliğinizde kullanılabilir durumda kalır, böylece iş düzenlenebilir ve yeniden başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="0b5b7-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="0b5b7-108">Durdurulmuş durumda bir iş için ücret ödemeyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="0b5b7-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="0b5b7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b5b7-109">EXAMPLES</span></span>

### <span data-ttu-id="0b5b7-110">Örnek 1: çalışan işi durdurma</span><span class="sxs-lookup"><span data-stu-id="0b5b7-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="0b5b7-111">Bu komut, iş StreamingJob işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="0b5b7-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="0b5b7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b5b7-112">PARAMETERS</span></span>

### <span data-ttu-id="0b5b7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5b7-113">-DefaultProfile</span></span>
<span data-ttu-id="0b5b7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b5b7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b5b7-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b5b7-115">-Name</span></span>
<span data-ttu-id="0b5b7-116">Durdurulacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b5b7-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5b7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5b7-117">-ResourceGroupName</span></span>
<span data-ttu-id="0b5b7-118">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b5b7-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b5b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5b7-119">CommonParameters</span></span>
<span data-ttu-id="0b5b7-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b5b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5b7-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b5b7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5b7-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b5b7-122">INPUTS</span></span>

### <span data-ttu-id="0b5b7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0b5b7-123">System.String</span></span>

## <span data-ttu-id="0b5b7-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b5b7-124">OUTPUTS</span></span>

### <span data-ttu-id="0b5b7-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0b5b7-125">System.Boolean</span></span>

## <span data-ttu-id="0b5b7-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b5b7-126">NOTES</span></span>

## <span data-ttu-id="0b5b7-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b5b7-127">RELATED LINKS</span></span>

[<span data-ttu-id="0b5b7-128">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b5b7-128">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="0b5b7-129">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b5b7-129">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="0b5b7-130">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b5b7-130">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="0b5b7-131">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b5b7-131">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="0b5b7-132">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0b5b7-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)


