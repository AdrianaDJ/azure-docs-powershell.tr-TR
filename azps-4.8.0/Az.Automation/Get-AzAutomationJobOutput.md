---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110089"
---
# <span data-ttu-id="c1f7d-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c1f7d-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="c1f7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f7d-103">Otomasyon işinin çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="c1f7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c1f7d-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1f7d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c1f7d-105">DESCRIPTION</span></span>
<span data-ttu-id="c1f7d-106">**Get-Azautomationjoi Input** cmdlet 'ı bir Azure Otomasyonu işinin çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="c1f7d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c1f7d-107">EXAMPLES</span></span>

### <span data-ttu-id="c1f7d-108">Örnek 1: Otomasyon işinin çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="c1f7d-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="c1f7d-109">Bu komut, işin belirtilen KIMLIĞINE sahip olan tüm çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="c1f7d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c1f7d-110">PARAMETERS</span></span>

### <span data-ttu-id="c1f7d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c1f7d-111">-AutomationAccountName</span></span>
<span data-ttu-id="c1f7d-112">Bu cmdlet 'in iş çıktısını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="c1f7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f7d-113">-DefaultProfile</span></span>
<span data-ttu-id="c1f7d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c1f7d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1f7d-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c1f7d-115">-Id</span></span>
<span data-ttu-id="c1f7d-116">Bu cmdlet 'in çıkış aldığı iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f7d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f7d-117">-ResourceGroupName</span></span>
<span data-ttu-id="c1f7d-118">Bu cmdlet 'in iş çıktısını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="c1f7d-119">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="c1f7d-119">-StartTime</span></span>
<span data-ttu-id="c1f7d-120">Bir başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c1f7d-121">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="c1f7d-122">Cmdlet bu saatten sonra oluşturulan çıktıyı alır.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="c1f7d-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="c1f7d-123">-Stream</span></span>
<span data-ttu-id="c1f7d-124">Çıktının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-124">Specifies the type of output.</span></span>
<span data-ttu-id="c1f7d-125">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="c1f7d-125">Valid values are:</span></span> 
- <span data-ttu-id="c1f7d-126">Tüm</span><span class="sxs-lookup"><span data-stu-id="c1f7d-126">Any</span></span>
- <span data-ttu-id="c1f7d-127">Hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="c1f7d-127">Debug</span></span>
- <span data-ttu-id="c1f7d-128">Hatalar</span><span class="sxs-lookup"><span data-stu-id="c1f7d-128">Error</span></span>
- <span data-ttu-id="c1f7d-129">Çıkışının</span><span class="sxs-lookup"><span data-stu-id="c1f7d-129">Output</span></span>
- <span data-ttu-id="c1f7d-130">Sürdüğü</span><span class="sxs-lookup"><span data-stu-id="c1f7d-130">Progress</span></span>
- <span data-ttu-id="c1f7d-131">Kapsamlı</span><span class="sxs-lookup"><span data-stu-id="c1f7d-131">Verbose</span></span>
- <span data-ttu-id="c1f7d-132">Uyarılarla</span><span class="sxs-lookup"><span data-stu-id="c1f7d-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1f7d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f7d-133">CommonParameters</span></span>
<span data-ttu-id="c1f7d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c1f7d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f7d-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1f7d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f7d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c1f7d-136">INPUTS</span></span>

### <span data-ttu-id="c1f7d-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c1f7d-137">System.Guid</span></span>

### <span data-ttu-id="c1f7d-138">Microsoft. Azure. Commands. Automation. Common. StreamType</span><span class="sxs-lookup"><span data-stu-id="c1f7d-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="c1f7d-139">System. Nullable ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="c1f7d-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c1f7d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c1f7d-140">System.String</span></span>

## <span data-ttu-id="c1f7d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c1f7d-141">OUTPUTS</span></span>

### <span data-ttu-id="c1f7d-142">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="c1f7d-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="c1f7d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c1f7d-143">NOTES</span></span>

## <span data-ttu-id="c1f7d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c1f7d-144">RELATED LINKS</span></span>

[<span data-ttu-id="c1f7d-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c1f7d-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="c1f7d-146">Özgeçmiş-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c1f7d-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="c1f7d-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c1f7d-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="c1f7d-148">Askıya alma-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c1f7d-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


