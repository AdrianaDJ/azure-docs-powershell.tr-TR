---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/wait-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Wait-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 047d0c7c9b141f10ee3f1be2ba1e739960f2e5bc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096007"
---
# <span data-ttu-id="2096a-101">Wait-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="2096a-101">Wait-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="2096a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2096a-102">SYNOPSIS</span></span>
<span data-ttu-id="2096a-103">İşin tamamlanmasını bekler.</span><span class="sxs-lookup"><span data-stu-id="2096a-103">Waits for a job to complete.</span></span>

## <span data-ttu-id="2096a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2096a-104">SYNTAX</span></span>

```
Wait-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2096a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2096a-105">DESCRIPTION</span></span>
<span data-ttu-id="2096a-106">**Wait-Azverilakeanaliz Ticsjob** cmdlet 'ı bir Azure Data Lake Analytics işinin tamamlamasını bekler.</span><span class="sxs-lookup"><span data-stu-id="2096a-106">The **Wait-AzDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="2096a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2096a-107">EXAMPLES</span></span>

### <span data-ttu-id="2096a-108">Örnek 1: işin tamamlanmasını bekle</span><span class="sxs-lookup"><span data-stu-id="2096a-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="2096a-109">Aşağıdaki komut belirtilen KIMLIğIN tamamlanma işini bekler.</span><span class="sxs-lookup"><span data-stu-id="2096a-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="2096a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2096a-110">PARAMETERS</span></span>

### <span data-ttu-id="2096a-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="2096a-111">-Account</span></span>
<span data-ttu-id="2096a-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2096a-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2096a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2096a-113">-DefaultProfile</span></span>
<span data-ttu-id="2096a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2096a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2096a-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="2096a-115">-JobId</span></span>
<span data-ttu-id="2096a-116">Bekleme işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2096a-116">Specifies the ID of the job for which to wait.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2096a-117">-Timeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="2096a-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="2096a-118">Bekleme işleminden çıkmadan önce beklenecek saniye sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2096a-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2096a-119">-Waitıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="2096a-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="2096a-120">İş durumu denetimi arasında geçen saniye sayısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="2096a-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2096a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2096a-121">CommonParameters</span></span>
<span data-ttu-id="2096a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2096a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2096a-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2096a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2096a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2096a-124">INPUTS</span></span>

### <span data-ttu-id="2096a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2096a-125">System.String</span></span>

### <span data-ttu-id="2096a-126">System. Guid</span><span class="sxs-lookup"><span data-stu-id="2096a-126">System.Guid</span></span>

### <span data-ttu-id="2096a-127">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2096a-127">System.Int32</span></span>

## <span data-ttu-id="2096a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2096a-128">OUTPUTS</span></span>

### <span data-ttu-id="2096a-129">Microsoft. Azure. Management. DataLake. Analytics. modeller. Jobınformation</span><span class="sxs-lookup"><span data-stu-id="2096a-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="2096a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2096a-130">NOTES</span></span>

## <span data-ttu-id="2096a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2096a-131">RELATED LINKS</span></span>

[<span data-ttu-id="2096a-132">Get-Azdatalakeçözümlerken</span><span class="sxs-lookup"><span data-stu-id="2096a-132">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="2096a-133">Stop-Azdatalakeanaliz Ticsjob</span><span class="sxs-lookup"><span data-stu-id="2096a-133">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="2096a-134">Submit-Azdatalakeanaliz Ticsjob</span><span class="sxs-lookup"><span data-stu-id="2096a-134">Submit-AzDataLakeAnalyticsJob</span></span>](./Submit-AzDataLakeAnalyticsJob.md)

