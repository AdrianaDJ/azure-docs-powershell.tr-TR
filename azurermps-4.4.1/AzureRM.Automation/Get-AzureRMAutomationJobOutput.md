---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: dd80c745c99c98d6ea5b551ab454661d4370cebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765069"
---
# <span data-ttu-id="112eb-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="112eb-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="112eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="112eb-102">SYNOPSIS</span></span>
<span data-ttu-id="112eb-103">Otomasyon işinin çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="112eb-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="112eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="112eb-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="112eb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="112eb-105">DESCRIPTION</span></span>
<span data-ttu-id="112eb-106">**Get-Azurermautomationjoi Input** cmdlet 'ı bir Azure Otomasyonu işinin çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="112eb-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="112eb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="112eb-107">EXAMPLES</span></span>

### <span data-ttu-id="112eb-108">Örnek 1: Otomasyon işinin çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="112eb-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="112eb-109">Bu komut, işin belirtilen KIMLIĞINE sahip olan tüm çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="112eb-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="112eb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="112eb-110">PARAMETERS</span></span>

### <span data-ttu-id="112eb-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="112eb-111">-AutomationAccountName</span></span>
<span data-ttu-id="112eb-112">Bu cmdlet 'in iş çıktısını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="112eb-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="112eb-113">-ID</span><span class="sxs-lookup"><span data-stu-id="112eb-113">-Id</span></span>
<span data-ttu-id="112eb-114">Bu cmdlet 'in çıkış aldığı iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="112eb-114">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="112eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="112eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="112eb-116">Bu cmdlet 'in iş çıktısını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="112eb-116">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="112eb-117">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="112eb-117">-StartTime</span></span>
<span data-ttu-id="112eb-118">Bir başlangıç saatini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="112eb-118">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="112eb-119">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="112eb-119">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="112eb-120">Cmdlet bu saatten sonra oluşturulan çıktıyı alır.</span><span class="sxs-lookup"><span data-stu-id="112eb-120">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="112eb-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="112eb-121">-Stream</span></span>
<span data-ttu-id="112eb-122">Çıktının türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="112eb-122">Specifies the type of output.</span></span>
<span data-ttu-id="112eb-123">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="112eb-123">Valid values are:</span></span> 

- <span data-ttu-id="112eb-124">Tüm</span><span class="sxs-lookup"><span data-stu-id="112eb-124">Any</span></span>
- <span data-ttu-id="112eb-125">Hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="112eb-125">Debug</span></span>
- <span data-ttu-id="112eb-126">Hatalar</span><span class="sxs-lookup"><span data-stu-id="112eb-126">Error</span></span>
- <span data-ttu-id="112eb-127">Çıkışının</span><span class="sxs-lookup"><span data-stu-id="112eb-127">Output</span></span>
- <span data-ttu-id="112eb-128">Sürdüğü</span><span class="sxs-lookup"><span data-stu-id="112eb-128">Progress</span></span>
- <span data-ttu-id="112eb-129">Kapsamlı</span><span class="sxs-lookup"><span data-stu-id="112eb-129">Verbose</span></span>
- <span data-ttu-id="112eb-130">Uyarılarla</span><span class="sxs-lookup"><span data-stu-id="112eb-130">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="112eb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112eb-131">-DefaultProfile</span></span>
<span data-ttu-id="112eb-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="112eb-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="112eb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112eb-133">CommonParameters</span></span>
<span data-ttu-id="112eb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="112eb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112eb-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="112eb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112eb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="112eb-136">INPUTS</span></span>

## <span data-ttu-id="112eb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="112eb-137">OUTPUTS</span></span>

### <span data-ttu-id="112eb-138">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="112eb-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="112eb-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="112eb-139">NOTES</span></span>

## <span data-ttu-id="112eb-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="112eb-140">RELATED LINKS</span></span>

[<span data-ttu-id="112eb-141">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="112eb-141">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="112eb-142">Özgeçmiş-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="112eb-142">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="112eb-143">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="112eb-143">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="112eb-144">Askıya al-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="112eb-144">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


