---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: f5c6976ca1fa398c38f642cef757f0e7956f40c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761609"
---
# <span data-ttu-id="a3e6d-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="a3e6d-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="a3e6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="a3e6d-103">Bir Otomasyon iş çıkışı kaydının tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="a3e6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3e6d-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3e6d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="a3e6d-106">**Get-Azautomationjoi Putrecord** cmdlet 'i, bir otomatikleştirme iş çıkışı kaydının tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="a3e6d-107">**Get-Azautomationjoverınput** cmdlet 'inin bir veya daha fazla iş çıkışı kaydını listemesine rağmen, herhangi bir çıktı kaydının değerinin yalnızca bir özetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="a3e6d-108">Bir çıkış kaydının çıkış değerinin başlangıç türü olarak tam değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="a3e6d-109">Ayrıca özetin, bu cmdlet 'in çıktısı olan tam değerin aşılabildiği en büyük uzunluğu vardır.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="a3e6d-110">**Get-Azautomationjoi Input** komutundan farklı olarak, bu cmdlet, herhangi bir çıkış kaydının çıkış değeri için ilk çıkış türünün tam değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="a3e6d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3e6d-111">EXAMPLES</span></span>

### <span data-ttu-id="a3e6d-112">Örnek 1: Otomasyon işinin tam çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="a3e6d-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="a3e6d-113">Bu komut, işin belirtilen iş KIMLIĞINE sahip tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="a3e6d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3e6d-114">PARAMETERS</span></span>

### <span data-ttu-id="a3e6d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a3e6d-115">-AutomationAccountName</span></span>
<span data-ttu-id="a3e6d-116">Bu cmdlet 'in iş çıkışı kaydını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="a3e6d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3e6d-117">-DefaultProfile</span></span>
<span data-ttu-id="a3e6d-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a3e6d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3e6d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="a3e6d-119">-Id</span></span>
<span data-ttu-id="a3e6d-120">Bu cmdlet 'in alınacağı iş çıkışı kaydının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="a3e6d-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="a3e6d-121">-JobId</span></span>
<span data-ttu-id="a3e6d-122">Bu cmdlet 'in çıkış kaydı aldığı iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="a3e6d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3e6d-123">-ResourceGroupName</span></span>
<span data-ttu-id="a3e6d-124">Bu cmdlet 'in iş çıkışı kaydını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="a3e6d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3e6d-125">CommonParameters</span></span>
<span data-ttu-id="a3e6d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3e6d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3e6d-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3e6d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3e6d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3e6d-128">INPUTS</span></span>

### <span data-ttu-id="a3e6d-129">System. Guid</span><span class="sxs-lookup"><span data-stu-id="a3e6d-129">System.Guid</span></span>

### <span data-ttu-id="a3e6d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a3e6d-130">System.String</span></span>

## <span data-ttu-id="a3e6d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3e6d-131">OUTPUTS</span></span>

### <span data-ttu-id="a3e6d-132">Microsoft. Azure. Commands. Automation. model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="a3e6d-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="a3e6d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3e6d-133">NOTES</span></span>

## <span data-ttu-id="a3e6d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3e6d-134">RELATED LINKS</span></span>

[<span data-ttu-id="a3e6d-135">Get-Azautomationjoi koyma</span><span class="sxs-lookup"><span data-stu-id="a3e6d-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

