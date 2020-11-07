---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsjobrecurrence
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsJobRecurrence.md
ms.openlocfilehash: d0430b283f122b5da41392a04fc9827bc03e3082
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763868"
---
# <span data-ttu-id="908d1-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span><span class="sxs-lookup"><span data-stu-id="908d1-101">Get-AzureRmDataLakeAnalyticsJobRecurrence</span></span>

## <span data-ttu-id="908d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="908d1-102">SYNOPSIS</span></span>
<span data-ttu-id="908d1-103">Veri Lake Analytics Iş yinelemesi veya yinelenmeleri alır.</span><span class="sxs-lookup"><span data-stu-id="908d1-103">Gets a Data Lake Analytics Job recurrence or recurrences.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="908d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="908d1-104">SYNTAX</span></span>

### <span data-ttu-id="908d1-105">GetAllInAccount (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="908d1-105">GetAllInAccount (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-SubmittedAfter <DateTimeOffset>]
 [-SubmittedBefore <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="908d1-106">Getbyspecificjobyinelenme</span><span class="sxs-lookup"><span data-stu-id="908d1-106">GetBySpecificJobRecurrence</span></span>
```
Get-AzureRmDataLakeAnalyticsJobRecurrence [-Account] <String> [-RecurrenceId] <Guid>
 [-SubmittedAfter <DateTimeOffset>] [-SubmittedBefore <DateTimeOffset>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="908d1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="908d1-107">DESCRIPTION</span></span>
<span data-ttu-id="908d1-108">**Get-Azurermdatalakeanalyzer** , belirli bir Azure Data Lake Analytics iş yinelemesini veya yinelenme listesini alır.</span><span class="sxs-lookup"><span data-stu-id="908d1-108">The **Get-AzureRmDataLakeAnalyticsJobRecurrence** gets a specified Azure Data Lake Analytics Job recurrence or a list of recurrence.</span></span>

## <span data-ttu-id="908d1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="908d1-109">EXAMPLES</span></span>

### <span data-ttu-id="908d1-110">Örnek 1: belirli bir yinelenme alma</span><span class="sxs-lookup"><span data-stu-id="908d1-110">Example 1: Get a specified recurrence</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -Account "contosoadla" -RecurrenceId 83cb7ad2-3523-4b82-b909-d478b0d8aea3
```

<span data-ttu-id="908d1-111">Bu komut, ' contosoadla ' hesabında kimliği ' 83cb7ad2-3523-4b82-b909-vseç478b0vseç8aea3 ' olan belirtilen iş yinelemesini alır.</span><span class="sxs-lookup"><span data-stu-id="908d1-111">This command gets the specified job recurrence with id '83cb7ad2-3523-4b82-b909-d478b0d8aea3' in account 'contosoadla'.</span></span>

### <span data-ttu-id="908d1-112">Örnek 2: hesaptaki tüm yinelenmeleri listesini alma</span><span class="sxs-lookup"><span data-stu-id="908d1-112">Example 2: Get a list of all recurrences in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsJobRecurrence -AccountName "contosoadla"
```

<span data-ttu-id="908d1-113">Bu komut, "contosoadla" hesabındaki tüm Yinelenmeler listesini alır</span><span class="sxs-lookup"><span data-stu-id="908d1-113">This command gets a list of all recurrences in the account "contosoadla"</span></span>

## <span data-ttu-id="908d1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="908d1-114">PARAMETERS</span></span>

### <span data-ttu-id="908d1-115">-Hesap</span><span class="sxs-lookup"><span data-stu-id="908d1-115">-Account</span></span>
<span data-ttu-id="908d1-116">İş tekrarını almak istediğiniz veri Lake Analytics hesap adının adı.</span><span class="sxs-lookup"><span data-stu-id="908d1-116">Name of the Data Lake Analytics account name under which want to retrieve the job recurrence.</span></span>

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

### <span data-ttu-id="908d1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908d1-117">-DefaultProfile</span></span>
<span data-ttu-id="908d1-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="908d1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="908d1-119">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="908d1-119">-RecurrenceId</span></span>
<span data-ttu-id="908d1-120">Bilgilerin geri döndürülmesi için belirli iş tekrarının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="908d1-120">ID of the specific job recurrence to return information for.</span></span>

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

### <span data-ttu-id="908d1-121">-SubmittedAfter</span><span class="sxs-lookup"><span data-stu-id="908d1-121">-SubmittedAfter</span></span>
<span data-ttu-id="908d1-122">Yalnızca belirtilen süreden sonra gönderilen iş tekrarını döndüren bir isteğe bağlı filtre.</span><span class="sxs-lookup"><span data-stu-id="908d1-122">An optional filter which returns job recurrence(s) only submitted after the specified time.</span></span>

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

### <span data-ttu-id="908d1-123">-Submittedbir</span><span class="sxs-lookup"><span data-stu-id="908d1-123">-SubmittedBefore</span></span>
<span data-ttu-id="908d1-124">Yalnızca belirtilen süreden önce gönderilen iş tekrarını döndüren bir isteğe bağlı filtre.</span><span class="sxs-lookup"><span data-stu-id="908d1-124">An optional filter which returns job recurrence(s) only submitted before the specified time.</span></span>

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

### <span data-ttu-id="908d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908d1-125">CommonParameters</span></span>
<span data-ttu-id="908d1-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="908d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908d1-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="908d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908d1-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="908d1-128">INPUTS</span></span>

### <span data-ttu-id="908d1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="908d1-129">System.String</span></span>

### <span data-ttu-id="908d1-130">System. Guid</span><span class="sxs-lookup"><span data-stu-id="908d1-130">System.Guid</span></span>

### <span data-ttu-id="908d1-131">System. Nullable ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="908d1-131">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="908d1-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="908d1-132">OUTPUTS</span></span>

### <span data-ttu-id="908d1-133">Microsoft. Azure. Commands. DataLakeAnalytics. model. Psjobrecurrenceınformation</span><span class="sxs-lookup"><span data-stu-id="908d1-133">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSJobRecurrenceInformation</span></span>

## <span data-ttu-id="908d1-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="908d1-134">NOTES</span></span>

## <span data-ttu-id="908d1-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="908d1-135">RELATED LINKS</span></span>