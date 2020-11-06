---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: 18551d6d839991cf0eb9e020c62fa0a24207d1e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591083"
---
# <span data-ttu-id="40fcf-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="40fcf-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="40fcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40fcf-102">SYNOPSIS</span></span>
<span data-ttu-id="40fcf-103">Bir Otomasyon iş çıkışı kaydının tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="40fcf-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40fcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40fcf-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40fcf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40fcf-105">DESCRIPTION</span></span>
<span data-ttu-id="40fcf-106">**Get-Azurermautomationjoi putrecord** cmdlet 'i, bir otomatikleştirme iş çıkışı kaydının tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="40fcf-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>

<span data-ttu-id="40fcf-107">**Get-Azurermautomationjoi Input** cmdlet 'inin bir veya daha fazla iş çıktısı kaydını listemesine rağmen, herhangi bir çıktı kaydının değerinin yalnızca bir özetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="40fcf-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="40fcf-108">Bir çıkış kaydının çıkış değerinin başlangıç türü olarak tam değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="40fcf-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="40fcf-109">Ayrıca özetin, bu cmdlet 'in çıktısı olan tam değerin aşılabildiği en büyük uzunluğu vardır.</span><span class="sxs-lookup"><span data-stu-id="40fcf-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="40fcf-110">**Get-Azurermautomationjoiınput** komutundan farklı olarak, bu cmdlet, herhangi bir çıkış kaydının çıkış değeri için kendi başlangıç türü olan tam değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="40fcf-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="40fcf-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40fcf-111">EXAMPLES</span></span>

### <span data-ttu-id="40fcf-112">Örnek 1: Otomasyon işinin tam çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="40fcf-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="40fcf-113">Bu komut, işin belirtilen iş KIMLIĞINE sahip tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="40fcf-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="40fcf-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40fcf-114">PARAMETERS</span></span>

### <span data-ttu-id="40fcf-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40fcf-115">-AutomationAccountName</span></span>
<span data-ttu-id="40fcf-116">Bu cmdlet 'in iş çıkışı kaydını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40fcf-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fcf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fcf-117">-DefaultProfile</span></span>
<span data-ttu-id="40fcf-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="40fcf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40fcf-119">-ID</span><span class="sxs-lookup"><span data-stu-id="40fcf-119">-Id</span></span>
<span data-ttu-id="40fcf-120">Bu cmdlet 'in alınacağı iş çıkışı kaydının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="40fcf-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fcf-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="40fcf-121">-JobId</span></span>
<span data-ttu-id="40fcf-122">Bu cmdlet 'in çıkış kaydı aldığı iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="40fcf-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fcf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40fcf-123">-ResourceGroupName</span></span>
<span data-ttu-id="40fcf-124">Bu cmdlet 'in iş çıkışı kaydını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="40fcf-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fcf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fcf-125">CommonParameters</span></span>
<span data-ttu-id="40fcf-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40fcf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fcf-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40fcf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fcf-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40fcf-128">INPUTS</span></span>

### <span data-ttu-id="40fcf-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="40fcf-129">None</span></span>
<span data-ttu-id="40fcf-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="40fcf-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40fcf-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40fcf-131">OUTPUTS</span></span>

### <span data-ttu-id="40fcf-132">Microsoft. Azure. Commands. Automation. model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="40fcf-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="40fcf-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40fcf-133">NOTES</span></span>

## <span data-ttu-id="40fcf-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40fcf-134">RELATED LINKS</span></span>

[<span data-ttu-id="40fcf-135">Get-Azurermautomationjoi yerleştir</span><span class="sxs-lookup"><span data-stu-id="40fcf-135">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)


