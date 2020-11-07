---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1EC96B4E-7731-4EE3-A0C1-EA0793F0FE5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/stop-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Stop-AzStreamAnalyticsJob.md
ms.openlocfilehash: 7b1b3af4a311b923880253573019c62ee399571c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937905"
---
# <span data-ttu-id="07adf-101">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07adf-101">Stop-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="07adf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07adf-102">SYNOPSIS</span></span>
<span data-ttu-id="07adf-103">Stream Analytics işini durdurur.</span><span class="sxs-lookup"><span data-stu-id="07adf-103">Stops a Stream Analytics job.</span></span>

## <span data-ttu-id="07adf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07adf-104">SYNTAX</span></span>

```
Stop-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07adf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="07adf-105">DESCRIPTION</span></span>
<span data-ttu-id="07adf-106">**Stop-AzStreamAnalyticsJob** cmdlet 'i, bir akış analizi işinin Azure 'da çalışmasını zaman uyumsuz olarak durdurur ve kullanılmış olan kaynakları ayırır.</span><span class="sxs-lookup"><span data-stu-id="07adf-106">The **Stop-AzStreamAnalyticsJob** cmdlet asynchronously stops a Stream Analytics job from running in Azure and deallocates resources that were that were being used.</span></span>
<span data-ttu-id="07adf-107">İş tanımı ve meta veriler, hem Azure Portal hem de yönetim API 'Leri ile aboneliğinizde kullanılabilir durumda kalır, böylece iş düzenlenebilir ve yeniden başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="07adf-107">The job definition and metadata remain available within your subscription through both the Azure Portal and Management APIs, such that the job can be edited and restarted.</span></span>
<span data-ttu-id="07adf-108">Durdurulmuş durumda bir iş için ücret ödemeyeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="07adf-108">You will not be charged for a job in the Stopped state.</span></span>

## <span data-ttu-id="07adf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07adf-109">EXAMPLES</span></span>

### <span data-ttu-id="07adf-110">Örnek 1: çalışan işi durdurma</span><span class="sxs-lookup"><span data-stu-id="07adf-110">EXAMPLE 1: Stop a running job</span></span>
```
PS C:\>Stop-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="07adf-111">Bu komut, iş StreamingJob işlemini durdurur.</span><span class="sxs-lookup"><span data-stu-id="07adf-111">This command stops the job StreamingJob.</span></span>

## <span data-ttu-id="07adf-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07adf-112">PARAMETERS</span></span>

### <span data-ttu-id="07adf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07adf-113">-DefaultProfile</span></span>
<span data-ttu-id="07adf-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07adf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07adf-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="07adf-115">-Name</span></span>
<span data-ttu-id="07adf-116">Durdurulacak Azure Stream Analytics işinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07adf-116">Specifies the name of the Azure Stream Analytics job to stop.</span></span>

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

### <span data-ttu-id="07adf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07adf-117">-ResourceGroupName</span></span>
<span data-ttu-id="07adf-118">Azure Stream Analytics işinin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07adf-118">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="07adf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07adf-119">CommonParameters</span></span>
<span data-ttu-id="07adf-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07adf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07adf-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07adf-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07adf-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07adf-122">INPUTS</span></span>

### <span data-ttu-id="07adf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="07adf-123">System.String</span></span>

## <span data-ttu-id="07adf-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07adf-124">OUTPUTS</span></span>

### <span data-ttu-id="07adf-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="07adf-125">System.Boolean</span></span>

## <span data-ttu-id="07adf-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07adf-126">NOTES</span></span>

## <span data-ttu-id="07adf-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07adf-127">RELATED LINKS</span></span>

[<span data-ttu-id="07adf-128">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07adf-128">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="07adf-129">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07adf-129">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="07adf-130">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07adf-130">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="07adf-131">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07adf-131">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="07adf-132">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="07adf-132">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)


