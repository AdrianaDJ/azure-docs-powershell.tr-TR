---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d571eb887069aa5c28029dfa98ab022c1d82fc88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096324"
---
# <span data-ttu-id="e54e2-101">Get-AzDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="e54e2-101">Get-AzDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="e54e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e54e2-102">SYNOPSIS</span></span>
<span data-ttu-id="e54e2-103">Veri Lake Analytics Iş yinelemesi veya yinelenmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="e54e2-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

## <span data-ttu-id="e54e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e54e2-104">SYNTAX</span></span>

### <span data-ttu-id="e54e2-105">GetAllInAccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e54e2-105">GetAllInAccount (Default)</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e54e2-106">Getbyspecificjobyinelenme</span><span class="sxs-lookup"><span data-stu-id="e54e2-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e54e2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e54e2-107">DESCRIPTION</span></span>
<span data-ttu-id="e54e2-108">**Get-Azdatalakeçözümlerken** , belirli bir Azure Data Lake Analytics iş yinelemesini veya yinelenme listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e54e2-108">The **Get-AzDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="e54e2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e54e2-109">EXAMPLES</span></span>

### <span data-ttu-id="e54e2-110">Örnek 1: belirli bir yinelenme alma</span><span class="sxs-lookup"><span data-stu-id="e54e2-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="e54e2-111">Bu komut, ' contosoadla ' hesabında kimliği ' 83cb7ad2-3523-4b82-b909-vseç478b0vseç8aea3 ' olan belirtilen iş yinelemesini alır.</span><span class="sxs-lookup"><span data-stu-id="e54e2-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="e54e2-112">Örnek 2: hesaptaki tüm yinelenmeleri listesini alma</span><span class="sxs-lookup"><span data-stu-id="e54e2-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="e54e2-113">Bu komut, "contosoadla" hesabındaki tüm Yinelenmeler listesini alır</span><span class="sxs-lookup"><span data-stu-id="e54e2-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="e54e2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e54e2-114">PARAMETERS</span></span>

### <span data-ttu-id="e54e2-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="e54e2-115">-Account</span></span>
<span data-ttu-id="e54e2-116">İş tekrarını almak istediğiniz veri Lake Analytics hesap adının adı.</span><span class="sxs-lookup"><span data-stu-id="e54e2-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="e54e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e54e2-117">-DefaultProfile</span></span>
<span data-ttu-id="e54e2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e54e2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e54e2-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="e54e2-119">-RecurrenceId</span></span>
<span data-ttu-id="e54e2-120">Bilgilerin geri döndürülmesi için belirli iş tekrarının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e54e2-120">ID of the specific job recurrence to return information for.</span></span>

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobRecurrence
Aliases: Id

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e2-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="e54e2-121">-SubmittedAfter</span></span>
<span data-ttu-id="e54e2-122">Yalnızca belirtilen süreden sonra gönderilen iş tekrarını döndüren bir isteğe bağlı filtre.</span><span class="sxs-lookup"><span data-stu-id="e54e2-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e2-123">-Submittedbir</span><span class="sxs-lookup"><span data-stu-id="e54e2-123">-SubmittedBefore</span></span>
<span data-ttu-id="e54e2-124">Yalnızca belirtilen süreden önce gönderilen iş tekrarını döndüren bir isteğe bağlı filtre.</span><span class="sxs-lookup"><span data-stu-id="e54e2-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e54e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54e2-125">CommonParameters</span></span>
<span data-ttu-id="e54e2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e54e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54e2-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e54e2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54e2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e54e2-128">INPUTS</span></span>

### <span data-ttu-id="e54e2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e54e2-129">System.String</span></span>

### <span data-ttu-id="e54e2-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="e54e2-130">System.Guid</span></span>

### <span data-ttu-id="e54e2-131">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e54e2-131">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e54e2-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e54e2-132">OUTPUTS</span></span>

### <span data-ttu-id="e54e2-133">Microsoft. Azure. Commands. DataLakeAnalytics. model. Psjobrecurrenceınformation</span><span class="sxs-lookup"><span data-stu-id="e54e2-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="e54e2-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e54e2-134">NOTES</span></span>

## <span data-ttu-id="e54e2-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e54e2-135">RELATED LINKS</span></span>
