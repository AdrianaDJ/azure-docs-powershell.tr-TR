---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 302129506c516cd0f2864210d5323b83fb54e0df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762960"
---
# <span data-ttu-id="dd883-101">Wait-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="dd883-101">Wait-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="dd883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd883-102">SYNOPSIS</span></span>
<span data-ttu-id="dd883-103">İşin tamamlanmasını bekler.</span><span class="sxs-lookup"><span data-stu-id="dd883-103">Waits for a job to complete.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd883-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd883-104">SYNTAX</span></span>

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd883-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd883-105">DESCRIPTION</span></span>
<span data-ttu-id="dd883-106">**Wait-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics işinin tamamlamasını bekler.</span><span class="sxs-lookup"><span data-stu-id="dd883-106">The **Wait-AzureRmDataLakeAnalyticsJob** cmdlet waits for an Azure Data Lake Analytics job to complete.</span></span>

## <span data-ttu-id="dd883-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd883-107">EXAMPLES</span></span>

### <span data-ttu-id="dd883-108">Örnek 1: işin tamamlanmasını bekle</span><span class="sxs-lookup"><span data-stu-id="dd883-108">Example 1: Wait for a job to complete</span></span>
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

<span data-ttu-id="dd883-109">Aşağıdaki komut belirtilen KIMLIğIN tamamlanma işini bekler.</span><span class="sxs-lookup"><span data-stu-id="dd883-109">The following command waits for the job with the specified ID to complete.</span></span>

## <span data-ttu-id="dd883-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd883-110">PARAMETERS</span></span>

### <span data-ttu-id="dd883-111">-Hesap</span><span class="sxs-lookup"><span data-stu-id="dd883-111">-Account</span></span>
<span data-ttu-id="dd883-112">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd883-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="dd883-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd883-113">-DefaultProfile</span></span>
<span data-ttu-id="dd883-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="dd883-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd883-115">-JobId</span><span class="sxs-lookup"><span data-stu-id="dd883-115">-JobId</span></span>
<span data-ttu-id="dd883-116">Bekleme işinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd883-116">Specifies the ID of the job for which to wait.</span></span>

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

### <span data-ttu-id="dd883-117">-Timeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="dd883-117">-TimeoutInSeconds</span></span>
<span data-ttu-id="dd883-118">Bekleme işleminden çıkmadan önce beklenecek saniye sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd883-118">Specifies the number of seconds to wait before exiting the wait operation.</span></span>

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

### <span data-ttu-id="dd883-119">-Waitıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="dd883-119">-WaitIntervalInSeconds</span></span>
<span data-ttu-id="dd883-120">İş durumu denetimi arasında geçen saniye sayısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="dd883-120">Specify the number of seconds that elapse between each check of the job state.</span></span>

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

### <span data-ttu-id="dd883-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd883-121">CommonParameters</span></span>
<span data-ttu-id="dd883-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd883-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd883-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd883-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd883-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd883-124">INPUTS</span></span>

### <span data-ttu-id="dd883-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dd883-125">System.String</span></span>

### <span data-ttu-id="dd883-126">System. Guid</span><span class="sxs-lookup"><span data-stu-id="dd883-126">System.Guid</span></span>

### <span data-ttu-id="dd883-127">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dd883-127">System.Int32</span></span>

## <span data-ttu-id="dd883-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd883-128">OUTPUTS</span></span>

### <span data-ttu-id="dd883-129">Microsoft. Azure. Management. DataLake. Analytics. modeller. Jobınformation</span><span class="sxs-lookup"><span data-stu-id="dd883-129">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="dd883-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd883-130">NOTES</span></span>

## <span data-ttu-id="dd883-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd883-131">RELATED LINKS</span></span>

[<span data-ttu-id="dd883-132">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="dd883-132">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="dd883-133">Stop-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="dd883-133">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="dd883-134">Submit-Azurermdatalakeanalyzer Ticsjob</span><span class="sxs-lookup"><span data-stu-id="dd883-134">Submit-AzureRmDataLakeAnalyticsJob</span></span>](./Submit-AzureRmDataLakeAnalyticsJob.md)


