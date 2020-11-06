---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Submit-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: bb0ad536d738facdfe50bc7983517f4505ab4ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592236"
---
# <span data-ttu-id="b5ff0-101">Submit-AzureRmDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="b5ff0-101">Submit-AzureRmDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="b5ff0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ff0-103">İş gönderir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-103">Submits a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5ff0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5ff0-104">SYNTAX</span></span>

### <span data-ttu-id="b5ff0-105">U-SQL için komut dosyası yoluyla iş gönderme işi</span><span class="sxs-lookup"><span data-stu-id="b5ff0-105">Submit job with script path for U-SQL</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ff0-106">E-SQL Işi gönderme</span><span class="sxs-lookup"><span data-stu-id="b5ff0-106">Submit U-SQL Job</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ff0-107">Reugeçerlice bilgileriyle U-SQL için komut dosyası yoluyla iş gönderme işi</span><span class="sxs-lookup"><span data-stu-id="b5ff0-107">Submit job with script path for U-SQL with reucurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ff0-108">Yineleme bilgileriyle U-SQL Işi gönderme</span><span class="sxs-lookup"><span data-stu-id="b5ff0-108">Submit U-SQL Job with recurrence information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ff0-109">Reugeçerlice ve boru hattı bilgileriyle U-SQL için komut dosyası yoluyla iş gönderme işi</span><span class="sxs-lookup"><span data-stu-id="b5ff0-109">Submit job with script path for U-SQL with reucurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5ff0-110">Yineleme ve kanal bilgileriyle U-SQL Işi gönderin</span><span class="sxs-lookup"><span data-stu-id="b5ff0-110">Submit U-SQL Job with recurrence and pipeline information</span></span>
```
Submit-AzureRmDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String>
 [[-Runtime] <String>] [[-CompileMode] <String>] [-CompileOnly] [[-DegreeOfParallelism] <Int32>]
 [[-Priority] <Int32>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5ff0-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5ff0-111">DESCRIPTION</span></span>
<span data-ttu-id="b5ff0-112">**Submit-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-112">The **Submit-AzureRmDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="b5ff0-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5ff0-113">EXAMPLES</span></span>

### <span data-ttu-id="b5ff0-114">Örnek 1: iş gönderme</span><span class="sxs-lookup"><span data-stu-id="b5ff0-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -DegreeOfParallelism 32
```

<span data-ttu-id="b5ff0-115">Bu komut bir Data Lake Analytics işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-115">This command submits a Data Lake Analytics job.</span></span>

## <span data-ttu-id="b5ff0-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5ff0-116">PARAMETERS</span></span>

### <span data-ttu-id="b5ff0-117">-Hesap</span><span class="sxs-lookup"><span data-stu-id="b5ff0-117">-Account</span></span>
<span data-ttu-id="b5ff0-118">Data Lake Analytics hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="b5ff0-119">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="b5ff0-119">-CompileMode</span></span>
<span data-ttu-id="b5ff0-120">İşin derleme modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-120">Specifies the compilation mode of the job.</span></span>
<span data-ttu-id="b5ff0-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b5ff0-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5ff0-122">Anlambilim</span><span class="sxs-lookup"><span data-stu-id="b5ff0-122">Semantic</span></span>
- <span data-ttu-id="b5ff0-123">Dolduğunda</span><span class="sxs-lookup"><span data-stu-id="b5ff0-123">Full</span></span>
- <span data-ttu-id="b5ff0-124">SingleBox</span><span class="sxs-lookup"><span data-stu-id="b5ff0-124">SingleBox</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Semantic, Full, SingleBox

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-125">-Yalnızca</span><span class="sxs-lookup"><span data-stu-id="b5ff0-125">-CompileOnly</span></span>
<span data-ttu-id="b5ff0-126">Bu cmdlet 'in işi çalıştırmadan derlendiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-126">Indicates that this cmdlet compiles the job without running it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-127">-Degreeofparalellizm</span><span class="sxs-lookup"><span data-stu-id="b5ff0-127">-DegreeOfParallelism</span></span>
<span data-ttu-id="b5ff0-128">İşin, izin verilen en fazla paralellik miktarını gösteren, işin veri Lake Analytics birimlerini (VSEÇLAU) belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-128">Specifies the Data Lake Analytics Units (DLAU) of the job, which indicates the maximum allowable parallelism of the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5ff0-129">-Name</span></span>
<span data-ttu-id="b5ff0-130">İş adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-130">Specifies the job name.</span></span>

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

### <span data-ttu-id="b5ff0-131">-Pipelineıd</span><span class="sxs-lookup"><span data-stu-id="b5ff0-131">-PipelineId</span></span>
<span data-ttu-id="b5ff0-132">Bu işin gönderimini gösteren bir KIMLIK, yinelenen bir iş kümesinin bir bölümüdür ve bir proje ardışık düzenine ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-132">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-133">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="b5ff0-133">-PipelineName</span></span>
<span data-ttu-id="b5ff0-134">Bu işle ilişkilendirilmiş potansiyel satış için isteğe bağlı bir kolay ad.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-134">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-135">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="b5ff0-135">-PipelineUri</span></span>
<span data-ttu-id="b5ff0-136">Bu ardışık düzene ilişkin kaynak hizmete bağlanan isteğe bağlı bir URI.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-136">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-137">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="b5ff0-137">-Priority</span></span>
<span data-ttu-id="b5ff0-138">İşin önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-138">Specifies the priority of the job.</span></span>
<span data-ttu-id="b5ff0-139">Belirtilmemişse, öncelik 1000.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-139">If not specified, the priority is 1000.</span></span>
<span data-ttu-id="b5ff0-140">Düşük bir sayı, daha yüksek bir iş önceliği gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-140">A low number indicates a higher job priority.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-141">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="b5ff0-141">-RecurrenceId</span></span>
<span data-ttu-id="b5ff0-142">Bu işin gönderimini gösteren bir KIMLIK, aynı yinelenme KIMLIĞINE sahip bir yinelenen iş kümesinin parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-142">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-143">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="b5ff0-143">-RecurrenceName</span></span>
<span data-ttu-id="b5ff0-144">İşler arasındaki yinelenme bağıntısı için isteğe bağlı bir kolay ad.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-144">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL with reucurrence information, Submit U-SQL Job with recurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-145">-RunId</span><span class="sxs-lookup"><span data-stu-id="b5ff0-145">-RunId</span></span>
<span data-ttu-id="b5ff0-146">Ardışık düzenin bu belirli çalışma yinelemesini tanımlayan bir KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-146">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: Submit job with script path for U-SQL with reucurrence and pipeline information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-147">-Runtime</span><span class="sxs-lookup"><span data-stu-id="b5ff0-147">-Runtime</span></span>
<span data-ttu-id="b5ff0-148">İşin çalışma zamanı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-148">Specifies the runtime version of the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-149">-Betik</span><span class="sxs-lookup"><span data-stu-id="b5ff0-149">-Script</span></span>
<span data-ttu-id="b5ff0-150">Çalıştırılacak komut dosyasının içeriğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-150">Specifies the contents of the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit U-SQL Job, Submit U-SQL Job with recurrence information, Submit U-SQL Job with recurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-151">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="b5ff0-151">-ScriptPath</span></span>
<span data-ttu-id="b5ff0-152">Komut dosyasının çalıştırılacağı yerel dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-152">Specifies the local file path to the script to run.</span></span>

```yaml
Type: System.String
Parameter Sets: Submit job with script path for U-SQL, Submit job with script path for U-SQL with reucurrence information, Submit job with script path for U-SQL with reucurrence and pipeline information
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ff0-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ff0-153">-DefaultProfile</span></span>
<span data-ttu-id="b5ff0-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5ff0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ff0-155">CommonParameters</span></span>
<span data-ttu-id="b5ff0-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ff0-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ff0-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ff0-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5ff0-158">INPUTS</span></span>

### <span data-ttu-id="b5ff0-159">Dizisi</span><span class="sxs-lookup"><span data-stu-id="b5ff0-159">String</span></span>
<span data-ttu-id="b5ff0-160">' SCRIPT ' parametresi ardışık düzenin ' String ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b5ff0-160">Parameter 'Script' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="b5ff0-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5ff0-161">OUTPUTS</span></span>

### <span data-ttu-id="b5ff0-162">Jobınformation</span><span class="sxs-lookup"><span data-stu-id="b5ff0-162">JobInformation</span></span>
<span data-ttu-id="b5ff0-163">Gönderilen iş için başlangıç iş ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="b5ff0-163">The initial job details for the submitted job.</span></span>

## <span data-ttu-id="b5ff0-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5ff0-164">NOTES</span></span>

## <span data-ttu-id="b5ff0-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5ff0-165">RELATED LINKS</span></span>

[<span data-ttu-id="b5ff0-166">Get-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="b5ff0-166">Get-AzureRmDataLakeAnalyticsJob</span></span>](./Get-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="b5ff0-167">Stop-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="b5ff0-167">Stop-AzureRmDataLakeAnalyticsJob</span></span>](./Stop-AzureRmDataLakeAnalyticsJob.md)

[<span data-ttu-id="b5ff0-168">Wait-Azurermdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="b5ff0-168">Wait-AzureRmDataLakeAnalyticsJob</span></span>](./Wait-AzureRmDataLakeAnalyticsJob.md)


