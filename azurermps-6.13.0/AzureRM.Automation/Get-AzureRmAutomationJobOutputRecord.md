---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: 63227ad14eb16c5a43e37095f7cfa80ccd8b9cce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572993"
---
# <span data-ttu-id="995e2-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="995e2-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="995e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="995e2-102">SYNOPSIS</span></span>
<span data-ttu-id="995e2-103">Bir Otomasyon iş çıkışı kaydının tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="995e2-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="995e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="995e2-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="995e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="995e2-105">DESCRIPTION</span></span>
<span data-ttu-id="995e2-106">**Get-Azurermautomationjoi putrecord** cmdlet 'i, bir otomatikleştirme iş çıkışı kaydının tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="995e2-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="995e2-107">**Get-Azurermautomationjoi Input** cmdlet 'inin bir veya daha fazla iş çıktısı kaydını listemesine rağmen, herhangi bir çıktı kaydının değerinin yalnızca bir özetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="995e2-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="995e2-108">Bir çıkış kaydının çıkış değerinin başlangıç türü olarak tam değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="995e2-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="995e2-109">Ayrıca özetin, bu cmdlet 'in çıktısı olan tam değerin aşılabildiği en büyük uzunluğu vardır.</span><span class="sxs-lookup"><span data-stu-id="995e2-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="995e2-110">**Get-Azurermautomationjoiınput** komutundan farklı olarak, bu cmdlet, herhangi bir çıkış kaydının çıkış değeri için kendi başlangıç türü olan tam değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="995e2-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="995e2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="995e2-111">EXAMPLES</span></span>

### <span data-ttu-id="995e2-112">Örnek 1: Otomasyon işinin tam çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="995e2-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="995e2-113">Bu komut, işin belirtilen iş KIMLIĞINE sahip tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="995e2-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="995e2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="995e2-114">PARAMETERS</span></span>

### <span data-ttu-id="995e2-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="995e2-115">-AutomationAccountName</span></span>
<span data-ttu-id="995e2-116">Bu cmdlet 'in iş çıkışı kaydını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="995e2-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="995e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="995e2-117">-DefaultProfile</span></span>
<span data-ttu-id="995e2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="995e2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="995e2-119">-ID</span><span class="sxs-lookup"><span data-stu-id="995e2-119">-Id</span></span>
<span data-ttu-id="995e2-120">Bu cmdlet 'in alınacağı iş çıkışı kaydının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="995e2-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="995e2-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="995e2-121">-JobId</span></span>
<span data-ttu-id="995e2-122">Bu cmdlet 'in çıkış kaydı aldığı iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="995e2-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="995e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="995e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="995e2-124">Bu cmdlet 'in iş çıkışı kaydını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="995e2-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="995e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="995e2-125">CommonParameters</span></span>
<span data-ttu-id="995e2-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="995e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="995e2-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="995e2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="995e2-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="995e2-128">INPUTS</span></span>

### <span data-ttu-id="995e2-129">System. Guid</span><span class="sxs-lookup"><span data-stu-id="995e2-129">System.Guid</span></span>

### <span data-ttu-id="995e2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="995e2-130">System.String</span></span>

## <span data-ttu-id="995e2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="995e2-131">OUTPUTS</span></span>

### <span data-ttu-id="995e2-132">Microsoft. Azure. Commands. Automation. model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="995e2-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="995e2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="995e2-133">NOTES</span></span>

## <span data-ttu-id="995e2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="995e2-134">RELATED LINKS</span></span>

[<span data-ttu-id="995e2-135">Get-Azurermautomationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="995e2-135">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)


