---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279116"
---
# <span data-ttu-id="d65ca-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="d65ca-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="d65ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d65ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d65ca-103">Bir Otomasyon iş çıkışı kaydının tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="d65ca-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="d65ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d65ca-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d65ca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d65ca-105">DESCRIPTION</span></span>
<span data-ttu-id="d65ca-106">**Get-Azautomationjoi Putrecord** cmdlet 'i, bir otomatikleştirme iş çıkışı kaydının tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="d65ca-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="d65ca-107">**Get-Azautomationjoverınput** cmdlet 'inin bir veya daha fazla iş çıkışı kaydını listemesine rağmen, herhangi bir çıktı kaydının değerinin yalnızca bir özetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d65ca-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="d65ca-108">Bir çıkış kaydının çıkış değerinin başlangıç türü olarak tam değerini döndürmez.</span><span class="sxs-lookup"><span data-stu-id="d65ca-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="d65ca-109">Ayrıca özetin, bu cmdlet 'in çıktısı olan tam değerin aşılabildiği en büyük uzunluğu vardır.</span><span class="sxs-lookup"><span data-stu-id="d65ca-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="d65ca-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d65ca-110">EXAMPLES</span></span>

### <span data-ttu-id="d65ca-111">Örnek 1: Otomasyon işinin tam çıkışını alma</span><span class="sxs-lookup"><span data-stu-id="d65ca-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="d65ca-112">Bu komut, işin belirtilen iş KIMLIĞINE sahip tam çıkışını alır.</span><span class="sxs-lookup"><span data-stu-id="d65ca-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="d65ca-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d65ca-113">PARAMETERS</span></span>

### <span data-ttu-id="d65ca-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d65ca-114">-AutomationAccountName</span></span>
<span data-ttu-id="d65ca-115">Bu cmdlet 'in iş çıkışı kaydını aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d65ca-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="d65ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65ca-116">-DefaultProfile</span></span>
<span data-ttu-id="d65ca-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d65ca-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d65ca-118">-ID</span><span class="sxs-lookup"><span data-stu-id="d65ca-118">-Id</span></span>
<span data-ttu-id="d65ca-119">Bu cmdlet 'in alınacağı iş çıkışı kaydının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d65ca-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="d65ca-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="d65ca-120">-JobId</span></span>
<span data-ttu-id="d65ca-121">Bu cmdlet 'in çıkış kaydı aldığı iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d65ca-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="d65ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="d65ca-123">Bu cmdlet 'in iş çıkışı kaydını aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d65ca-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="d65ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65ca-124">CommonParameters</span></span>
<span data-ttu-id="d65ca-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d65ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65ca-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d65ca-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65ca-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d65ca-127">INPUTS</span></span>

### <span data-ttu-id="d65ca-128">System. Guid</span><span class="sxs-lookup"><span data-stu-id="d65ca-128">System.Guid</span></span>

### <span data-ttu-id="d65ca-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d65ca-129">System.String</span></span>

## <span data-ttu-id="d65ca-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d65ca-130">OUTPUTS</span></span>

### <span data-ttu-id="d65ca-131">Microsoft. Azure. Commands. Automation. model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="d65ca-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="d65ca-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d65ca-132">NOTES</span></span>

## <span data-ttu-id="d65ca-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d65ca-133">RELATED LINKS</span></span>

[<span data-ttu-id="d65ca-134">Get-Azautomationjoi koyma</span><span class="sxs-lookup"><span data-stu-id="d65ca-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


