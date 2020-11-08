---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0DB9595A-6C8B-4F3F-A707-2DB41D7C7470
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/submit-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Submit-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 2fcd30c523508620d7d7ed20ebce60facc2678a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107861"
---
# <span data-ttu-id="8c14d-101">Submit-AzDataLakeAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="8c14d-101">Submit-AzDataLakeAnalyticsJob</span></span>

## <span data-ttu-id="8c14d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c14d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c14d-103">İş gönderir.</span><span class="sxs-lookup"><span data-stu-id="8c14d-103">Submits a job.</span></span>

## <span data-ttu-id="8c14d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c14d-104">SYNTAX</span></span>

### <span data-ttu-id="8c14d-105">Submitusenjobwithscriptpath</span><span class="sxs-lookup"><span data-stu-id="8c14d-105">SubmitUSqlJobWithScriptPath</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c14d-106">Gönderuseniş</span><span class="sxs-lookup"><span data-stu-id="8c14d-106">SubmitUSqlJob</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c14d-107">Submitustojobwithscriptpathandyinelenme</span><span class="sxs-lookup"><span data-stu-id="8c14d-107">SubmitUSqlJobWithScriptPathAndRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c14d-108">Gönderustojobwithyinelenme</span><span class="sxs-lookup"><span data-stu-id="8c14d-108">SubmitUSqlJobWithRecurrence</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c14d-109">Submitusenjobwithscriptpathandpipeline</span><span class="sxs-lookup"><span data-stu-id="8c14d-109">SubmitUSqlJobWithScriptPathAndPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-ScriptPath] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c14d-110">Submitusenjobwithpipeline</span><span class="sxs-lookup"><span data-stu-id="8c14d-110">SubmitUSqlJobWithPipeline</span></span>
```
Submit-AzDataLakeAnalyticsJob [-Account] <String> [-Name] <String> [-Script] <String> [[-Runtime] <String>]
 [[-CompileMode] <String>] [-CompileOnly] [[-AnalyticsUnits] <Int32>] [[-Priority] <Int32>]
 [-ScriptParameter <IDictionary>] -RecurrenceId <Guid> [-RecurrenceName <String>] -PipelineId <Guid>
 [-PipelineName <String>] [-PipelineUri <String>] [-RunId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c14d-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c14d-111">DESCRIPTION</span></span>
<span data-ttu-id="8c14d-112">**Submit-Azdatalakeanalizleri Ticsjob** cmdlet 'ı bir Azure Data Lake Analytics işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="8c14d-112">The **Submit-AzDataLakeAnalyticsJob** cmdlet submits an Azure Data Lake Analytics job.</span></span>

## <span data-ttu-id="8c14d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c14d-113">EXAMPLES</span></span>

### <span data-ttu-id="8c14d-114">Örnek 1: iş gönderme</span><span class="sxs-lookup"><span data-stu-id="8c14d-114">Example 1: Submit a job</span></span>
```
PS C:\>Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32
```

<span data-ttu-id="8c14d-115">Bu komut bir Data Lake Analytics işi gönderir.</span><span class="sxs-lookup"><span data-stu-id="8c14d-115">This command submits a Data Lake Analytics job.</span></span>

### <span data-ttu-id="8c14d-116">Örnek 2: betik parametreleriyle bir iş gönderme</span><span class="sxs-lookup"><span data-stu-id="8c14d-116">Example 2: Submit a job with script parameters</span></span>
```
PS C:\>$parameters = [ordered]@{}
$parameters["Department"] = "Sales"
$parameters["NumRecords"] = 1000
$parameters["StartDateTime"] = (Get-Date).AddDays(-14)
Submit-AzDataLakeAnalyticsJob -Account "ContosoAdlAccount" -Name "New Job" -ScriptPath $LocalScriptPath -AnalyticsUnits 32 -ScriptParameter $parameters
```

<span data-ttu-id="8c14d-117">U-SQL komut dosyası parametreleri ana kod içeriğinin önüne alınır; örneğin: @Department String = "Satışlar"; @NumRecords Int = 1000; DECLARE @StartDateTime = New DateTime (2017, 12, 6, 0, 0, 0, 0);</span><span class="sxs-lookup"><span data-stu-id="8c14d-117">U-SQL script parameters are prepended above the main script contents, e.g.: DECLARE @Department string = "Sales"; DECLARE @NumRecords int = 1000; DECLARE @StartDateTime DateTime = new DateTime(2017, 12, 6, 0, 0, 0, 0);</span></span>

## <span data-ttu-id="8c14d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c14d-118">PARAMETERS</span></span>

### <span data-ttu-id="8c14d-119">-Hesap</span><span class="sxs-lookup"><span data-stu-id="8c14d-119">-Account</span></span>
<span data-ttu-id="8c14d-120">İşin altında gönderildiği veri Lake Analytics hesabının adı.</span><span class="sxs-lookup"><span data-stu-id="8c14d-120">Name of Data Lake Analytics account under which the job will be submitted.</span></span>

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

### <span data-ttu-id="8c14d-121">-Çözümlemesi</span><span class="sxs-lookup"><span data-stu-id="8c14d-121">-AnalyticsUnits</span></span>
<span data-ttu-id="8c14d-122">Bu iş için kullanılacak analitik birimleri.</span><span class="sxs-lookup"><span data-stu-id="8c14d-122">The analytics units to use for this job.</span></span> <span data-ttu-id="8c14d-123">Genellikle, daha hızlı betik yürütme zamanına sahip bir komut dosyası sonuçlarına daha fazla analitik birimi tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="8c14d-123">Typically, more analytics units dedicated to a script results in faster script execution time.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: DegreeOfParallelism

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-124">-CompileMode</span><span class="sxs-lookup"><span data-stu-id="8c14d-124">-CompileMode</span></span>
<span data-ttu-id="8c14d-125">Bu işte yapılacak derleme türü.</span><span class="sxs-lookup"><span data-stu-id="8c14d-125">The type of compilation to be done on this job.</span></span> <span data-ttu-id="8c14d-126">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8c14d-126">Valid values:</span></span> 
- <span data-ttu-id="8c14d-127">Anlam (yalnızca anlamlı denetimler ve gerekli sağlamlık denetimleri gerçekleştirir)</span><span class="sxs-lookup"><span data-stu-id="8c14d-127">Semantic (Only performs semantic checks and necessary sanity checks)</span></span>
- <span data-ttu-id="8c14d-128">Tam (tam derleme)</span><span class="sxs-lookup"><span data-stu-id="8c14d-128">Full (Full compilation)</span></span>
- <span data-ttu-id="8c14d-129">SingleBox (tam derleme yerel olarak gerçekleştirildi)</span><span class="sxs-lookup"><span data-stu-id="8c14d-129">SingleBox (Full compilation performed locally)</span></span>

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

### <span data-ttu-id="8c14d-130">-Yalnızca</span><span class="sxs-lookup"><span data-stu-id="8c14d-130">-CompileOnly</span></span>
<span data-ttu-id="8c14d-131">Gönderimin yalnızca işi oluşturması gerektiğini ve true olarak ayarlanmış olması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8c14d-131">Indicates that the submission should only build the job and not execute if set to true.</span></span>

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

### <span data-ttu-id="8c14d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c14d-132">-DefaultProfile</span></span>
<span data-ttu-id="8c14d-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8c14d-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c14d-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="8c14d-134">-Name</span></span>
<span data-ttu-id="8c14d-135">Gönderecek işin kolay adı.</span><span class="sxs-lookup"><span data-stu-id="8c14d-135">The friendly name of the job to submit.</span></span>

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

### <span data-ttu-id="8c14d-136">-Pipelineıd</span><span class="sxs-lookup"><span data-stu-id="8c14d-136">-PipelineId</span></span>
<span data-ttu-id="8c14d-137">Bu işin gönderimini gösteren bir KIMLIK, yinelenen bir iş kümesinin bir bölümüdür ve bir proje ardışık düzenine ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="8c14d-137">An ID that indicates the submission of this job is a part of a set of recurring jobs and also associated with a job pipeline.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-138">-Ardışık Düzen adı</span><span class="sxs-lookup"><span data-stu-id="8c14d-138">-PipelineName</span></span>
<span data-ttu-id="8c14d-139">Bu işle ilişkilendirilmiş potansiyel satış için isteğe bağlı bir kolay ad.</span><span class="sxs-lookup"><span data-stu-id="8c14d-139">An optional friendly name for the pipeline associated with this job.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-140">-PipelineUri</span><span class="sxs-lookup"><span data-stu-id="8c14d-140">-PipelineUri</span></span>
<span data-ttu-id="8c14d-141">Bu ardışık düzene ilişkin kaynak hizmete bağlanan isteğe bağlı bir URI.</span><span class="sxs-lookup"><span data-stu-id="8c14d-141">An optional uri that links to the originating service associated with this pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-142">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="8c14d-142">-Priority</span></span>
<span data-ttu-id="8c14d-143">İşin önceliği.</span><span class="sxs-lookup"><span data-stu-id="8c14d-143">The priority of the job.</span></span> <span data-ttu-id="8c14d-144">Belirtilmemişse, öncelik 1000.</span><span class="sxs-lookup"><span data-stu-id="8c14d-144">If not specified, the priority is 1000.</span></span> <span data-ttu-id="8c14d-145">Küçük bir sayı, daha yüksek bir iş önceliği gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c14d-145">A lower number indicates a higher job priority.</span></span>

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

### <span data-ttu-id="8c14d-146">-RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="8c14d-146">-RecurrenceId</span></span>
<span data-ttu-id="8c14d-147">Bu işin gönderimini gösteren bir KIMLIK, aynı yinelenme KIMLIĞINE sahip bir yinelenen iş kümesinin parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="8c14d-147">An ID that indicates the submission of this job is a part of a set of recurring jobs with the same recurrence ID.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-148">-RecurrenceName</span><span class="sxs-lookup"><span data-stu-id="8c14d-148">-RecurrenceName</span></span>
<span data-ttu-id="8c14d-149">İşler arasındaki yinelenme bağıntısı için isteğe bağlı bir kolay ad.</span><span class="sxs-lookup"><span data-stu-id="8c14d-149">An optional friendly name for the recurrence correlation between jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-150">-RunId</span><span class="sxs-lookup"><span data-stu-id="8c14d-150">-RunId</span></span>
<span data-ttu-id="8c14d-151">Ardışık düzenin bu belirli çalışma yinelemesini tanımlayan bir KIMLIK.</span><span class="sxs-lookup"><span data-stu-id="8c14d-151">An ID that identifies this specific run iteration of the pipeline.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubmitUSqlJobWithScriptPathAndPipeline, SubmitUSqlJobWithPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-152">-Runtime</span><span class="sxs-lookup"><span data-stu-id="8c14d-152">-Runtime</span></span>
<span data-ttu-id="8c14d-153">İsteğe bağlı olarak, iş için kullanılacak çalışma zamanının sürümünü ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8c14d-153">Optionally set the version of the runtime to use for the job.</span></span> <span data-ttu-id="8c14d-154">Ayarlandığında, varsayılan çalışma zamanı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8c14d-154">If left unset, the default runtime is used.</span></span>

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

### <span data-ttu-id="8c14d-155">-Betik</span><span class="sxs-lookup"><span data-stu-id="8c14d-155">-Script</span></span>
<span data-ttu-id="8c14d-156">Yürütülecek komut dosyası (satır içi).</span><span class="sxs-lookup"><span data-stu-id="8c14d-156">Script to execute (written inline).</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJob, SubmitUSqlJobWithRecurrence, SubmitUSqlJobWithPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-157">-ScriptParameter</span><span class="sxs-lookup"><span data-stu-id="8c14d-157">-ScriptParameter</span></span>
<span data-ttu-id="8c14d-158">Bu işin komut dosyası parametreleri, parametre adlarının (dize) değerlere (Byte, SByte, int, uint (veya uint32), Long, ulong (veya uint64), float, Double, Decimal, Short (veya int16), ushort (veya UInt16), Char, String, DateTime, bool, Guid veya Byte []).</span><span class="sxs-lookup"><span data-stu-id="8c14d-158">The script parameters for this job, as a dictionary of parameter names (string) to values (any combination of byte, sbyte, int, uint (or uint32), long, ulong (or uint64), float, double, decimal, short (or int16), ushort (or uint16), char, string, DateTime, bool, Guid, or byte[]).</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-159">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="8c14d-159">-ScriptPath</span></span>
<span data-ttu-id="8c14d-160">Gönderecek komut dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="8c14d-160">Path to the script file to submit.</span></span>

```yaml
Type: System.String
Parameter Sets: SubmitUSqlJobWithScriptPath, SubmitUSqlJobWithScriptPathAndRecurrence, SubmitUSqlJobWithScriptPathAndPipeline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c14d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c14d-161">CommonParameters</span></span>
<span data-ttu-id="8c14d-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c14d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c14d-163">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c14d-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c14d-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c14d-164">INPUTS</span></span>

### <span data-ttu-id="8c14d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="8c14d-165">System.String</span></span>

### <span data-ttu-id="8c14d-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c14d-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8c14d-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8c14d-167">System.Int32</span></span>

### <span data-ttu-id="8c14d-168">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="8c14d-168">System.Collections.IDictionary</span></span>

### <span data-ttu-id="8c14d-169">System. Guid</span><span class="sxs-lookup"><span data-stu-id="8c14d-169">System.Guid</span></span>

### <span data-ttu-id="8c14d-170">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="8c14d-170">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8c14d-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c14d-171">OUTPUTS</span></span>

### <span data-ttu-id="8c14d-172">Microsoft. Azure. Management. DataLake. Analytics. modeller. Jobınformation</span><span class="sxs-lookup"><span data-stu-id="8c14d-172">Microsoft.Azure.Management.DataLake.Analytics.Models.JobInformation</span></span>

## <span data-ttu-id="8c14d-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c14d-173">NOTES</span></span>

## <span data-ttu-id="8c14d-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c14d-174">RELATED LINKS</span></span>

[<span data-ttu-id="8c14d-175">Get-Azdatalakeçözümlerken</span><span class="sxs-lookup"><span data-stu-id="8c14d-175">Get-AzDataLakeAnalyticsJob</span></span>](./Get-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8c14d-176">Stop-Azdatalakeanaliz Ticsjob</span><span class="sxs-lookup"><span data-stu-id="8c14d-176">Stop-AzDataLakeAnalyticsJob</span></span>](./Stop-AzDataLakeAnalyticsJob.md)

[<span data-ttu-id="8c14d-177">Wait-Azdatalakeanalyzer</span><span class="sxs-lookup"><span data-stu-id="8c14d-177">Wait-AzDataLakeAnalyticsJob</span></span>](./Wait-AzDataLakeAnalyticsJob.md)


